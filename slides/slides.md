---
theme: default
title: AI 工具概覽
info: KKday 全球策略行銷處工作坊 2026/03/25
colorSchema: light
aspectRatio: 16/9
fonts:
  sans: Noto Sans TC
  mono: Fira Code
---

# AI 工具概覽

快速搞懂名詞，建立正確期待

<div class="abs-br m-6 text-sm opacity-50">
KKday 全球策略行銷處工作坊 — 2026/03/25
</div>

<!--
「在我們開始動手之前，先花幾分鐘把一些名詞搞清楚。
這些詞你們可能在新聞或同事聊天中聽過，今天一次幫大家對齊。」
-->

---

# AI 到底是什麼？

<div class="grid grid-cols-2 gap-12 mt-4">
<div>

### 你可以想成...

<div class="text-xl mt-4 leading-relaxed">
一個讀過<span class="text-blue-600 font-bold">整個網路</span>的文字助手<br>
你打字問它，它打字回你
</div>

<div class="mt-6 text-sm opacity-70">

- 正式名稱：**LLM**（Large Language Model，大型語言模型）
- 它的原理：看過海量文字，學會「接下來最可能的回答」
- 不是搜尋引擎——它是在「生成」答案，不是在「查」答案

</div>

</div>
<div>

### 你不需要知道的

<div class="mt-4 text-base opacity-60">

- 神經網路怎麼運作
- 模型怎麼訓練的
- 參數有幾億個

</div>

<div class="mt-6 p-4 bg-blue-50 rounded-lg text-base">
你只需要知道：<br>
<strong>怎麼問問題，讓它給你有用的答案</strong>
</div>

</div>
</div>

<!--
「AI 這個詞很大，今天我們講的 AI 其實就是大型語言模型，英文叫 LLM。
你可以把它想成一個讀過整個網路的文字助手，你用文字跟它互動。
它的強項是語言理解和生成，不是什麼都會。」
-->

---

# 今天會用到的名詞

<div class="grid grid-cols-3 gap-6 mt-6">

<div class="p-5 bg-amber-50 rounded-lg">
<div class="text-lg font-bold mb-2">Prompt（提示詞）</div>
<div class="text-sm">你打給 AI 的<strong>指令或問題</strong></div>
<div class="mt-3 text-sm opacity-70">
就像跟同事交辦工作——<br>說得越清楚，結果越好
</div>
</div>

<div class="p-5 bg-green-50 rounded-lg">
<div class="text-lg font-bold mb-2">上下文（Context）</div>
<div class="text-sm">AI 記住的<strong>這次對話內容</strong></div>
<div class="mt-3 text-sm opacity-70">
你不用每次重新描述——<br>它記得你前面說了什麼
</div>
</div>

<div class="p-5 bg-purple-50 rounded-lg">
<div class="text-lg font-bold mb-2">Artifacts</div>
<div class="text-sm">Claude 的<strong>即時預覽視窗</strong></div>
<div class="mt-3 text-sm opacity-70">
做出的網頁、圖表會直接<br>顯示在右邊讓你互動
</div>
</div>

</div>

<div class="mt-6 text-center text-sm opacity-50">
等等 Demo 時會實際看到這些東西
</div>

<!--
「今天最常用到三個詞：
- Prompt 就是你打給 AI 的話，中文叫提示詞。說得越清楚，AI 回的越好。
- 上下文就是 AI 會記住這次對話講過什麼，所以你可以一直追問、一直修改。
- Artifacts 是 Claude 的一個功能，做出來的東西會直接預覽在旁邊，等等 Demo 就會看到。」
-->

---

# 你可能會聽到的名詞

<div class="mt-2 text-sm opacity-60 mb-4">不需要記住，知道是什麼就好</div>

<div class="grid grid-cols-2 gap-x-12 gap-y-4">

<div class="flex items-start gap-3">
<div class="text-base font-bold text-blue-700 w-36 shrink-0">多模態</div>
<div class="text-sm">AI 不只看得懂文字，還能看懂<strong>圖片、PDF、影片</strong>。<br>Gemini 的圖像辨識就是多模態能力。</div>
</div>

