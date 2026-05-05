# Open Design 快速參考卡
## Deck & Prototype 提示詞範本

---

## 🎯 快速命令

### 啟動 Open Design
```bash
cd open-design
pnpm tools-dev run web
# 打開 http://localhost:5175
```

### 重啟 Daemon（如果出現問題）
```bash
pnpm tools-dev restart
```

---

## 📊 Deck 模式 - 提示詞範本

### 範本 1：季度規劃企劃案
```
create a Q2 2026 business review deck.

sections:
- cover: "Q2 2026 Review" with our logo
- kpis: 4 cards showing: Revenue +15%, Users +8K, Features 12, Bugs Fixed 87
- accomplishments: 5 major launches with icons
- learnings: 3 key insights from this quarter
- next quarter: roadmap for Q3

design:
- use our purple (#714eff) for titles and primary elements
- use orange (#f97824) for highlights and important metrics
- make it magazine-style, professional, 8-10 slides
```

### 範本 2：銷售/投資者提案
```
create an investment pitch deck for Series B funding round.

content:
- problem: 1 slide describing market pain point
- solution: 1-2 slides on our unique approach
- market: 1 slide with TAM/SAM/SOM numbers
- product: 2 slides with key features and screenshots
- team: 1 slide with founder photos and bios
- traction: 1 slide with metrics (users, revenue, growth)
- ask: 1 slide with funding amount and use of funds

style:
- professional but not corporate
- lots of breathing room, clean layout
- use our purple as primary brand color
- add green for positive metrics, red for challenges
```

### 範本 3：月度狀態報告
```
create a monthly status report for March 2026.

structure:
- highlight: 1 major achievement this month
- metrics: progress on 3-4 OKRs (show trend lines if possible)
- completed: bulleted list of 10-15 completed tasks
- in progress: 5-6 ongoing initiatives with timeline
- blockers: 2-3 challenges and how we're addressing them
- next month: 3-4 priority focus areas
- team: any hiring, departures, or kudos

colors:
- use brand purple for headings
- green backgrounds for completed/positive items
- orange for in-progress
- red for blockers
```

### 範本 4：內部培訓材料
```
create a training deck on [TOPIC].

slides:
- title slide with topic
- why this matters: 1 slide
- key concepts: 3-5 slides (one concept per slide)
- real-world examples: 2-3 slides with case studies
- best practices: 2-3 actionable takeaways
- resources: 1 slide with links and further reading
- Q&A: blank slide for discussion

make it visual with icons and diagrams. use our colors to highlight key points.
keep text minimal (headlines + 2-3 bullet points per slide).
```

---

## 🖼️ Prototype 模式 - 提示詞範本

### 範本 1：功能列表/看板
```
create a feature request voting page.

components:
- header: "Feature Requests" with purple background
- search/filter: search bar + filter dropdown (status, priority)
- feature cards: 
  - title (16px semibold)
  - description (14px regular, 2 lines max)
  - tags: 2-3 tags using our badge system (success green, warning orange)
  - vote count: "👍 42 votes" with primary color
  - vote button: purple primary button "Vote Now"
  - submitted by: "Jane D. • 3 days ago" (small gray text)
- pagination or infinite scroll at bottom

requirements:
- use our brand colors throughout
- primary action buttons in purple (#714eff)
- secondary actions in orange (#f97824)
- success badges in green (#1ba279)
- 44px minimum touch targets
- responsive (1 col mobile, 2-3 cols desktop)
- all spacing follow our 8px grid
```

### 範本 2：設定/管理面板
```
create a user account settings page.

sections:
- account info: 
  - avatar (circular, 80px)
  - name field (editable)
  - email field (read-only)
  - member since date
- preferences:
  - email notifications toggle
  - marketing emails checkbox
  - theme selector (light/dark)
  - language dropdown
- danger zone:
  - "Export my data" button (secondary)
  - "Delete account" button (red danger style)

requirements:
- group related settings in cards (spacing: lg/24px between)
- use our primary purple for save/submit buttons
- use red/danger color for destructive actions
- all form inputs 44px minimum height
- focus states with 2px primary color border
- responsive layout
```

