# AI 工具比較表 — Workshop 講師參考 + 教學用

> 最後更新：2026-03-23
> 公司主要使用 Claude + Gemini 生態系

## 一、先搞懂：同一個 AI，不同的使用方式

> 「Claude」和「Gemini」各自有多種介面，就像 Google 有網頁版也有 App 一樣。
> 先把名詞搞清楚，後面討論才不會混淆。

### 依介面分類總覽

```
┌─────────────────────────────────────────────────────┐
│                    CLI（命令列）                       │
│  門檻：⭐⭐⭐ 需要熟悉 Terminal                        │
│  適合：工程師、自動化流程                               │
│                                                       │
│  ┌──────────────┐    ┌──────────────┐                │
│  │ Claude Code  │    │  Gemini CLI  │                │
│  └──────────────┘    └──────────────┘                │
├─────────────────────────────────────────────────────┤
│               網頁對話介面（Web Chat）                  │
│  門檻：⭐ 打開瀏覽器就能用                              │
│  適合：所有人                                          │
│                                                       │
│  ┌──────────────┐    ┌──────────────┐                │
│  │  Claude Desktop   │    │ gemini.google │                │
│  │              │    │   .com       │                │
│  └──────────────┘    └──────────────┘                │
├─────────────────────────────────────────────────────┤
│                 應用程式（App）                         │
│  門檻：⭐ 手機 / 桌面安裝即用                           │
│  適合：所有人，行動中使用                               │
│                                                       │
│  ┌──────────────┐    ┌──────────────┐                │
│  │  Claude App  │    │ Gemini App   │                │
│  │ (iOS/Android/│    │(iOS/Android/ │                │
│  │  Desktop)    │    │ Windows/Mac) │                │
│  └──────────────┘    └──────────────┘                │
└─────────────────────────────────────────────────────┘
```

---

## 二、講師參考：各介面詳細比較

### CLI（命令列介面）

> 工程師用的進階工具，一般同仁不需要會操作，但知道它存在就好。

| | Claude Code | Gemini CLI |
|---|---|---|
| **是什麼** | Anthropic 的 AI coding agent，跑在 Terminal 裡 | Google 的 AI CLI 工具（開源） |
| **誰在用** | 公司的工程師（Web Squad 等） | 工程師、資料分析師 |
| **能做什麼** | 寫程式、改 code、跑測試、自動化流程 | 分析檔案、生成程式碼 |
| **讀取檔案** | 直接讀電腦上的任何檔案 | 直接讀電腦上的任何檔案 |
| **跑程式** | 任何語言都能直接執行 | 任何語言都能直接執行（透過本地 shell） |
| **連接外部服務** | **MCP 生態系**（Slack、Google Calendar、Jira、GitHub 等，持續擴充） | 同樣支援 MCP（stdio/SSE/HTTP），可共用同一套 MCP server |
| **最強項** | 軟體開發 + MCP 生態系最成熟 | 大檔案分析（1M token 上下文）+ 免費 + 開源 |

**跟學員怎麼講**：

> 「你們可能聽過工程師說在用 Claude Code——那是跑在 Terminal 黑色畫面裡的工具，
> 可以直接改程式碼、連接 Slack 等服務。今天我們不會用到它，但如果未來你們有
> 自動化需求，可以請工程師幫忙用這個工具來做。」

---

### 網頁對話介面（Web Chat）

> 今天 Workshop 主要使用的介面，打開瀏覽器就能用。

| | Claude Desktop | gemini.google.com |
|---|---|---|
| **網址** | https://Claude Desktop | https://gemini.google.com |
| **登入** | 公司帳號 | Google 帳號 |
| **上傳檔案** | CSV/Excel/PDF/圖片（單檔 30MB，單次對話最多 20 檔） | CSV/Excel/PDF/圖片 + Google Drive 整合 |
| **圖像辨識** | 支援（上傳圖片分析） | **最強**（多模態辨識領先） |
| **跑程式算數據** | Python/JS（Analysis tool，自動執行） | Python（Colab 整合） |
| **上網搜尋** | 內建（附引用來源） | 內建（Google Search 整合最強） |
| **生成圖片** | 不行（可透過 Artifacts 產互動圖表、SVG） | Imagen 4 內建 |
| **生成影片** | 不行 | Veo 3（需付費方案） |
| **互動式圖表** | **Artifacts**（直接產可互動的圖表網頁） | 基本圖表 |
| **Google Workspace** | 透過 MCP 連接（需額外設定） | **原生整合**（Drive/Docs/Sheets/Gmail） |
| **繁體中文** | 自然流暢 | 普通（持續改善中） |

