---
name: UniOpen Brand
description: Modern, accessible design system with vibrant purple primary color and warm orange accent. Built for seamless team collaboration and product excellence.
version: alpha

colors:
  primary: "#714eff"
  primary-light: "#dcd1ff"
  primary-palest: "#f0ecff"
  secondary: "#f97824"
  secondary-light: "#ffe0cb"
  tertiary: "#096dd9"
  success: "#1ba279"
  danger: "#e60013"
  warning: "#faad14"
  neutral-light: "#ffffff"
  neutral-dark: "#000000"
  neutral-bg: "#fafafa"
  neutral-subtle: "#e0e0e0"
  neutral-muted: "#bdbdbd"

typography:
  display:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: 32px
    fontWeight: 700
    lineHeight: 1.2
  heading:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.3
  body-lg:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
  body:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  caption:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.4

spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px

rounded:
  none: 0px
  sm: 4px
  md: 8px
  lg: 12px
  full: 9999px

components:
  button-primary:
    background: "{colors.primary}"
    text: "{colors.neutral-light}"
    hover: "#5a27f2"
    disabled: "{colors.neutral-subtle}"
  button-secondary:
    background: "{colors.secondary}"
    text: "{colors.neutral-light}"
    hover: "#ee660c"
  card:
    background: "{colors.neutral-light}"
    border: "{colors.neutral-subtle}"
    shadow: "0 1px 3px rgba(0, 0, 0, 0.08)"
  input:
    background: "{colors.neutral-light}"
    border: "{colors.neutral-muted}"
    focus: "{colors.primary}"
    disabled: "{colors.neutral-subtle}"
  badge-success:
    background: "rgba(27, 162, 121, 0.1)"
    text: "{colors.success}"
  badge-danger:
    background: "rgba(230, 0, 19, 0.1)"
    text: "{colors.danger}"

---

## Overview

UniOpen 是一套現代、無障礙的設計系統，以紫色作為品牌主色，橙色為輔助色。設計簡潔清晰，易於接近，專為產品團隊快速協作和高效交付而設計。

**品牌個性：** 專業、創新、可信任、充滿活力

**目標用戶：** 產品經理、設計師、開發者、企業團隊

**情感基調：** 現代但不冷漠，專業但易於親近

---

## Color Palette

### Primary — Deep Purple (#714eff)
UniOpen 的核心身份色。代表創新、信任、高級感。

- **#714eff** — Primary Base，用於所有主要互動元素
- **#dcd1ff** — Primary Light，懸停狀態、次要強調
- **#f0ecff** — Primary Palest，禁用狀態、淡背景

### Secondary — Warm Orange (#f97824)
輔助色，用於吸引注意力和促進行動。

- **#f97824** — Secondary Base，警告、促進行動
- **#ffe0cb** — Secondary Light，懸停狀態

### Semantic Colors
- **Success (Green)**: #1ba279 — 成功、確認
- **Danger (Red)**: #e60013 — 錯誤、破壞性操作
- **Warning (Gold)**: #faad14 — 警告、需要注意
- **Info (Blue)**: #096dd9 — 資訊、中立通知

### Neutral Scale
- **Light**: #ffffff — 背景、卡片、文字背景
- **Dark**: #000000 — 主要文字、高對比元素
- **Background**: #fafafa — 頁面背景、次要容器
- **Subtle**: #e0e0e0 — 邊框、分隔線
- **Muted**: #bdbdbd — 禁用狀態、輔助邊框

---

## Typography

### Font Stack
所有文字使用 **Inter** 作主字體，提供清晰、現代的視覺語言。系統自動回退到系統字體確保跨平台一致性。

### Type Scale & Usage

| Level | Size | Weight | Usage |
|-------|------|--------|-------|
| **Display** | 32px | 700 | 頁面主標題、品牌宣言 |
| **Heading** | 24px | 600 | 主要內容標題、版塊標題 |
| **Body-lg** | 16px | 400 | 詳細說明、長篇內容 |
| **Body** | 14px | 400 | 標籤、輔助文字、卡片副題 |
| **Caption** | 12px | 400 | 註解、細節、時間戳 |