<div class="flex items-start gap-3">
<div class="text-base font-bold text-blue-700 w-36 shrink-0">Token</div>
<div class="text-sm">AI 讀寫的計量單位，大約 <strong>1 個中文字 ≈ 1~2 個 token</strong>。<br>輸入和輸出越多，消耗越多 token。</div>
</div>

<div class="flex items-start gap-3">
<div class="text-base font-bold text-blue-700 w-36 shrink-0">CLI（命令列）</div>
<div class="text-sm">用文字指令操作的介面（黑色畫面）。<br>Claude Code、Gemini CLI 都是 CLI 工具，<strong>適合自動化流程</strong>。</div>
</div>

<div class="flex items-start gap-3">
<div class="text-base font-bold text-blue-700 w-36 shrink-0">MCP</div>
<div class="text-sm">讓 AI 連接外部服務（Slack、Jira 等）的<strong>標準協定</strong>。<br>像 USB 一樣，統一了 AI 跟各種工具的接法。</div>
</div>

<div class="flex items-start gap-3">
<div class="text-base font-bold text-blue-700 w-36 shrink-0">Connectors</div>
<div class="text-sm">Claude 內建的「<strong>一鍵連接</strong>」功能。<br>不需要工程師，在設定頁授權就能連 Slack 等服務。</div>
</div>

<div class="flex items-start gap-3">
<div class="text-base font-bold text-blue-700 w-36 shrink-0">Hallucination</div>
<div class="text-sm">AI <strong>一本正經地胡說八道</strong>。<br>看起來很有自信，但答案是編的。所以要 double check。</div>
</div>

</div>

<!--
「這頁的名詞你不需要記住，但以後看新聞或跟工程師聊天時會比較有感覺。
最重要的是最後一個 Hallucination——AI 幻覺，就是 AI 會一本正經地編答案。
這就是為什麼我們一直強調要 double check。」
-->

---

# 公司有哪些 AI 工具？

<div class="grid grid-cols-3 gap-6 mt-4">

<div class="p-4 rounded-lg border border-gray-200">
<div class="text-center text-sm font-bold opacity-60 mb-3">網頁版</div>
<div class="flex justify-center gap-4">
<div class="text-center">
<div class="px-3 py-2 bg-amber-50 rounded font-bold text-sm">claude.ai</div>
</div>
<div class="text-center">
<div class="px-3 py-2 bg-blue-50 rounded font-bold text-sm">gemini.google.com</div>
</div>
</div>
<div class="text-center text-xs mt-2 opacity-60">打開瀏覽器就能用</div>
</div>

<div class="p-4 rounded-lg border-2 border-blue-200 bg-blue-50">
<div class="text-center text-sm font-bold opacity-60 mb-3">桌面 App（今天主要用）</div>
<div class="flex justify-center gap-4">
<div class="text-center">
<div class="px-3 py-2 bg-amber-100 rounded font-bold text-sm">Claude Desktop</div>
</div>
<div class="text-center">
<div class="px-3 py-2 bg-blue-100 rounded font-bold text-sm">Gemini App</div>
</div>
</div>
<div class="text-center text-xs mt-2 opacity-60">安裝在電腦上，支援 Connectors</div>
</div>

<div class="p-4 rounded-lg border border-gray-200 opacity-60">
<div class="text-center text-sm font-bold opacity-60 mb-3">CLI（工程師用）</div>
<div class="flex justify-center gap-4">
<div class="text-center">
<div class="px-3 py-2 bg-gray-100 rounded font-bold text-sm">Claude Code</div>
</div>
<div class="text-center">
<div class="px-3 py-2 bg-gray-100 rounded font-bold text-sm">Gemini CLI</div>
</div>
</div>
<div class="text-center text-xs mt-2 opacity-60">Terminal 裡跑，適合自動化流程</div>
</div>

</div>

