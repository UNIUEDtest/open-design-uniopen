# UniOpen × Open Design 執行指南
## 5 步完整上手 Deck 和 Prototype 模式

---

## 前置準備（5 分鐘）

### 你需要的東西

1. **Node.js v24** — [下載](https://nodejs.org/)
2. **一個 API 金鑰**（選其一）：
   - Anthropic Claude API key（推薦）
   - OpenAI API key
   - 其他相容提供商
3. **本指南提供的 2 個檔案**：
   - `DESIGN.md` ✅ 已準備好
   - 本指南本身 ✅ 就是這個

### 快速檢查

```bash
# 檢查 Node 版本
node --version  # 應該是 v24.x

# 檢查 pnpm 版本
pnpm --version  # 應該是 10.33.x
```

---

## 📋 第 1 步：安裝 Open Design（15 分鐘）

### 1.0 前置：確保 pnpm 安裝到全局路徑

Open Design 需要 pnpm 10.33.x。如果你的系統還沒有安裝，或出現「command not found: pnpm」的錯誤，先執行這個：

```bash
# 用 npm 安裝全局 pnpm
npm install -g pnpm

# 驗證
pnpm --version  # 應該輸出 10.33.2+
```

**如果上面的命令成功，你會看到：**
```
pnpm --version # 輸出 10.33.2+
added 1 package in 2s
```

✅ **如果已經有 pnpm 10.33.x，跳過這個步驟，直接進到 1.1**

---

### 1.1 克隆專案

```bash
# 克隆已包含 UniOpen 設計系統的團隊 repo
git clone https://github.com/UNIUEDtest/open-design-uniopen.git
cd open-design-uniopen
```

### 1.2 安裝依賴

```bash
# 啟用 corepack
corepack enable

# 驗證 pnpm 版本
pnpm --version  # 必須是 10.33.2

# 安裝依賴
pnpm install
```

### 1.3 啟動本地開發環境

```bash
pnpm tools-dev run web
```

**預期輸出：**
```
✓ daemon listening on http://localhost:7456
✓ web listening on http://localhost:5175
✓ open http://localhost:5175 in your browser
```

### 1.4 打開瀏覽器

在瀏覽器中打開 `http://localhost:5175`，你會看到：

```
┌─────────────────────────────────────────────────┐
│  ⚙️ Welcome to Open Design                       │
│                                                 │
│  [Paste your API key]                           │
│  ┌──────────────────────────────────────────┐  │
│  │ sk-ant-... (or sk-...)                   │  │
│  └──────────────────────────────────────────┘  │
│                                                 │
│  [Detect Agents] [Start]                       │
└─────────────────────────────────────────────────┘
```

**如果沒有 Claude Code 或其他代理工具安裝，選 "Detect Agents" 會提供 BYOK 代理選項。**

---

## 🎨 第 2 步：確認 Design System 已就位（2 分鐘）

### 2.1 驗證設計系統已在正確位置

clone 下來的 repo 已經包含 uniopen 設計系統，直接確認即可：

```bash
# 確認檔案存在
ls -la design-systems/uniopen/DESIGN.md
```

**預期輸出：**
```
-rw-r--r--  1 user  staff  11KB  May  4 12:00 design-systems/uniopen/DESIGN.md
```

✅ **看到這個輸出就代表設計系統已就位，不需要任何額外操作。**

### 2.2 重啟 daemon 以載入設計系統

```bash
# 停止目前的 daemon
pnpm tools-dev stop

# 等待 2 秒
sleep 2

# 重新啟動
pnpm tools-dev run web
```

**預期輸出：**
```
Open Design dev server ready
Web: http://127.0.0.1:XXXXX/
Daemon: http://127.0.0.1:XXXXX/
```

### 2.3 驗證設計系統已載入

1. **重新整理瀏覽器**（Cmd+R 或 Ctrl+R）
2. **進入任一個 Project**（或建立新的）
3. **查看頂部的「Design System」下拉菜單**
4. **搜尋 "uniopen" **

應該能看到：
```
┌─ Design System
│  ├─ Neutral Modern (Default)
│  ├─ Warm Editorial
│  ├─ ... 70+ 內建系統 ...
│  └─ UniOpen Brand ✨ ← 你的系統已載入！
```

### 2.4 測試設計系統是否正確應用

選擇 **「uniopen Brand」**，然後在聊天框輸入：

```
create a button with our brand primary color.
the button should be purple (#714eff) with white text.
```

**預期結果：**
在右側 Preview 窗格中，你應該看到一個**紫色按鈕（#714eff）**，而不是預設的藍色。

✅ **如果看到紫色按鈕，你的設計系統已成功整合！**

---

## 📊 第 3 步：執行 Deck 模式 - 製作企劃案（20 分鐘）

Deck 模式用於快速生成幻燈片、企劃案、呈現文件。

### 3.1 選擇 Deck 模式

在 Open Design UI 中：

1. 上方左側找到 **Skill** 選擇器（預設是 "web-prototype"）
2. 點擊改為 **guizang-ppt** 或 **html-ppt**（Deck 專用 Skill）
3. 確認 **Design System** 仍是 **UniOpen Brand**

```
Skill: [web-prototype ▼]  →  [guizang-ppt ▼]
Design System: [UniOpen Brand ▼] ✓ Keep
```

### 3.2 生成你的第一份企劃案

在聊天框輸入以下提示詞：

```
create a Q2 2026 product roadmap deck in our brand colors.
include:
- cover slide with UniOpen logo and "Q2 Product Roadmap"
- timeline showing: January features (Q1 carryover), February sprints, March milestones
- each slide should have purple (#714eff) accent color
- add 3 key metrics at the bottom
- make it magazine-style, professional but not stiff
```

**Expected Output:**
1. 右側 Preview 窗格會顯示幻燈片預覽
2. 左側 Chat 面板會流式輸出生成計畫（TodoWrite）
3. 約 30-60 秒後，一份完整的 Deck 會出現在 Preview 中

### 3.3 檢查和導出

**在 Preview 窗格中：**

```
┌─────────────────────────────────────┐
│ Slide 1/7                    ⬅️ ➡️   │
│                                     │
│   Q2 Product Roadmap               │
│   (紫色背景，橙色重點)              │
│                                     │
│ [Save to Disk] [Export as HTML]    │
│ [Export as PDF] [Export as PPTX]   │
└─────────────────────────────────────┘
```

- **Save to Disk** → 保存到 `./.od/artifacts/` 資料夾
- **Export as PPTX** → 下載為 PowerPoint（可在 Office 中編輯）
- **Export as PDF** → 下載為 PDF 分享

### 3.4 實戰練習

試試其他企劃案：

```
# 月度進度報告
create a March 2026 progress report slide deck.
include sections:
- achievements: list 5 major launches
- challenges: 3 blockers we overcame
- next month priorities: roadmap for April
use our secondary orange color #f97824 for highlights

---

# 銷售提案
create a sales pitch deck for a B2B partnership.
include sections:
- problem statement (headline)
- solution overview (2 slides)
- use cases (3 slides with icons)
- pricing model (table)
- closing CTA
ensure brand colors purple and orange are used throughout
```

**💡 Tip:** 每份企劃案不同，AI 會根據你的提示詞創意調整設計。你可以迭代改進：

```
the deck looks good but make the text darker and add more breathing room between slides
```

---

## 🖼️ 第 4 步：執行 Prototype 模式 - 快速原型（20 分鐘）

Prototype 模式用於生成網頁/App 原型，用於快速驗證想法。

### 4.1 選擇 Prototype 模式

1. 切換 **Skill** 回 **web-prototype**（預設）
2. **Design System** 維持 **UniOpen Brand**

```
Skill: [guizang-ppt ▼]  →  [web-prototype ▼]
Design System: [UniOpen Brand ▼] ✓ Keep
```

### 4.2 生成你的第一個原型

在聊天框輸入：

```
create a product feature request voting page for our product.
include:
- header with "Feature Requests" title using our brand
- search bar to filter requests
- list of 5 feature cards with:
  - feature title
  - description (2 lines)
  - vote count (with thumbs up icon)
  - tags (using our badge component)
- primary action button "Submit Request" in purple
use our full color system: purple for primary, orange for highlights, green for success badges
make it responsive (works on mobile and desktop)
```

**Expected Output:**

1. **Preview 窗格顯示實時原型**（可互動！）
2. **HTML 程式碼** 會在左側 Chat 面板流式顯示
3. **約 45-90 秒後**，完整的功能原型會出現

### 4.3 互動測試

在 Preview 中你可以：
- ✅ 點擊按鈕、輸入文字
- ✅ 檢查響應式設計（拉寬/縮小視窗）
- ✅ 驗證色彩是否符合品牌規範

### 4.4 提供反饋並迭代

如果原型需要調整，直接在聊天框說出來：

```
# 調整設計
the spacing is too tight. make the cards have more padding and add more gap between them.

---

# 新增功能
add a filter dropdown at the top to filter by: All, Bugs, Feature Requests, Improvements

---

# 改變配色
use more of our orange secondary color in the badges instead of just green and red
```

**AI 會立即重新生成原型，Preview 會實時更新。**

### 4.5 導出原型

**在 Preview 窗格中：**

```
[Save to Disk] [Copy Code] [Export as HTML] [Share Link]
```

- **Save to Disk** → 保存完整專案到本地
- **Copy Code** → 複製 HTML/CSS/JS，貼到你的專案
- **Export as HTML** → 下載單個 HTML 檔案，可離線打開
- **Share Link** → 生成臨時分享連結（可給 PM/設計師評審）

### 4.6 實戰練習

試試其他原型：

```
# 設定頁面
create a user settings page with sections:
- account info (email, name, avatar)
- notification preferences (toggle switches for different notification types)
- theme selector (light/dark)
- privacy settings (checkboxes)
use our design tokens for spacing and colors. make sure all form elements are 44px minimum height for accessibility

---

# 儀表板
create a simple product analytics dashboard showing:
- 4 key metrics at the top (cards): users, signups, features launched, bugs fixed
- a line chart showing user growth over 6 months
- a table of recent feature releases
use our purple primary for charts and our orange for highlighted rows

---

# 行動應用原型
create a mobile app mockup (375px width) for a task management app:
- header with "My Tasks" and add button
- 3 tabs: Today, This Week, Backlog
- task cards with: title, due date, priority badge (red for high, orange for medium, green for low)
- swipe hint at the bottom
ensure touch targets are 44px minimum
```

---

## ✅ 第 5 步：團隊協作工作流程（持續）

現在你已經有了完整的工作流程。以下是建議的團隊使用方式：

### 5.1 設計師工作流程

```
Figma 中高保真設計 → 
  ↓
提取到 DESIGN.md（已完成）→ 
  ↓
Open Design 快速原型 → 
  ↓
PM/開發反饋 → 
  ↓
修改 → Figma 迭代
```

### 5.2 PM 工作流程

```
想法 → 
  Open Design 快速企劃案 → 
  Deck 幻燈片 → 
  分享給利益相關者 → 
  反饋收集
```

### 5.3 開發團隊工作流程

```
功能需求 → 
  Open Design 快速原型 → 
  確認 UI 與設計系統一致 → 
  複製程式碼到專案 → 
  微調與最佳化
```

### 5.4 保持設計系統同步

**每月檢查清單：**

1. ✅ Figma 設計規範有變更？
2. ✅ 更新 `DESIGN.md` 中的對應部分
3. ✅ 在 Open Design 中重新上傳 `DESIGN.md`
4. ✅ 生成一份測試原型確認變更生效

---

## 🐛 常見問題 & 故障排除

### Q1: 按鈕顏色還是藍色，不是紫色？

**A:** 設計系統沒有載入。檢查：
1. 右上方 **Design System** 選擇器是否是 **UniOpen Brand**？
2. 如果沒看到，重啟 daemon：
```bash
pnpm tools-dev stop
sleep 2
pnpm tools-dev run web
```
3. 重新整理瀏覽器（Cmd+R）

### Q2: "Detect Agents" 找不到 Claude Code 或其他代理？

**A:** 你需要安裝代理 CLI。快速修復：
```bash
# 安裝 Claude Code
npm install -g @anthropic-ai/claude-code

# 或使用 BYOK (Bring Your Own Key)
# 貼上 Anthropic/OpenAI API 密鑰在歡迎畫面
```

### Q3: Preview 中的原型不互動？

**A:** 刷新頁面或重啟 daemon：
```bash
pnpm tools-dev restart
```

### Q4: 生成速度太慢？

**A:** 可能是 API 限流。試試：
1. 簡化提示詞（少一些細節要求）
2. 等待 2-3 分鐘後重試
3. 檢查 API 使用量配額

### Q5: 能導出為 Figma 嗎？

**A:** 暫時不能直接出到 Figma，但可以：
1. 匯出為 HTML
2. 截圖並手動在 Figma 中參考
3. 複製程式碼到專案後截圖匯入

---

## 📞 獲得幫助

### 官方資源

- **GitHub Issues**: https://github.com/nexu-io/open-design/issues
- **Docs**: https://github.com/nexu-io/open-design (QUICKSTART.md)
- **討論**: GitHub Discussions

### 你的團隊資源

- **DESIGN.md 完整版本**: 本文件夾中的 `DESIGN.md`
- **Figma 設計規範**: https://www.figma.com/design/CMaxycoplHn78tNRevovH7/🍊​-uniopen-brand-guidelines
- **色彩代幣完整文檔**: 你上傳的原始 `DESIGN.md` (色彩層級定義)

---

## 🎉 下一步

恭喜！你已經完全掌握了 Open Design。接下來可以：

### 短期（本週）
- [ ] 用 Deck 模式製作一份真實企劃案
- [ ] 用 Prototype 模式生成 2-3 個實際功能頁面
- [ ] 讓 PM/設計師試用 1-2 次

### 中期（本月）
- [ ] 為常見工作流程寫 Prompt 範本（保存供重複使用）
- [ ] 訓練整個團隊使用 Open Design
- [ ] 根據反饋調整 DESIGN.md

### 長期（持續）
- [ ] 建立「Prompt 庫」（設計、企劃、開發常用提示詞）
- [ ] 集成到 CI/CD（自動生成設計文件/原型）
- [ ] 探索 Open Design 的 Skill 定制功能

---

## 📝 筆記與記錄

**第一次啟動時間**: ________________
**首份成功的 Deck 時間**: ________________
**首份成功的 Prototype 時間**: ________________
**團隊開始使用的日期**: ________________

**遇到的問題**:
```
_________________________________
_________________________________
_________________________________
```

**改進建議**:
```
_________________________________
_________________________________
_________________________________
```

---

**祝你使用愉快！🚀**