### 範本 3：儀表板/Analytics
```
create a product analytics dashboard.

layout:
- header: "Analytics" title + date range picker
- metrics row: 4 cards showing
  - active users (28,450)
  - new signups (1,230 this week)
  - features launched (12 this month)
  - bug fixes (87 this month)
- charts row: 2 sections
  - left: line chart of user growth over 6 months (use our purple)
  - right: pie chart of feature adoption (use color ramp: purple, orange, green, blue)
- table: recent feature releases
  - columns: feature name, launch date, adoption %, status
  - status: success (green), in-progress (orange), paused (gray)
- cta button: "Download Report" at bottom

requirements:
- large, readable numbers (24-32px)
- smooth transitions on chart hover
- zebra striping on table rows
- use semantic colors (green = positive, orange = caution, red = negative)
- responsive (stack vertically on mobile)
```

### 範本 4：著陸頁面
```
create a landing page for [PRODUCT/SERVICE].

structure:
- hero section:
  - headline: [main value prop]
  - subheadline: [supporting description]
  - CTA button: "Get Started" (purple primary)
  - hero image/mockup: [product in use]
- features section:
  - 3 feature cards with:
    - icon (colorful)
    - feature name (16px semibold)
    - description (14px regular)
- social proof / pricing section (if applicable)
- footer:
  - links: product, pricing, about, contact
  - copyright

design:
- use brand purple for primary CTA buttons
- use orange for secondary CTAs or highlights
- white/light background with subtle borders
- lots of whitespace
- clean, modern, professional
- mobile responsive (1 col mobile, 2-3 cols desktop)
```

### 範本 5：行動應用
```
create a mobile app mockup (375px width) for [APP NAME].

key screens:
1. onboarding: welcome + permission request
2. home: main navigation + content feed
3. details: expanded view of selected item with actions
4. settings: preferences and account options

requirements:
- 44px minimum tap targets (buttons, links, form inputs)
- use our purple for primary actions
- use orange for highlights/secondary
- bottom navigation bar for main sections
- header with logo/title
- card-based layout for content
- show loading states and empty states
- responsive to different phone orientations

make it feel native and polished.
```

---

## 🎨 色彩參考速查表

### 主色
| 用途 | 顏色 | 代碼 | Hex |
|------|------|------|-----|
| 主要按鈕、CTA | Purple | primary | #714eff |
| 主要懸停 | Purple-Dark | primary-hover | #5a27f2 |
| 淺色背景 | Purple-Light | primary-light | #dcd1ff |
| 極淺背景 | Purple-Palest | primary-palest | #f0ecff |

### 輔助色
| 用途 | 顏色 | 代碼 | Hex |
|------|------|------|-----|
| 次要按鈕 | Orange | secondary | #f97824 |
| 警告/強調 | Orange-Light | secondary-light | #ffe0cb |

### 語義色
| 用途 | 顏色 | 代碼 | Hex |
|------|------|------|-----|
| 成功/確認 | Success | — | #1ba279 |
| 錯誤/危險 | Danger | — | #e60013 |
| 警告 | Warning | — | #faad14 |
| 資訊 | Info | — | #096dd9 |

### 中立色
| 用途 | 顏色 | 代碼 | Hex |
|------|------|------|-----|
| 主要背景 | Light | — | #ffffff |
| 頁面背景 | Background | — | #fafafa |
| 邊框 | Subtle | — | #e0e0e0 |
| 主要文字 | Dark | — | #000000 |

---

## 📐 排版速查表

### 大小
| 用途 | 大小 | 粗細 |
|------|------|------|
| 頁面標題 | 32px | 700 (Bold) |
| 區段標題 | 24px | 600 (Semibold) |
| 卡片標題 | 16px | 600 (Semibold) |
| 主要內容 | 14px | 400 (Regular) |
| 小文字/標籤 | 12px | 400 (Regular) |

### 行高
- 標題: 1.2-1.3
- 段落: 1.5
- 標籤: 1.4

---

## 📏 間距速查表