<div class="mt-6 text-center text-base">
同一個 AI，不同的使用方式——就像 Google 有網頁版也有 App
</div>

<!--
「Claude 跟 Gemini 各自有三種使用方式：網頁版、桌面 App、還有工程師用的 CLI。
今天我們主要用 Claude Desktop——就是裝在電腦上的桌面 App，功能跟網頁版一樣，
但多了 Connectors 可以直接連 Slack、Google Calendar 等服務。
CLI 是用文字指令操作的進階介面，適合做自動化。有興趣的話之後可以試試看。」
-->

---
layout: section
---

# Claude Desktop 介紹

不只是對話框——你的 AI 協作中心

<!--
「接下來花幾分鐘帶大家認識今天的主角——Claude Desktop。
它不只是把網頁版包成一個 App，而是多了很多獨家功能。」
-->

---

# Claude Desktop：三個分頁

<div class="grid grid-cols-2 gap-6">
<div>
<img src="/screenshots/desktop-tabs-1.png" alt="Claude Desktop 三個分頁總覽" class="rounded-lg shadow-lg" style="max-height: 300px;" />
</div>
<div class="flex flex-col gap-3 justify-center">

<div class="p-3 bg-amber-50 rounded-lg">
<span class="font-bold">Chat</span> — 一般對話、問答、分析資料
</div>

<div class="p-3 bg-purple-50 rounded-lg">
<span class="font-bold">Cowork</span> — 背景代理人，交辦後自動執行
</div>

<div class="p-3 bg-green-50 rounded-lg">
<span class="font-bold">Code</span> — 開發助手，讀取編輯本地檔案
</div>

</div>
</div>

<!--
「打開 Claude Desktop，最上面有三個分頁：Chat、Cowork、Code。
今天我們主要會用 Chat，但 Cowork 也非常值得認識。」
-->

---

# Chat 分頁：你最熟悉的對話介面

<div class="grid grid-cols-2 gap-6">
<div>
<img src="/screenshots/desktop-tabs-2.png" alt="Chat 分頁介面" class="rounded-lg shadow-lg" style="max-height: 300px;" />
</div>
<div class="text-sm">

**怎麼用**

1. **打字問問題**：下方輸入框直接輸入
2. **上傳檔案**：點 **+** 按鈕，或拖曳檔案進來
3. **選模型**：右下角切換（Opus 4.6 / Sonnet 等）
4. **快捷按鈕**：Code / Write / Create / Learn / From Drive

**跟網頁版的差別**

- 支援 **Connectors**（直接連 Slack、Google Drive 等）
- Mac 雙擊 Option 鍵 → **Quick Entry**（截圖快速提問）

</div>
</div>

<!--
「Chat 分頁長這樣，跟網頁版很像。
下方輸入框打字就能問問題，點加號可以上傳檔案。
桌面版多了 Connectors 跟 Quick Entry——Mac 上雙擊 Option 鍵
可以快速截圖問 AI，等等可以試試看。」
-->

---

# Cowork 分頁：你的背景代理人

<div class="grid grid-cols-2 gap-6">
<div>
<img src="/screenshots/desktop-tabs-3.png" alt="Cowork 分頁介面" class="rounded-lg shadow-lg" style="max-height: 280px;" />
</div>
<div class="text-sm">

**Chat vs Cowork**

| | Chat | Cowork |
|---|---|---|
| 要盯著嗎？ | 要 | **不用，去做別的事** |
| 檔案存取 | 手動上傳 | **直接讀整個資料夾** |
| 適合 | 快速問答 | **耗時複雜任務** |
| 執行方式 | 即時對話 | **背景虛擬機自動跑** |

</div>
</div>

<div class="mt-3 p-3 bg-purple-50 rounded-lg text-sm">

**怎麼用**：點「Cowork」→ 選資料夾（Work in a folder）→ 描述任務 → 按「**Let's go**」→ 去喝杯咖啡

</div>

