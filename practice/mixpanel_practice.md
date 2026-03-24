# Mixpanel × AI 實作練習指南

> 本文件記錄了使用 AI 工具查詢 Mixpanel 數據並產出分析報告的完整對話流程，供工作坊學員跟著操作。

---

## Step 1：連接 Mixpanel Connector

在 Cowork 中加入 Mixpanel connector，連接成功後 AI 即可使用以下功能：

- **查詢與分析**：Run-Query、Get-Query-Schema、Get-Report
- **事件與屬性**：Get-Events、Get-Event-Details、Get-Property-Names、Get-Property-Values
- **Dashboard**：List-Dashboards、Get-Dashboard、Create-Dashboard

---

## Step 2：查詢專案列表

**Prompt：**

```
幫我查 product page 的 mweb 事件
```

**AI 做了什麼：**

1. 先呼叫 `Get-Projects` 取得所有專案列表
2. 辨識出 **KKday PC/M/App**（project id: `1683153`）是目標專案
3. 用 `Get-Events` 搜尋關鍵字 `product`，找到 25 個相關事件
4. 再搜尋 `ProdPg`，找到 76 個 Product Page 相關事件

**回傳的事件分類：**

| 類型 | 範例 |
|------|------|
| 頁面瀏覽 | `View_ProdPg`、`View_ProdPg_Optimization` |
| 點擊事件 | `Click_ProdPg_BookingBtn`、`Click_ProdPg_PackageCard`、`Click_ProdPg_Calendar` |
| 曝光事件 | `Impression_ProdPg_GetHelp`、`Impression_ProdPg_reviewSummaryCard` |
| 頁面載入 | `PageLoad_BusJpKosokuRouteProdPg`、`PageLoad_RailJrRouteProdPg` |

---

## Step 3：確認事件屬性

**AI 做了什麼：**

呼叫 `Get-Property-Names` 取得 `View_ProdPg` 事件的所有屬性，關鍵屬性包括：

| 屬性 | 說明 | 用途 |
|------|------|------|
| `Platform` | 平台（m.kkday.com / www.kkday.com / iOS / Android） | 篩選 mweb |
| `DisplayCountry` | 用戶所在國家 | 國家分佈分析 |
| `vertical` | 產品類型（TICKET / TOUR / DEFAULT） | 類型拆解 |
| `utm_source` | 流量來源 | 渠道歸因 |
| `prod_avg_rating` | 商品平均評分 | 品質分析 |
| `is_marketplace` | 是否為 marketplace 商品 | 供給側分析 |

---

## Step 4：確認篩選值

**AI 做了什麼：**

呼叫 `Get-Property-Values` 查詢 `Platform` 屬性的實際值，發現 mweb 對應的值是 `m.kkday.com`（不是 "mweb"）。

> 💡 **學習點**：不要假設屬性值，先用 Get-Property-Values 確認實際資料長什麼樣子。

---

## Step 5：跑數據查詢

**Prompt：**

```
View_ProdPg 是我們 product 頁的數據，你可以幫我想一個適合工作坊的題目嗎？
我想要讓產品團隊直接產生報表或是分析出產品增長的背後原因
```

**AI 詢問了 3 個釐清問題：**

1. 產出格式？→ PPT 簡報
2. 分析方向？→ 綜合分析（漏斗 + 歸因 + 行為）
3. 時間範圍？→ 最近 30 天

**AI 同時跑了多組查詢：**

### 查詢 A：每日流量趨勢

```json
{
  "report_type": "insights",
  "report": {
    "name": "ProdPg mweb daily trend",
    "metrics": [
      { "eventName": "View_ProdPg", "measurement": { "type": "basic", "math": "total" } },
      { "eventName": "View_ProdPg", "measurement": { "type": "basic", "math": "unique" } }
    ],
    "chartType": "line",
    "unit": "day",
    "dateRange": { "type": "relative", "range": { "unit": "day", "value": 30 } },
    "filters": [
      { "type": "string", "propertyName": "Platform", "operator": "equals", "value": "m.kkday.com" }
    ]
  }
}
```

**結果摘要：**
- 日均 PV：~169K
- 日均 UV：~100K
- 週末明顯高於工作日（+30%）

### 查詢 B：國家分佈

