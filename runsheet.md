# Workshop Runsheet — 2025/03/25 全球策略行銷處

> 學員：Celine Goh, Yoshita, Daniel, YZ
> 教學：Rex（主講）+ Jeff（助教）
> 旁聽：Ming, Mike

## 時間表

| 時間 | Phase | 內容 | 負責 |
|------|-------|------|------|
| 13:00–13:20 | 1. 破冰 | 自我介紹 → 破冰提問 → 今天約定 | Rex |
| 13:20–13:50 | 2. 暖場 Demo | Demo 1 做網頁 + Demo 2 讀資料 | Rex |
| 13:50–14:00 | 2.5 AI 能與不能 | 3 min 心智模型 → 投票選 2 個深入主題 | Rex |
| 14:00–14:45 | 3a. 深入主題 1 | 釐清 → Live Coding → 成果展示 | Rex + Jeff |
| 14:45–14:55 | — 休息 | — | — |
| 14:55–15:40 | 3b. 深入主題 2 | 釐清 → Live Coding → 成果展示 | Rex + Jeff |
| 15:40–16:20 | 4. 學員練習 | claude.ai 動手做 | 全員 |
| 16:20–16:50 | 5. 收尾 | 總結 → Prompt 框架 → AI 工具全景比較 → 後續支援 | Rex |
| 16:50–17:00 | 6. Buffer | 自由交流 / Ming & Mike 總結 | 全員 |

## 設備 Checklist

### 前 3 天（3/22 前）
- [ ] 4 份假資料 CSV 已建立（✅ 已完成）
- [ ] 每個 demo 劇本自己跑一遍（確認 10 min 內完成）
- [ ] 每個 demo prompt 也在 claude.ai 網頁版跑一遍（確認回應品質穩定）
- [ ] 確認投影 / 螢幕分享設備
- [ ] 和 Jeff 對齊分工

### 前 1 天（3/24）
- [ ] 確認學員的電腦都能上 claude.ai
- [ ] 列印 cheatsheet（4 份 + 備用）
- [ ] 測試公司 WiFi + Claude Code 連線穩定度
- [ ] 準備 backup：每個 demo 的成功結果截圖（卡住時直接秀圖繼續講）

### 當天
- [ ] 早到 15 min 測設備
- [ ] 開好 terminal + 瀏覽器 + data/ 資料夾
- [ ] 準備白板筆 / 便利貼（投票用）
- [ ] terminal 字體調大（讓投影看得清楚）

## 分工

| 角色 | Rex | Jeff |
|------|-----|------|
| 主講 & Live Coding | ✅ | |
| 用 claude.ai 同步示範 | | ✅ |
| 學員練習時巡場 | 2 人 | 2 人 |
| 記錄學員提問 & 回饋 | | ✅ |
| 處理技術問題 | ✅ | ✅ |

## 風險應對

| 風險 | 應對 |
|------|------|
| Claude Code 卡住 / 回應慢 | 切 claude.ai 網頁版繼續 |
| 需求太複雜做不完 | 用預備的「縮小版」prompt |
| 學員沒興趣 | 問「你昨天花最多時間在什麼？」即時切主題 |
| 學員期望 AI 直接操作後台系統 | 開場說明：「今天做到 AI 幫你整理好設定，後台自動化是下一階段」 |
| 網路不穩 | 準備離線截圖 / 預錄畫面 |
| Ming/Mike 問超範圍的 | 記下來當 follow-up，不硬答 |

## Demo 前暖機指令

開場前先跑一次 Claude Code 讓它 warm up：
```bash
echo "Hello Claude" | claude --no-input
```

確保 terminal 已在 workshop data 目錄：
```bash
cd /Users/rex.tsou/kkday-b2c-web-workspace/workshop/2025-03-25-global-marketing
```