<!--
「Cowork 是 Claude Desktop 最強大的功能。
你交辦一個任務，它會自己翻閱資料夾、規劃步驟、產出檔案。
你不用一直守在螢幕前，做完會通知你。
Chat 是即時對話，Cowork 是委派任務。」
-->

---

# Dispatch：手機交辦，電腦執行

<div class="grid grid-cols-2 gap-6">
<div class="flex justify-center">
<img src="/screenshots/dispatch-setup-1.png" alt="Dispatch 設定畫面" class="rounded-lg shadow-lg" style="max-height: 310px;" />
</div>
<div class="text-sm">

**手機 = 對講機，電腦 = 執行者**

用手機 Claude App 遠端交辦任務，辦公室電腦自動執行。

**設定方式**

1. 更新 Desktop + 手機 App 到最新版
2. Cowork 分頁 → 左側「**Dispatch**」→「**Get started**」
3. 開啟檔案存取 + 保持電腦喚醒
4. 手機 App 傳訊息，電腦就開始執行

<div class="mt-3 p-2 bg-orange-50 rounded text-xs">
注意：電腦需<strong>保持開機且 App 開著</strong><br>
目前僅 Pro / Max 方案可用，<strong>Team 方案尚未開放</strong>
</div>

</div>
</div>

<!--
「Dispatch 是 2026 年 3 月剛推出的新功能。
你在外面開會，用手機跟 Claude 說要做什麼，
辦公室的電腦就會開始處理。唯一限制是電腦要保持開機。」
-->

---

# Scheduled Tasks：讓 Claude 定時幫你做事

<div class="mt-2">
<img src="/screenshots/scheduled-tasks.png" alt="排程任務設定" class="rounded-lg shadow-lg mx-auto" style="max-height: 120px;" />
</div>

<div class="grid grid-cols-2 gap-8 mt-4 text-sm">
<div>

**怎麼設定**

- 在 Cowork 輸入 `/schedule`
- 或左側「Scheduled」→「+ New task」

**可選頻率**：每小時 / 每天 / 平日 / 每週 / 手動觸發

</div>
<div>

**行銷應用情境**

- 每天早上 9 點自動整理昨天的行銷數據
- 每週一產出上週各管道 ROAS 報表
- 每天追蹤競品社群動態並摘要
- 定時檢查 coupon 到期日並提醒

</div>
</div>

<div class="mt-3 text-xs opacity-60 text-center">
電腦需保持開機；錯過的排程會在喚醒時自動補跑
</div>

<!--
「排程任務：設好時間跟內容，Claude 定時自動執行。
例如每天早上 9 點自動整理行銷數據，完全不用手動。」
-->

---

# Connectors：一鍵連接你的工作工具

<div class="grid grid-cols-2 gap-6 text-sm">
<div>

**設定步驟**

1. 對話框點 **+** →「**Connectors**」
2. 瀏覽服務，點「**Connect**」
3. 完成 OAuth 授權（一鍵）
4. 所有對話都能用

**支援服務**：Google Drive / Slack / Jira / Google Calendar / Notion / GitHub 等 50+

<span class="text-xs opacity-60">完整清單：claude.ai/connectors</span>

</div>
<div>

<div class="p-3 bg-amber-50 rounded-lg">

**之前**：開 Slack 複製 → 貼到 Claude → 複製結果 → 貼回 Slack

**現在**：「幫我看 Slack #marketing 頻道今天有什麼重點」

</div>

<div class="mt-3">

**行銷情境**

- 「Google Drive 裡的報表，跟上週比有什麼變化？」
- 「把分析結果發到 Slack #weekly-report」
- 「Jira 上這週有哪些行銷相關 ticket？」

</div>
</div>
</div>

<!--
「Connectors 讓 Claude 直接連你的工具，不用複製貼上。
設定很簡單：點加號、選服務、授權，一次設定所有對話都能用。」
-->

---

# Claude Desktop：快速上手

<div class="grid grid-cols-3 gap-6 mt-2 text-sm">
<div>

**安裝**