```json
{
  "report_type": "insights",
  "report": {
    "name": "ProdPg mweb by country",
    "metrics": [
      { "eventName": "View_ProdPg", "measurement": { "type": "basic", "math": "unique" } }
    ],
    "chartType": "bar",
    "dateRange": { "type": "relative", "range": { "unit": "day", "value": 30 } },
    "filters": [
      { "type": "string", "propertyName": "Platform", "operator": "equals", "value": "m.kkday.com" }
    ],
    "breakdowns": [
      { "metric": { "type": "property", "propertyName": "DisplayCountry" } }
    ]
  }
}
```

**結果摘要：**

| 國家 | 不重複用戶 | 佔比 |
|------|-----------|------|
| TW | 805,542 | 30.6% |
| JP | 716,833 | 27.2% |
| HK | 426,739 | 16.2% |
| US | 330,470 | 12.5% |
| KR | 145,530 | 5.5% |
| EN | 115,898 | 4.4% |

### 查詢 C：產品類型分佈

```json
{
  "report_type": "insights",
  "report": {
    "name": "ProdPg mweb by vertical",
    "metrics": [
      { "eventName": "View_ProdPg", "measurement": { "type": "basic", "math": "unique" } }
    ],
    "breakdowns": [
      { "metric": { "type": "property", "propertyName": "vertical" } }
    ]
  }
}
```

**結果摘要：**

| Vertical | 不重複用戶 | 佔比 |
|----------|-----------|------|
| DEFAULT | 1,006,710 | 35.3% |
| TICKET | 995,094 | 34.9% |
| TOUR | 763,394 | 26.8% |
| HOTEL_DYNAMIC | 52,007 | 1.8% |
| F&B | 24,364 | 0.9% |

---

## Step 6：產出分析簡報

AI 自動將上述數據整合成一份 10 頁的 PPT 簡報：

| 頁數 | 內容 | 視覺元素 |
|------|------|----------|
| 1 | 封面 | 深色背景 + 青色強調線 |
| 2 | 議程 | 5 個編號項目 |
| 3 | 流量總覽 | 大數字卡片 + 折線圖 |
| 4 | 國家分佈 | 長條圖 + Insight 卡片 |
| 5 | 流量來源 | 水平長條圖 + 警示框 |
| 6 | 產品類型 | 甜甜圈圖 + 數據列表 |
| 7 | 轉換漏斗 | 漏斗視覺化（深色背景） |
| 8 | 用戶行為 | 水平比例條 + 觀察框 |
| 9 | 關鍵發現 | 5 項行動方案（HIGH/MED/NEW） |
| 10 | 討論 | 3 個討論問題 |

---

## 關鍵發現總結

1. **方案卡片 → 預訂的轉換率僅 10%** → 優化價格展示、可用日期提示
2. **96% 流量缺少 UTM 標記** → 制定 UTM 規範
3. **評論互動率 3%，圖片 0.7%** → 測試更突出的評論摘要與圖片設計
4. **週末流量高於工作日 +30%** → 週末加強推播與限時優惠
5. **ChatGPT 已成 Top 3 可追蹤來源** → 研究 AI 搜尋優化策略（AIO）

---

## 練習題（學員自行操作）

試著用以下 prompt 與 AI 互動，練習從數據中找洞察：

### 練習 1：不同國家的轉換率比較

```
幫我比較 TW、JP、HK 三個國家在 mweb 上，
從 View_ProdPg → Click_ProdPg_BookingBtn 的轉換率差異
```

### 練習 2：週末 vs 工作日行為差異

```
幫我分析 mweb 的 View_ProdPg，
週末和工作日的用戶行為有什麼不同？
可以看看點擊方案、查看評論、查看圖片的比例差異
```

### 練習 3：特定 Vertical 深入分析

```
針對 TICKET vertical 的商品頁，
幫我分析哪些國家的用戶最多，轉換率如何？
```

### 練習 4：流量來源品質分析

```
幫我比較不同 utm_source 進到 product page 後的行為差異，
哪個來源的用戶互動最深？
```

---

## Tips

- 不確定屬性值長什麼樣？先請 AI 用 `Get-Property-Values` 查
- 想看漏斗？至少需要 2 個步驟的事件
- 想看趨勢？用 line chart + day 為單位
- 想做比較？善用 breakdown 拆解維度
- AI 可以同時跑多組查詢，不用一個一個來