---

### 應用程式（App）

> 跟網頁版功能相同，差別在於可以在手機上用、支援語音輸入。

| | Claude App | Gemini App |
|---|---|---|
| **平台** | iOS / Android / macOS / Windows | iOS / Android / Windows（Mac beta 中） |
| **跟網頁版差異** | 功能相同，多了語音對話 | 功能相同，深度整合 Android 系統，Gemini Live 支援相機/螢幕分享 |
| **適合場景** | 通勤時用語音問問題、手機上快速查資料 | Android 用戶直接語音叫 Gemini、用相機即時辨識 |

---

## 三、Claude vs Gemini 什麼時候用哪個？

> 不管用哪個介面（網頁或 App），選擇邏輯都一樣：

| 場景 | 用 Claude | 用 Gemini |
|---|---|---|
| 分析 CSV/Excel 資料 | 上傳到 Claude Desktop，寫作品質好 | 資料已在 Google Sheets 就直接用 |
| 寫報告 / Email / 文案 | **首選**——結構清楚、繁中自然 | 可以，但繁中品質略遜 |
| 辨識圖片內容（截圖、照片、名片） | 可以 | **首選**——多模態辨識最強 |
| 產生圖片 | 不行 | **可以**（Imagen 4） |
| 操作 Google Drive/Docs/Sheets | 透過 MCP 可連接（需額外設定） | **原生整合最方便** |
| 連接 Slack / Jira / 其他服務（簡單） | **Claude Desktop Connectors**（一鍵授權） | Gemini 有 Google Workspace 原生整合 |
| 連接 Slack / Jira / 其他服務（進階） | **Claude Code** + MCP | **Gemini CLI** + MCP（共用同一套生態系） |
| 需要互動式 Dashboard | **Artifacts**（可互動的圖表網頁） | 基本圖表 |

**一句話記住**：文字分析找 Claude，看圖生圖找 Gemini。

---

## 四、教學用：學員看的簡化版

> 公司有 Claude 和 Gemini 兩套 AI 工具，各自有網頁版和 App。

### 名詞對照（先搞懂名字）

| 類型 | Claude 家族 | Gemini 家族 |
|---|---|---|
| **網頁版**（今天主要用） | Claude Desktop | gemini.google.com |
| **手機/電腦 App** | Claude App | Gemini App |
| **工程師用的 CLI** | Claude Code（Terminal 裡跑） | Gemini CLI（Terminal 裡跑） |

> CLI 是工程師的工具，你不需要會用。但知道它叫什麼，跟工程師溝通時不會搞混。

### 依場景選工具

| 我想要... | 用這個 | 為什麼 |
|---|---|---|
| 分析 CSV/Excel 資料 | **Claude Desktop** | 上傳 → 問問題 → 拿圖表和結論 |
| 寫報告 / Email / 文案 | **Claude Desktop** | 結構化寫作品質最穩，繁中最自然 |
| 辨識截圖、照片、掃描文件 | **Gemini** | 圖像辨識最準確 |
| 分析 Google Sheets 裡的資料 | **Gemini** | 直接連 Google Drive，不用下載上傳 |
| 需要生成配圖 | **Gemini** | Imagen 內建，描述就生圖 |
| 通勤中快速問問題 | **Claude App / Gemini App** | 手機上直接語音問 |
| 想做跨工具自動化（簡單） | **Claude Desktop**（Connectors） | 設定頁一鍵授權，免裝任何東西，支援 Slack、Jira、Google Calendar 等 50+ 服務 |
| 想做跨工具自動化（進階） | **Claude Code** / **Gemini CLI** + MCP | 工程師用 CLI 設定 MCP server，彈性最大，兩者共用同一套 MCP 生態系 |

### 搭配使用的建議流程

```
1. 圖片/截圖相關 → 先丟 Gemini 辨識整理成文字
2. 拿到結構化資料後 → 丟 Claude Desktop 做深入分析、產報告
3. 報告需要配圖 → 回 Gemini 生成
4. 資料在 Google Sheets → 直接用 Gemini
```

### 共通的 Prompt 技巧（所有介面都適用）

今天學的這些方法，不管在 Claude Desktop、Gemini 網頁版、還是 App 上都能用：
- 指定角色：「你是資深行銷分析師...」
- 分步驟：「第一步...第二步...」
- 給範例：「格式像這樣...」
- 指定輸出格式：「用表格」「用條列」
- 追問修改：「改成只看台灣客戶」「再精簡一點」