1. **claude.ai/download** 下載
2. macOS 11+ / Windows 10+
3. 用公司帳號登入

</div>
<div>

**Chat 操作**

- 輸入框打字發問
- 點 **+** 上傳檔案或加 Connectors
- 拖曳檔案直接上傳
- Mac 雙擊 **Option** → Quick Entry

</div>
<div>

**Cowork 操作**

1. 點「**Cowork**」分頁
2. Settings → 授權資料夾 + 填寫偏好
3. 描述任務 →「**Let's go**」

</div>
</div>

<div class="mt-4 p-3 bg-blue-50 rounded-lg text-sm">

**小技巧**：輸入 `/` 可看所有斜線指令（`/schedule` 建排程、`/search` 搜尋等）；右下角可切換 AI 模型

</div>

<!--
「下載安裝到 claude.ai/download，登入就好。
Chat 操作跟網頁版一樣。Cowork 第一次用先到設定授權資料夾。
輸入斜線可以看到所有快捷指令。」
-->

---
layout: section
---

# AI 能與不能

建立正確期待，讓你更知道怎麼用

<!--
「OK 名詞對齊了，接下來聊聊 AI 的邊界。
剛才大家看到 AI 可以寫網頁、分析資料，看起來很厲害，
但在我們往下走之前，先聊聊它做得到和做不到的事。」
-->

---
layout: two-cols
---

# AI 擅長 <span class="text-green-600">✓</span>

<v-clicks>

- **讀懂資料、做計算、找規律**<br><span class="text-sm opacity-70">→ 剛才的客戶分析</span>
- **寫文字：報告、Email、翻譯**<br><span class="text-sm opacity-70">→ 等等會看到</span>
- **記住這次對話的上下文**<br><span class="text-sm opacity-70">→ 剛才我們連續追問，不用重新描述</span>
- **把重複的邏輯自動化**<br><span class="text-sm opacity-70">→ 等等深入主題會做</span>

</v-clicks>

::right::

# AI 做不到 <span class="text-orange-500">✗</span>

<v-clicks>

- **搜尋結果不保證 100% 正確**<br><span class="text-sm opacity-70">可以上網搜，但還是要自己驗證</span>
- **操作後台系統需要額外設定**<br><span class="text-sm opacity-70">透過 Computer Use、MCP 等工具可以做到，但需要設定和監督</span>
- **數字、日期一定要 double check**<br><span class="text-sm opacity-70">AI 會很有自信地給出錯誤答案（Hallucination！）</span>

</v-clicks>

<!--
用剛才的 demo 舉例帶過每個擅長項目。
做不到的部分重點強調「不保證正確」——呼應前面講的 Hallucination。
-->

---
layout: center
---

# 把 AI 當成一個<br>反應超快、但需要你 double check 的<span class="text-blue-600">實習生</span>

<div class="mt-8 text-xl opacity-70">
你給方向，它幫你跑腿。
</div>

<!--
一句話總結。
接著轉場：「OK，那我們來選今天要深入做哪兩個主題。」
-->

---
layout: section
---

# Claude vs Gemini 怎麼選？

什麼時候開 Claude，什麼時候開 Gemini

<!--
「今天我們主要用 Claude Desktop，但公司也有 Gemini。
最後幾分鐘幫大家搞清楚：什麼時候開 Claude，什麼時候開 Gemini。」
-->

---

# 依場景選工具

| 我想要... | 用這個 | 一句話原因 |
|---|---|---|
| 分析 CSV / Excel | **Claude** | 上傳 → 問問題 → 拿圖表和結論 |
| 寫報告 / Email / 文案 | **Claude** | 結構化寫作最穩，繁中最自然 |
| 辨識截圖、照片、掃描文件 | **Gemini** | 圖像辨識最準確（多模態最強） |
| 分析 Google Sheets | **Gemini** | 直連 Google Drive，不用下載上傳 |
| 需要生成配圖 | **Gemini** | Imagen 內建，描述就生圖 |

<style>
td:nth-child(2) { font-weight: bold; }
</style>