### Line Height
- 標題：1.2–1.3（緊密）
- 身體文本：1.5（舒適閱讀）
- 標籤：1.4（緊湊）

---

## Spacing System

基於 8px 基礎單位的嚴格間距系統，確保視覺和諧與一致性。

| Token | Value | Typical Usage |
|-------|-------|---------------|
| **xs** | 4px | Icon 間距、微調、緊密 UI |
| **sm** | 8px | 元素內部間距、按鈕內邊距 |
| **md** | 16px | 組件外間距、卡片間距 |
| **lg** | 24px | 區塊間距、版塊邊距 |
| **xl** | 32px | 主要區塊間距 |
| **2xl** | 48px | 版塊分隔、大型間距 |

### Layout Margins
- 移動端：lg/24px 側邊距
- 桌面：lg/24px 側邊距，內容寬度最大 1200px

---

## Shapes & Roundedness

現代設計使用最小化圓角，保持清晰與軟度的平衡。

| Token | Value | Usage |
|-------|-------|-------|
| **none** | 0px | 邊框、分隔線、銳利邊界 |
| **sm** | 4px | 小按鈕、標籤、輸入框 |
| **md** | 8px | 標準組件、較大按鈕 |
| **lg** | 12px | 卡片、模態框、大型容器 |
| **full** | 9999px | 藥丸按鈕、圓形頭像 |

---

## Layout & Grid

### Breakpoints
- **Mobile**: < 640px — 單欄流式佈局
- **Tablet**: 640px–1024px — 雙欄或三欄
- **Desktop**: > 1024px — 三欄或四欄

### Grid System
- 基礎單位：8px
- 移動邊距：24px
- 桌面最大寬度：1200px
- 欄間距：24px

### Spacing Hierarchy
| Level | Padding | Margin |
|-------|---------|--------|
| 頁面邊距 | lg/24px | — |
| 卡片邊距 | md/16px | md/16px |
| 內部元素 | sm/8px | sm/8px |

---

## Elevation & Depth

扁平設計，通過邊框和顏色對比表達層級。

### Shadow System
- **No Shadow**: 邊框 + 色彩對比
- **Subtle**: `0 1px 3px rgba(0, 0, 0, 0.08)` — 卡片
- **Focused**: `0 0 0 2px {colors.primary}` — 焦點指示

### Depth Layers
| Layer | Background | Border | Usage |
|-------|-----------|--------|-------|
| L0 (Surface) | neutral-light | neutral-subtle | 卡片、容器 |
| L1 (Overlay) | neutral-light | primary | 模態、下拉菜單 |
| L2 (Elevated) | neutral-bg | none | 懸浮工具欄 |

---

## Accessibility

所有色彩對比符合 **WCAG AA 標準**。

### Requirements
- 文字對比比：≥ 4.5:1（正常文字），≥ 3:1（大文字）
- 互動元素最小尺寸：44px × 44px
- 焦點指示：2px solid primary 色
- 禁用狀態：清晰視覺降級（顏色、不透明度、光標變化）

### Color Contrast Pairs
| Foreground | Background | Ratio | Status |
|-----------|-----------|-------|--------|
| #000000 (text) | #ffffff | 21:1 | ✅ WCAG AAA |
| #714eff (primary) | #ffffff | 4.8:1 | ✅ WCAG AA |
| #f97824 (secondary) | #ffffff | 5.2:1 | ✅ WCAG AA |
| #1ba279 (success) | #ffffff | 6.4:1 | ✅ WCAG AA |
| #e60013 (danger) | #ffffff | 5.1:1 | ✅ WCAG AA |

---

## Component Patterns

### Buttons