| Token | 大小 | 用途 |
|-------|------|------|
| xs | 4px | icon 間距、微調 |
| sm | 8px | 內部間距、按鈕邊距 |
| md | 16px | 組件間距 |
| lg | 24px | 區塊間距 |
| xl | 32px | 主要間距 |
| 2xl | 48px | 版塊分隔 |

---

## 🔲 圓角速查表

| Token | 大小 | 用途 |
|-------|------|------|
| none | 0px | 邊框、銳邊 |
| sm | 4px | 按鈕、小元素 |
| md | 8px | 標準組件 |
| lg | 12px | 卡片、模態框 |
| full | 9999px | 圓形、藥丸按鈕 |

---

## 💡 常用提示詞片段

### 加入無障礙性
```
ensure all interactive elements are 44px minimum height.
all color contrasts meet WCAG AA standards.
add focus rings for keyboard navigation.
include proper alt text for all images.
```

### 要求特定樣式
```
use magazine-style layout with lots of breathing room.
make it clean and minimalist, no visual clutter.
professional but approachable tone.
modern and contemporary feel.
```

### 要求互動性
```
make buttons interactive and show hover states.
add smooth transitions between states.
show loading indicators for long-running operations.
provide success/error feedback for user actions.
```

### 要求響應式設計
```
responsive design that works on mobile, tablet, and desktop.
1 column layout on mobile, 2-3 columns on tablet, 3-4 on desktop.
touch-friendly on mobile (44px+ tap targets).
adapt font sizes for readability on all screen sizes.
```

---

## 🚀 工作流程快速檢查清單

### 開始一個新項目
- [ ] 確認 Open Design 已啟動 (`pnpm tools-dev run web`)
- [ ] 驗證 DESIGN.md 已上傳
- [ ] 確認 Design System 選擇器顯示 "UniOpen Brand"
- [ ] 測試提示詞確認色彩正確

### 生成 Deck
- [ ] 切換到 Deck Skill (`guizang-ppt` 或 `html-ppt`)
- [ ] 編寫清晰的內容提示詞
- [ ] 檢查預覽中的色彩和排版
- [ ] 導出為 PPTX（可在 PowerPoint 中編輯）

### 生成 Prototype
- [ ] 確認 Skill 是 `web-prototype`
- [ ] 寫詳細的功能和設計要求
- [ ] 檢查預覽的互動性
- [ ] 驗證 44px 最小觸發目標
- [ ] 導出為 HTML 或複製程式碼

### 收集反饋並迭代
- [ ] 分享預覽連結給利益相關者
- [ ] 收集反饋信息
- [ ] 在聊天框輸入修改要求
- [ ] 檢查更新的預覽
- [ ] 重複直到滿意

---

## 📞 快速救援

| 問題 | 解決方案 |
|------|--------|
| 按鈕還是藍色不是紫色 | 檢查 Design System 選擇器，重新上傳 DESIGN.md |
| Daemon 不響應 | `pnpm tools-dev restart` |
| 找不到 Claude Code | 安裝 `npm install -g @anthropic-ai/claude-code` 或使用 BYOK |
| 生成太慢 | 簡化提示詞，等待 2-3 分鐘 |
| Preview 空白 | 刷新頁面，檢查瀏覽器控制台錯誤 |

---

## 📚 進階用法

### 保存常用提示詞

在本地建立 `prompts.txt` 檔案，記錄你最常用的提示詞：

```
# 企劃案範本
[你的企劃案提示詞...]

# 原型範本
[你的原型提示詞...]

# 列表頁面
[你的列表提示詞...]
```

需要時，複製貼上即可。

### 與團隊分享

1. **分享預覽連結**
   - Preview 窗格右下有 Share 按鈕
   - 生成臨時連結，可給 PM/設計師開啟

2. **導出完整檔案**
   - 保存到 Disk → 整個專案資料夾
   - 導出為 PPTX/HTML/PDF → 單個檔案
   - 複製程式碼 → 貼到你的代碼庫

### 版本控制

提交你的 DESIGN.md 到 Git：

```bash
git add DESIGN.md
git commit -m "feat: update design system colors and typography"
git push
```

---

**上一步完成？** ✅ 返回執行指南繼續！