<!--
逐行帶過，每個都用一句話解釋。
強調不是哪個比較好，而是各有擅長。
「辨識截圖那邊，就是前面講到的多模態能力。」
-->

---
layout: center
---

# 文字分析找 <span class="text-amber-600">Claude</span>，看圖生圖找 <span class="text-blue-600">Gemini</span>

<!--
一句話記住。停 2 秒讓大家記住這句話。
-->

---

# 搭配使用的建議流程

```mermaid
graph LR
    A["📷 收到截圖 / 照片"] -->|丟給| B["Gemini 辨識整理"]
    B -->|拿到文字| C["Claude 深入分析"]
    C -->|需要配圖| D["Gemini 生成圖片"]

    style B fill:#DBEAFE,stroke:#2563EB,color:#1E3A5F
    style C fill:#FEF3C7,stroke:#D97706,color:#78350F
    style D fill:#DBEAFE,stroke:#2563EB,color:#1E3A5F
```

<div class="mt-6 text-center text-lg">
兩個工具各有擅長，搭配著用效果最好
</div>

<!--
「實際工作上，一件事可能兩個都用到。」

1. 收到截圖/照片 → Gemini 辨識整理成文字
2. 拿到文字資料 → Claude 深入分析、產報告
3. 報告需要配圖 → Gemini 生成

舉例：客戶傳了一張手寫訂單照片 → Gemini 辨識 → Claude 做分析報告 → Gemini 生配圖
-->

---

# Prompt 技巧，兩邊都通用

<v-clicks>

- **描述情境與目標** — 「我要準備週會報告，對象是行銷主管，需要各管道的 ROAS 比較」
- **給範例** — 「格式像這樣：名字 / 國家 / 金額」
- **指定格式** — 「用表格」「用條列」「用 email 格式」
- **追問修改** — 「改成只看台灣客戶」「再精簡一點」

</v-clicks>

<div v-click class="mt-4 p-3 bg-amber-50 rounded-lg text-sm">

**常見迷思**：「要先跟 AI 說『你是一個資深分析師』才會回答得好」——現在的 AI 已經很擅長理解意圖，**把你的情境和目標講清楚**比指定角色更有效。你也不需要手動把任務拆成步驟，AI 會自己規劃。

</div>

<div v-click class="mt-3 text-center text-lg font-bold text-blue-700">
帶走的是方法，不是只有一個工具
</div>

<!--
「你們可能在網路上看過『要先指定角色 AI 才會回答得好』——
這在早期的模型確實有效，但現在的 Claude 和 Gemini 已經很聰明了。
與其說『你是資深分析師』，不如把你的情境講清楚：
『我要準備週會報告，對象是行銷主管，需要各管道 ROAS 比較』。
AI 會自動用對的專業程度回答你。同樣地，你也不用手動拆步驟，
把目標講清楚，AI 會自己規劃怎麼做。」
-->

---
layout: center
---

# 帶走一個行動

<div class="text-2xl mt-6 leading-relaxed">
回去找一件<span class="text-blue-600 font-bold">你這週要做的事</span><br>
先用 Claude Desktop 試試看
</div>

<div class="mt-8 text-lg opacity-70">
卡住了就截圖丟 Slack 問 Rex 或 Jeff<br>
下週我們做個 15 分鐘 follow-up，聽聽大家的實戰經驗
</div>

<!--
「回去之後，找一件你這週要做的事，先用 Claude Desktop 試試看。
卡住了就截圖丟 Slack 問我們。下週我們做個 15 分鐘 follow-up，聽聯大家的實戰經驗。」
-->

---
layout: center
class: text-center
---

# 謝謝！

<div class="mt-4 text-lg opacity-70">
Slack 找 Rex 或 Jeff
</div>

<div class="mt-2 text-sm opacity-50">
有確定要做的自動化需求 → 開 JIRA ticket
</div>

<!--
交給 Ming & Mike 總結，或進入自由 Q&A 時間。
-->