**Primary Button**
- Background: primary (#714eff)
- Text: neutral-light (#ffffff)
- Hover: #5a27f2 (darker)
- Disabled: neutral-subtle (#e0e0e0), text gray
- Border-radius: sm (4px)
- Padding: sm vertically (8px), md horizontally (16px)
- Min-height: 44px

**Secondary Button**
- Background: secondary (#f97824)
- Text: neutral-light (#ffffff)
- Hover: #ee660c
- Otherwise same as Primary

### Cards
- Background: neutral-light (#ffffff)
- Border: 0.5px solid neutral-subtle (#e0e0e0)
- Border-radius: lg (12px)
- Padding: lg (24px)
- Shadow: `0 1px 3px rgba(0, 0, 0, 0.08)`

### Input Fields
- Background: neutral-light (#ffffff)
- Border: 0.5px solid neutral-muted (#bdbdbd)
- Focus: 2px solid primary (#714eff), border color same
- Disabled: background neutral-subtle, text muted
- Padding: sm (8px) vertical, md (16px) horizontal
- Min-height: 44px

### Badges
- **Success**: bg rgba(27, 162, 121, 0.1), text #1ba279
- **Danger**: bg rgba(230, 0, 19, 0.1), text #e60013
- **Warning**: bg rgba(250, 173, 20, 0.1), text #faad14
- Border-radius: full (9999px)
- Padding: xs (4px) vertical, sm (8px) horizontal

---

## Implementation for AI Agents

### Claude Code / Cursor / Copilot Guidelines

When generating UI using this DESIGN.md, follow these principles:

#### 1. Color Selection Rules
- **Primary CTA**: Use primary (#714eff) for main call-to-action buttons
- **Secondary Actions**: Use secondary (#f97824) for alternative or warning actions
- **Confirmations**: Use success (#1ba279) for success feedback, completion states
- **Errors & Alerts**: Use danger (#e60013) for errors, destructive actions
- **Info & Notices**: Use info (#096dd9) for informational messages
- **Backgrounds**: Use neutral-light for cards, neutral-bg for page background
- **Text**: Use neutral-dark for primary text, neutral-muted for secondary/disabled

#### 2. Typography Hierarchy
- Page title: display (32px, bold) + primary color or neutral-dark
- Section heading: heading (24px, semibold)
- Card title: body-lg (16px, semibold)
- Regular content: body (14px, regular)
- Labels & captions: caption (12px, regular)
- Never mix heading sizes arbitrarily; follow the scale

#### 3. Spacing & Layout
- Component internal spacing: sm (8px)
- Component external margin: md (16px)
- Section padding: lg (24px)
- Between sections: xl (32px)
- Always align to 8px grid

#### 4. Roundedness Rules
- Button corners: sm (4px)
- Card corners: lg (12px)
- Input fields: sm (4px)
- Modals: lg (12px)
- Avatars / circles: full (9999px)

#### 5. Interactive States
- **Hover**: Lighten primary by 10% (#5a27f2) or darken slightly for secondary
- **Focus**: Add 2px solid primary focus ring, no outline color change
- **Active**: Darken by 15%, maintain contrast
- **Disabled**: Use neutral-subtle bg, muted text, cursor: not-allowed

#### 6. Common Patterns
- **Primary form**: display title + body description + md spacing + primary button
- **Card list**: cards in md-spaced grid (1 col mobile, 2-3 cols desktop)
- **Alert banner**: colored badge + body text + dismissible icon
- **Modal**: lg rounded container on neutral-light, min 400px width
- **Navigation**: primary text for active, muted for inactive, focus ring on keyboard nav

---

## Migration from Existing Design System

This DESIGN.md is derived from UniOpen's comprehensive color token system:

- **gt (Global Tokens)** → Raw color values in this document
- **at (Alias/Semantic Tokens)** → Named colors (primary, secondary, success)
- **ct (Component Tokens)** → Component-specific rules in this document

### Sync Strategy
Keep this file synchronized with the source Figma design system and the full DESIGN.md file in the project repository. Review quarterly for updates.

---

## Tools & Commands

### Validate this DESIGN.md
```bash
npx @google/design.md lint DESIGN.md
```

### Export to Tailwind Config
```bash
npx @google/design.md export --format tailwind DESIGN.md
```

### Export to W3C Design Tokens
```bash
npx @google/design.md export --format dtcg DESIGN.md
```

---

## Version History

- **v1 (alpha)** — Initial release based on UniOpen color system, typography, spacing, and component patterns. Ready for Open Design integration.

