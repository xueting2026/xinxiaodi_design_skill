---
version: 1.1
name: 信小递司机端
description: 信小递司机端微信小程序设计系统，基于 Figma 设计稿整理，色彩体系对齐 Pangea Design，Token 分 primitive/semantic/component 三层，设计宽度 375px（iPhone X）。
colors:
  # === 色彩体系对齐 Pangea：色板 1→10 由浅到深，主色/常规态 = 6 级 ===
  # 品牌色 Primary（青绿）
  primary-1: "#E8FFFB"   # 浅色/白色悬浮
  primary-2: "#ADEEE4"   # 文字禁用
  primary-3: "#79DDD1"   # 一般禁用
  primary-4: "#4ACCC1"   # 特殊场景
  primary-5: "#22BBB3"   # 悬浮 (brand-hover)
  primary-6: "#00AAA6"   # 常规主色 (brand)
  primary-7: "#009093"   # 点击 (brand-active)
  primary-8: "#00757B"
  primary-9: "#005C64"
  primary-10: "#00444D"
  # 中性灰 Gray（文字/线条/填充来源）
  gray-1: "#F7F8FA"
  gray-2: "#F2F3F5"
  gray-3: "#E5E6EB"
  gray-4: "#C9CDD4"
  gray-5: "#A9AEB8"
  gray-6: "#86909C"
  gray-7: "#6B7785"
  gray-8: "#4E5969"
  gray-9: "#272E3B"
  gray-10: "#1D2129"
  # 语义文字 Text（对齐 Pangea color-text-1..4）——值全部取自中性灰 Gray，不单独维护 hex
  color-text-1: "{gray-10}"  # #1D2129 主文字/标题（旧 text-3）
  color-text-2: "{gray-8}"   # #4E5969 次强调正文
  color-text-3: "{gray-6}"   # #86909C 辅助/次要信息（旧 text-2 近似）
  color-text-4: "{gray-4}"   # #C9CDD4 占位符/置灰（旧 text-1 近似）
  # 语义线条 Border（对齐 Pangea color-border-1..4）——取自中性灰 Gray
  color-border-1: "{gray-2}"  # #F2F3F5 浅
  color-border-2: "{gray-3}"  # #E5E6EB 一般（旧 border-1）
  color-border-3: "{gray-4}"  # #C9CDD4 深（旧 border-2 近似）
  color-border-4: "{gray-6}"  # #86909C 重/按钮描边
  # 语义填充 Fill（对齐 Pangea color-fill-1..5）——white 为纯白，其余取自中性灰 Gray
  color-fill-white: "#FFFFFF"  # 卡片/输入框表面（非灰阶）
  color-fill-1: "{gray-1}"     # #F7F8FA 浅/禁用底
  color-fill-2: "{gray-2}"     # #F2F3F5 页面背景/卡片内嵌区（旧 bg-1）
  color-fill-3: "{gray-3}"     # #E5E6EB 预改约底部等特定区域（旧 bg-2）
  color-fill-4: "{gray-4}"     # #C9CDD4 清除按钮底
  color-fill-5: "{gray-8}"     # #4E5969 强调/图标
  # 功能状态色 Functional（default=6 级，bg=1 级）
  success: "#00B42A"     # 成功；success-bg #E8FFEA
  warning: "#FF7D00"     # 警告；warning-bg #FFF7E8
  danger: "#F53F3F"      # 危险/错误/必传（旧 danger-1 #EE0A24）；danger-bg #FFECE8
  info: "#165DFF"        # 信息
  # 业务标签色 Subcolor（承载语义，不可替换）
  blue: "#165DFF"        # 蓝色标签（提货点/运单状态）
  orange: "#FF7D00"      # 橙色标签（2C/收货点）、约定时间
  purple: "#722ED1"      # 紫色标签（电商补货）
  # 旧命名保留为兼容别名（指向新值）：vi-1→primary-1, vi-2→primary-6, vi-3→primary-7,
  # text-3→color-text-1, text-2→color-text-3, text-1→color-text-4,
  # border-1→color-border-2, bg-1→color-fill-2, bg-2→color-fill-3, danger-1→danger
  # 中性色 Neutral
  gray-4: "#C9CDD4"     # 清除按钮背景、禁用文字
  gray-5: "#C8C9CC"     # checkbox/radio 未选中边框
typography:
  page-title:
    fontFamily: PingFang SC
    fontSize: 16px
    fontWeight: 500
    lineHeight: 22px
  card-title:
    fontFamily: PingFang SC
    fontSize: 14px
    fontWeight: 600
    lineHeight: 20px
  body-emphasis:
    fontFamily: PingFang SC
    fontSize: 14px
    fontWeight: 500
    lineHeight: 20px
  body:
    fontFamily: PingFang SC
    fontSize: 12px
    fontWeight: 500
    lineHeight: 18px
  secondary:
    fontFamily: PingFang SC
    fontSize: 12px
    fontWeight: 400
    lineHeight: 18px
  caption:
    fontFamily: PingFang SC
    fontSize: 10px
    fontWeight: 400
    lineHeight: 14px
  button-large:
    fontFamily: PingFang SC
    fontSize: 16px
    fontWeight: 400
    lineHeight: 22px
    color: "{colors.color-text-1}(深底反白时为白)"
  button-medium:
    fontFamily: PingFang SC
    fontSize: 14px
    fontWeight: 400
    lineHeight: 20px
  button-small:
    fontFamily: PingFang SC
    fontSize: 14px
    fontWeight: 400
    lineHeight: 20px
  tag:
    fontFamily: PingFang SC
    fontSize: 10px
    fontWeight: 400
    lineHeight: 14px
  number:
    fontFamily: Nunito Sans
    fontSize: 14px
    fontWeight: 500
    lineHeight: 20px
    fontVariantNumeric: tabular-nums   # 等宽数字：运单号/重量/时间竖排对齐
spacing:
  # 基础刻度（4px 栅格，补齐 20/28/40/48）
  base: 4px
  1: 4px
  2: 8px
  3: 12px
  4: 16px
  5: 20px
  6: 24px
  7: 28px
  8: 32px
  10: 40px
  12: 48px
  # 语义间距（每个用途对应唯一刻度，消除歧义）
  inset: { xs: 8px, sm: 12px, md: 16px, lg: 24px }   # 组件内边距
  stack: { xs: 4px, sm: 8px, md: 12px, lg: 16px, xl: 24px }  # 纵向堆叠
  inline: { xs: 4px, sm: 8px, md: 12px }             # 横向并排
  gap-list: 12px       # 卡片列表间距（唯一用途）
  gap-section: 24px    # 页面区块之间
  page-margin: 16px    # 页面左右边距（唯一用途）
rounded:
  # 基础刻度
  xs: 2px          # 标签 (radius-tag)
  sm: 4px          # 按钮、输入框、Tab、搜索框 (radius-control)
  md: 10px         # 卡片 (radius-card)
  lg: 12px         # 图标背景 (radius-icon-bg)
  dialog: 8px      # 弹窗 (radius-dialog)
  pill: 999px      # 真胶囊，与高度无关（旧值 58px 已废弃）
  full: 50%        # 头像、浮窗按钮 (radius-circle)
components:
  button-primary-large:
    backgroundColor: "{colors.primary-6}"
    textColor: "{colors.color-fill-white}"
    typography: "{typography.button-large}"
    rounded: "{rounded.sm}"
    height: 40px
    widthMode: block   # 默认整行 width:100%（旧 width:303px + padding:0 119px 已废弃）
    paddingX: 16px
  button-primary-large-hover:
    backgroundColor: "{colors.vi-3}"
    textColor: "{colors.white}"
    typography: "{typography.button-large}"
    rounded: "{rounded.sm}"
    height: 40px
  button-primary-large-disabled:
    backgroundColor: "{colors.vi-2}"
    textColor: "#FFFFFF opacity 40%"
    typography: "{typography.button-large}"
    rounded: "{rounded.sm}"
    height: 40px
  button-light-large:
    backgroundColor: "rgba(0,170,166,0.1)"
    textColor: "{colors.vi-2}"
    typography: "{typography.button-large}"
    rounded: "{rounded.sm}"
    height: 40px
  button-clear-large:
    backgroundColor: "{colors.bg-2}"
    textColor: "{colors.text-3}"
    typography: "{typography.button-large}"
    rounded: "{rounded.sm}"
    height: 40px
  button-primary-small:
    backgroundColor: "{colors.vi-2}"
    textColor: "{colors.white}"
    typography: "{typography.button-small}"
    rounded: "{rounded.sm}"
    padding: "6px 8px"
    height: 32px
  button-light-small:
    backgroundColor: "{colors.vi-1}"
    textColor: "{colors.vi-2}"
    typography: "{typography.button-small}"
    rounded: "{rounded.sm}"
    padding: "6px 8px"
    height: 32px
  button-text-small:
    backgroundColor: transparent
    textColor: "{colors.vi-2}"
    typography: "{typography.button-small}"
    rounded: "{rounded.sm}"
    padding: "6px 8px"
    height: 32px
  input-register:
    backgroundColor: "{colors.color-fill-white}"
    textColor: "{colors.color-text-1}"
    placeholderColor: "{colors.color-text-4}"
    typography: "{typography.body-emphasis}"
    rounded: "{rounded.sm}"
    padding: "0 12px"
    height: 48px
    widthMode: block   # width:100%（旧 width:303px 已废弃）
    borderColor: "{colors.color-border-2}"
  searchbox:
    backgroundColor: "{colors.white}"
    textColor: "{colors.text-3}"
    placeholderColor: "{colors.text-1}"
    typography: "{typography.button-small}"
    rounded: "{rounded.sm}"
    padding: "0 8px 0 4px"
    height: 36px
  card:
    backgroundColor: "{colors.color-fill-white}"
    rounded: "{rounded.md}"
    shadow: "0px 4px 12px rgba(0,0,0,0.05)"
    padding: "12px 16px"
    widthMode: block       # width:100% + max-width:343px（旧 width:343px 已废弃）
    maxWidth: 343px
  tag-status:
    borderWidth: 1px
    rounded: "{rounded.xs}"
    typography: "{typography.tag}"
    height: 20px
    padding: "0 4px"
  checkbox:
    size: 16px
    rounded: 2px
    borderColor: "{colors.gray-5}"
    checkedColor: "{colors.vi-2}"
    disabledBg: "{colors.bg-2}"
  radio:
    size: 16px
    rounded: 50%
    borderColor: "{colors.border-2}"
    borderWidth: 1.5px
    checkedColor: "{colors.vi-2}"
  tab:
    height: 28px
    rounded: 4px
    gap: 8px
    activeBackground: "{colors.vi-2}"
    activeTextColor: "{colors.white}"
    inactiveBackground: transparent
    inactiveTextColor: "{colors.text-2}"
  floating-button:
    size: 60px
    rounded: 50%
    background: "linear-gradient(135deg, #00AAA6, #009B97)"
    shadow: "0px 4px 12px rgba(0,170,166,0.3)"
  floating-button-small:
    size: 40px
    rounded: 50%
    background: "linear-gradient(135deg, #00AAA6, #009B97)"
---

# 信小递司机端

## 概述

信小递是海信集团物流司机端微信小程序的设计系统。视觉风格以品牌绿 `#00AAA6` 为核心，搭配中性灰阶构建信息层次，服务于提货、派送、签收等物流场景。设计宽度 375px（iPhone X），字体统一使用 PingFang SC。整体风格简洁实用：卡片圆角、克制的色彩、清晰的信息层级，优先保证操作效率与可读性。

## 颜色

色彩体系对齐 Pangea Design：每个色系都是 **1→10 由浅到深的 10 级色板**，主色/常规态固定在第 6 级。Token 分三层，业务代码只用 semantic / 组件层，不直接写 primitive 或 hex。

**色板（primitive，第 1 层）**

- **品牌色 primary-1…10**：`primary-6 #00AAA6` 是品牌主色，`primary-5` 悬浮、`primary-7` 点击、`primary-1` 浅底。
- **中性灰 gray-1…10**、**危险 red**、**警告 orange**、**成功 green**、**信息 arcoblue（含蓝色标签）**、**紫色 purple** 各 10 级。

**语义层（semantic，第 2 层，按用途命名）**

- **文字** `color-text-1…4`：`1 #1D2129` 主文字 → `2 #4E5969` 次强调 → `3 #86909C` 辅助/次要 → `4 #C9CDD4` 占位/置灰。
- **线条** `color-border-1…4`：`1 #F2F3F5` 浅 → `2 #E5E6EB` 一般（分割线/输入框边框）→ `3 #C9CDD4` 深 → `4 #86909C` 重/描边。
- **填充** `color-fill-white/1…5`：白面 → `fill-2 #F2F3F5` 页面背景/卡片内嵌区 → `fill-3 #E5E6EB` 预改约底部等特定区域。
- **品牌交互** `brand`(默认) / `brand-hover` / `brand-active` / `brand-bg`(浅底) / `brand-bg-subtle`(半透明底)。
- **功能状态** `success #00B42A` / `warning #FF7D00` / `danger #F53F3F` / `info #165DFF`，各带 `-bg` 浅底。`danger` 用于错误文字与必传提醒。
- **业务标签** `blue #165DFF`（提货点/运单状态）、`orange #FF7D00`（2C/收货点/约定时间）、`purple #722ED1`（电商补货）——颜色承载业务含义，不可替换。

> 旧命名（`vi-1/2/3`、`text-1/2/3`、`border-1/2`、`bg-1/2`、`danger-1`）仍作为**兼容别名**保留，指向上述新值。新代码请优先使用语义命名，不要硬编码 hex。

## 排版

PingFang SC 为唯一字体家族。上文 `typography` token 携带 `fontFamily`、`fontSize`、`fontWeight` 与 `lineHeight`：

- `page-title`（16px/Medium）用于页面标题与导航栏标题。
- `card-title`（14px/Semibold）用于卡片标题行。
- `body-emphasis`（14px/Medium）用于正文中需要强调的信息。
- `body`（12px/Medium）用于一般正文内容。
- `secondary`（12px/Regular）用于辅助说明，搭配 `text-2` 色值。
- `caption`（10px/Regular）用于次要信息、时间、标签文字。
- `button-large`（16px/Regular）用于大按钮文字，`button-medium`（14px/Regular）用于中按钮，`button-small`（14px/Regular）用于小按钮与搜索框内文字。按钮文字统一 Regular(400)，深底时反白。
- `tag`（10px/Regular）用于标签组件。
- `number`（Nunito Sans / tabular-nums）用于运单号、重量、时间等数字，等宽让竖排数字对齐。对应工具类 `.text-number`。

`body` 与 `secondary` 覆盖大多数文字场景。字号来自原始刻度（10/12/13/14/16/18/20/24），字重仅 Regular(400)/Medium(500)/Semibold(600) 三档，不要在这些 token 之外自行设定字号或字重。

## 布局

间距遵循 4px 基础刻度，完整档位：4、8、12、16、20、24、28、32、40、48px（全部 4 的倍数）。为消除"一个数管多个用途"的歧义，间距分两层使用：

- **基础刻度**给出可用的像素值；
- **语义间距**把用途固定到唯一刻度：`inset`（组件内边距：xs 8 / sm 12 / md 16 / lg 24）、`stack`（纵向堆叠：4/8/12/16/24）、`inline`（横向并排：4/8/12）、`gap-list`=12（卡片列表间距，唯一用途）、`gap-section`=24（区块之间）、`page-margin`=16（页面左右边距，唯一用途）。

卡片内边距 12px（竖）/16px（横），页面左右边距 16px，卡片列表间距 12px。内容区域限定在 343px 宽度（375px 减去左右各 16px 边距）。

页面结构自上而下：
```
├── 状态栏 (44px, 系统)
├── 导航栏 (44px, 白色/渐变)
├── 内容区域
│   ├── 头部区域 (渐变背景)
│   ├── 功能卡片 (白色卡片, 圆角10px)
│   ├── 列表区域
│   │   ├── 筛选/搜索栏
│   │   ├── Tab切换
│   │   └── 卡片列表 (间距12px)
│   └── 空状态
└── 浮动按钮 (固定定位, 右下角)
```

### 状态栏 & 标题栏规则

状态栏和标题栏合为一组（`.demo-topbar` 容器），**仅用于 demo / 原型预览**还原真机顶部效果。开发时系统（小程序 / App）会自带顶部，无需实现——可通过 `.demo-topbar { display:none }` 或加 `.demo-topbar--hidden` 一次性隐藏，也可直接删除整个容器。

- **状态栏**：demo 中始终存在。配色见下方《背景与字色解耦》。
- **标题栏**：是否显示由当前页面决定，显示时由三部分组成：
  - **返回按钮**：仅二级及以下页面有，点击返回上一级；一级页面（首页、登录页）无返回按钮。
  - **标题**：始终存在，按当前页面命名（如「首页」「待到库」）；登录页标题为「信小递」。**标题始终相对整栏（375px）水平居中，不管左右两侧按钮功能增减都保持居中**（绝对定位居中实现）。
  - **胶囊按钮**：小程序平台始终提供，固定在右侧，距右 6px，宽度自适应（87×32）。胶囊图标跟随字色：深色字用 `bar_navbar_black.svg`，白色字用 `bar_navbar_transparent.svg`。

#### 背景与字色解耦（选字色看底色亮度，不看"是不是渐变头部"）

状态栏/标题栏有**两个独立维度**：**背景**（白底 or 透明）与**字色**（深色 or 白色）。旧快捷类把两者捆在一起，只覆盖了 2 种组合，容易在"浅色渐变头部"这种场景选错字色。现在拆开：

- **背景快捷类**（含默认字色）：
  - `statusbar--dark` / `titlebar--solid` = 白底 + 深色字（常规白底内页）。
  - `statusbar--light` / `titlebar--transparent` = 透明背景 + 白色字（深色/饱和品牌绿渐变头部，如首页）。
- **字色修饰符**（独立覆盖字色，叠加到任意背景上）：`--ink-dark`（深色字）/ `--ink-light`（白色字）。用于补齐快捷类没覆盖的组合。

**判定规则（关键）**：字色不由"是否渐变头部"决定，而由**状态栏正后方那块底色的亮度**决定——取该底色算 WCAG 相对亮度，或比较深色字（`#1D2129`）与白字对它的对比度，取对比度高的那个：

- **浅底**（白底 / 浅色渐变，如异常提报页 `#D6F5F3`）→ **深色字**：透明背景透出浅渐变时写 `statusbar--light statusbar--ink-dark` + `titlebar--transparent titlebar--ink-dark`，系统图标用 `bar_status_black.svg`、胶囊用 `bar_navbar_black.svg`。
- **深底**（饱和品牌绿渐变 / 深色，如首页）→ **白色字**：`statusbar--light` + `titlebar--transparent`（白字为默认，无需再加 ink），系统图标用 `bar_status_white.svg`、胶囊用 `bar_navbar_transparent.svg`。
- 底色若为**照片/复杂图**，无法可靠判定亮度 → 加半透明蒙层保证对比度，或询问确认，不硬猜。

> 四种组合对照与配套图标见 `components/statusbar-titlebar.json` 的 `inkModifiers` 字段。

### Demo 手机框：固定定位浮层收敛（375px）

原型 demo 里页面被约束在 375px 手机框（`#app { width:375px; margin:0 auto; position:relative; overflow:hidden }`），但设计系统中用 `position:fixed` 的浮层（弹窗蒙层 `.dialog-overlay`、浮动按钮 `.fab`）是相对**视口**定位的，在宽屏浏览器里会溢出到手机框之外（蒙层铺满整屏、浮动按钮贴在浏览器右下角）。

规则：demo/原型里，凡 `position:fixed` 的浮层都要收敛到手机框内——在 `#app`（已是 `position:relative`）作用域下把它们改成 `position:absolute`，让其定位相对手机框而非视口：

```css
#app .dialog-overlay { position: absolute; }
#app .fab { position: absolute; }
```

自定义浮层（吐司、照片查看器等）同理，直接用 `position:absolute; inset:0`（相对 `#app`），不要用 `fixed`。此规则仅针对 demo 预览；交付到小程序/App 时顶部与浮层由系统或真实容器承载，无需此覆盖。

## 形状

圆角保持克制，并提供组件级语义 token：`radius-tag 2px`（标签）、`radius-control 4px`（按钮/输入框/Tab/搜索框）、`radius-card 10px`（卡片）、`radius-icon-bg 12px`（图标背景）、`radius-dialog 8px`（弹窗）、`radius-circle 50%`（头像/浮窗按钮）、`radius-pill 999px`（展开/收起等胶囊，真胶囊、与高度无关——旧值 58px 已废弃）。一个视图内保持统一的圆角家族，不混用。

## 层级与深度

层级通过背景色区分：`bg-1` 灰底页面 → `white` 卡片表面 → `bg-1` 卡片内嵌内容区。阴影仅用于卡片容器（`0px 4px 12px rgba(0,0,0,0.05)`）和浮窗弹出层（`0 4px 16px rgba(0,0,0,0.12)`）。浮动按钮使用品牌色阴影（`0px 4px 12px rgba(0,170,166,0.3)`）。

## 组件

上文 `components` token 给出各元素的即用值：

- **大按钮（button-primary-large）**：实心品牌色填充，白色文字，高 40px，**默认整行（width:100%，`.btn--lg`）**，用于页面级主操作（登录、提交）。旧的 `width:303px` + `padding:0 119px` 硬编码已废弃，改为左右内边距 16px + 文字居中，宽度随内容区自适应。hover 切换为 `brand-active`，禁用态文字降 40% 透明度。
- **中按钮（button-medium，`.btn--md`）**：高 36px，内容自适应宽度（`width:auto`，左右内边距 12px），介于页面级大按钮与卡片内小按钮之间；需要整行时加 `.btn--block`。
- **浅色大按钮（button-light-large）**：`rgba(0,170,166,0.1)` 半透明填充，`vi-2` 文字，用于次要操作。
- **清除大按钮（button-clear-large）**：`bg-2` 填充，`text-3` 文字，用于取消/重置。
- **小按钮（button-primary-small）**：32px 高，`vi-2` 填充，用于卡片内操作（扫码到库、分单、审核）。
- **浅色小按钮（button-light-small）**：`vi-1` 填充，`vi-2` 文字。
- **文字小按钮（button-text-small）**：透明填充，`vi-2` 文字，无底色，用于低强调操作（更多）。
- **输入框（input-register）**：白色填充，`border-1` 边框，48px 高，用于注册/登录页。
- **文本域（textarea）**：多行输入，与输入框同族（`border-1` 边框、4px 圆角、focus 品牌色 + 外发光）。`.textarea-field` 包裹 `.textarea` + `.textarea-counter`（右下角字数计数器 `N/max`，12px `text-1`，随输入更新，`maxlength` 达上限停止输入）；`resize:none`。计数交互由 `XUI.initTextarea('.textarea-field')`（或 `XUI.initAll`）自动挂载。用于备注、异常说明等多行录入。
- **搜索框（searchbox）**：白色填充，36px 高，含搜索图标 + 输入区 + 查询按钮（28px 高，`vi-2` 背景）。可附加筛选下拉（12px `vi-2` 文字 + 分割线）或排序/筛选图标按钮（36×36px）。**拍照获取变体**：省略左侧搜索图标，查询按钮文案改为「拍照获取」，placeholder「请输入柜号或拍照获取」；点击按钮唤起相机拍照 → OCR 识别柜号 → 回填输入框（复用 `.searchbox`/`.searchbox__query`，无需新增 class）。
- **卡片（card）**：白色填充，10px 圆角，343px 宽，低阴影。**运单卡片 = `.card` 容器 + `.card__*` 原子类拼装**（值全部取自 tokens，定义见 `ui.css` 第 8 节，勿在示例/原型里写私有卡片类）。按三层结构拼装：
  - 列表容器：`.card-list`（提供 12px 卡片间距）
  - 提货/收货信息（地点头）：`.card__location` / `.card__location-row` / `.card__addr` / `.card__warehouse` / `.card__cargo`
  - 全宽分割线：`.card__divider.card__divider--full`
  - 运单信息（调度单分组）：`.card__dispatch` / `.card__dispatch-row` / `.card__dispatch-plate` / `.card__dispatch-time`
  - 展开/收起：`.card__toggle` / `.card__toggle-pill`（展开态 `.card__toggle-pill--open`）
  - 订单信息（展开区）：`.card__orders`（`.card__orders--visible` 显隐）/ `.card__order` / `.card__order-top` / `.card__order-sap` / `.card__order-body` / `.card__field`（`.card__field-label` + `.card__field-value`）/ `.card__product` / `.card__order-footer` / `.card__order-contact` / `.card__order-appoint`
  - 底部按钮区：`.card__footer.card__footer--between` / `.card__stats` / `.card__actions`
- **拖车业务卡片**：用于拖车业务各页面（提柜、返柜等），**三层结构与运单卡片一致，复用同一套 `.card__*` 原子类**：场站(地点头) → 调度单(调度单号+下达时间) → 运单小卡片(运单号 + 运单信息字段 + 操作按钮)。一个大卡片可含多个调度单，每个调度单下可挂多个运单小卡片，每个运单小卡片底部各带一个操作按钮。**注意调度单号（`D22110100291`）与运单号（`HECPX…`）是不同层级的不同数据。** 容器加 **`.card--trailer`** 修饰以收敛拖车专属间距。
  - 场站信息（地点头）：`.card__location` / `.card__location-row`（`.tag.tag--orange` 场景标签 + `.card__addr.card__addr--wrap` 地址，标签文案随页面切换：提柜页=「提柜点」、返柜页=「返柜点」）/ `.card__warehouse`（【编码】+名称，如 `【A001】xx场站`）
  - 全宽分割线：`.card__divider.card__divider--full`（场站头与调度单之间 / 多个调度单组之间）
  - 调度单头（调度单号+下达时间）：`.card__dispatch` / `.card__dispatch-row` / `.card__dispatch-plate`（调度单号）/ `.card__dispatch-time`（下达时间）。**调度单号 D… 行上下间距 8px**（`.card--trailer .card__dispatch` padding `8px 16px`）。
  - 运单小卡片：包裹层 `.card__waybill`（左右 16px、底部 8px），内含 `.card__order`（绿底头 `.card__order-top`：`.card__waybill-label`「运单号」12px Medium `color-text-1`/#1D2129 + `.card__order-sap` 值；**绿底头下方带 0.5px `color-border-3`/#C9CDD4 分割线** / 灰底身 `.card__order-body`）
  - 运单信息字段网格（置于灰底身内）：`.card__grid`，短字段（提单号/车牌号/柜子类型/是否多地拼货）一排 2 个各占 50%（`.card__grid-item`），长字段（要求装货时间/首个装货点）独占一行 100%（`.card__grid-item--full`），每项 `.card__grid-label` + `.card__grid-value`
  - 运单小卡片底部操作按钮：`.card__waybill-actions` + `.btn.btn--sm.btn--primary`（如「提柜」，每个运单小卡片各 1 个）。**按钮距上间距 8px**（`.card--trailer .card__order` 取消下边距 + `.card__waybill-actions` padding-top 8px）。
  - **字段占位宽度规则**：长字段独占一行 100%（`.card__grid-item--full`，完整显示、可换行、不省略）；其余为短字段一排 2 个各 50%（`.card__grid-item`，值超出 50% 单行省略 `...`）。**长字段集合 = 要求装货时间 / 首个装货点 / 柜号 / 预约入园时间 / 月台信息。** 后续新增字段时，**必须先询问该字段是长字段还是短字段**再决定占位宽度，不得臆断。
  - **应用场景**：拖车业务 8 个列表页——提柜 / 入园 / 落柜 / 提重柜 / 离园 / 过磅 / 返重柜 / 改约。每个列表页 = 状态栏+标题栏 + 定位栏 + **有筛选的搜索框** + 拖车业务卡片列表。逐页字段、场站标签与按钮见 `card.json → 拖车业务卡片结构.pageFieldConfig`。下表为速览（(长)=长字段占 100%）：

| 列表页 | 场站标签 | 编码示例 | 运单信息字段 | 按钮 |
|--------|----------|----------|--------------|------|
| 提柜 | 提柜点 | A001 | 提单号、车牌号、柜子类型、是否多地拼货、要求装货时间(长)、首个装货点(长) | 提柜 |
| 入园 | 装货点 | H1532 | 车牌号、订舱号、柜子类型、柜号(长)、是否多地拼货、预约入园时间(长)、装货点顺序、要求装货时间(长) | 入园登记 |
| 落柜 | 装货点 | H1532 | 车牌号、订舱号、柜子类型、柜号(长)、是否多地拼货、要求装货时间(长)、装货点顺序、月台信息(长) | 落柜登记 |
| 提重柜 | 装货点 | H1532 | 车牌号、订舱号、柜子类型、柜号(长)、是否多地拼货、要求装货时间(长)、装货点顺序、月台信息(长) | 提重柜登记 |
| 离园 | 装货点 | H1532 | 车牌号、订舱号、柜子类型、柜号(长)、是否多地拼货、装货进度、装货点顺序、月台信息(长) | 离园登记 |
| 过磅 | 无场站头 | — | 车牌号、订舱号、柜子类型、柜号(长)、是否多地拼货 | 过磅登记 |
| 返重柜 | 返柜点 | A001 | 提单号、车牌号、订舱号、柜子类型、柜号(长)、货品分类、货品件数、货品重量、货品体积 | 返重柜 |
| 改约 | 装货点 | H1532 | 车牌号、订舱号、柜子类型、柜号(长)、是否多地拼货、预约入园时间(长)、装货点顺序、要求装货时间(长) | 改约 |

  - 注：**过磅列表页的卡片无场站头**，直接从调度单信息（调度单号+下达时间）开始。
- **物流信息卡片**：用于**订单管理**列表页（管理端）。343px 宽、10px 圆角、低阴影的 `.card`。结构：顶部订单号行（直发标签 + 订单号 + 状态如「已锁」，下带 0.5px 分割线）→ 信息区（分销商名称 16px Semibold + 整单甩单/2C 标签行 + 路线「起 → 止」行）→ 灰底信息块（`color-fill-2`：下单/统仓/组织/件重方/承运商等键值对，值超出单行省略）→ 全宽分割线 → 底部按钮组（`.card__footer.card__footer--between` + `.card__actions`，如 更多/改转运/取消分单/分单/审核）。复用 `.card__*` 原子类，勿写私有卡片类。
- **签收管理卡片**：用于**待签收**下的整单签收 / 整单拒收 / 回单上传等操作。结构：运单号绿底头（`.card__order-top`：运单号 + SAP 单号 + 2C 标签，下带 0.5px 分割线）→ 告警条（可选，`#FDE7E9` 底 + `danger-1` 红字，如「用户已申请退货退款，送前务必电联！」）→ 签单/回单图片上传区（灰底 `color-fill-2`，标题如「上传该订单的签单图片！」+ `uploader` 组件 + 红字必填提示「签单照片必传！」）→ 展开区（拒收原因选择行（点击唤起 `sheet` 动作面板）+ 订单详情：订单号/收货地址/品类型号数量/收货联系人电话）→ 展开/收起 pill。**图片上传用 `uploader` 组件、拒收原因选择用 `sheet` 动作面板，勿自造。**
- **标签（tag-status）**：1px 边框，2px 圆角，20px 高。颜色按业务含义：蓝色（运单状态）、橙色（2C）、紫色（电商补货）。
- **多选框（checkbox）**：16px 方形，2px 圆角。未选中 `gray-5` 边框，选中 `vi-2` 填充+白色勾，禁用 `bg-2` 填充。半选态 `vi-2` 填充+白色横线。
- **单选框（radio）**：16px 圆形，1.5px `border-2` 边框。选中 `vi-2` 填充+白色勾。
- **Tab 切换**：28px 高，4px 圆角，选中态 `vi-2` 背景白色文字，未选中透明背景 `text-2` 文字。
- **浮动按钮**：60px 圆形，品牌绿渐变，品牌色阴影。小号 40px。
- **图片上传（uploader）**：拍照/上传图片组件，置于灰底（`bg-1`）内嵌区。字段容器 `.uploader-field`（空态：`.uploader` 添加按钮 + `.uploader__hint` 红字提示并排；有图态加 `.uploader-field--filled`：隐藏提示、`.uploader` 单行不换行且横向滚动）。添加按钮与缩略图统一 **72×72**、间距 8px，每个上传区最多 **9 张**。
  - 添加按钮 `.uploader__add`：白底 + `1px dashed` 边框 + 4px 圆角，竖向居中「图标 + 文案」；图标用 `assets/icons/pic_gray_24px.svg`，文案 10px `text-2`：空态「拍照/上传」，有图后「还能传N张」（N=9−已传数）。
  - 缩略图：72×72 单元格内含 64×64 图片（`.uploader__thumb-img`，radius 4px、顶部偏移 8px），右上角删除按钮 `.uploader__del`（20px，图标 `assets/icons/pic_close.svg`：深色半透明圆 + 白描边 + ×）。
  - 提示 `.uploader__hint`：必填/上限说明，12px Medium `danger-1`（#EE0A24），**仅空态显示**。
  - 交互：**空态显示红字提示**；点击添加 → 唤起拍照/相册 → 上传后**红字消失、切换为有图态**并追加缩略图、更新「还能传N张」；**缩略图超出一行时整行左右滑动查看**；满 9 张隐藏添加按钮；点删除移除并回填数量（删至 0 张恢复空态红字提示）。
- **弹出面板（sheet）**：表单级底部上滑面板，用于选择/时间等录入，取代临时下拉。遮罩 `#000000` 60% 且限页面宽度；面板白底、顶部 16px 圆角、**最高 536px 超出内容区滚动**；头部固定「左取消 / 中标题 / 右确认」（`.sheet__header` + `.sheet__cancel`/`.sheet__title`/`.sheet__confirm`）。三种内容变体：
  - **动作面板（列表选择）**：`.sheet__body` 放 `.sheet__option` 列表，单选高亮 `.sheet__option--selected`（vi-2）。
  - **选择器（单列滚轮）**：`.sheet__wheel`（单列 `.sheet__wheel-col`，中间 `.sheet__wheel-band` 选中带，居中项 `.sheet__wheel-item--active`）。
  - **时间选择（多列滚轮）**：`.sheet__wheel` 多列（如 时/分）。
  交互：`XUI.openSheet('#id')` / `XUI.closeSheet('#id')`（取消/确认/点遮罩/Esc 关闭）；列表用 `XUI.initSheetOptions`、滚轮用 `XUI.initWheel`（值存 `col.dataset.value`），均由 `XUI.initAll` 自动挂载。表单里点击选择/时间控件（如 `.dialog__field-select`）→ 打开对应面板。`#app` 手机框内加 `#app .sheet-overlay{position:absolute}` 收敛。**滚轮项字号 16px**（`.sheet__wheel-item`）。
  - **选型**：选项少（约 ≤7）且带描述文字 → 动作面板列表；值多/有序/纯枚举、需快速滚动 → 选择器滚轮；时间(时/分)或多维联动 → 时间选择。
  - **使用场景**：
    - 动作面板（列表选择）：拖车异常类型选择、拒收原因选择、筛选维度/单号类型（选项少）、卡片「更多操作」动作列表。
    - 选择器（单列滚轮）：柜子类型（20GP/40HQ…）、装货点顺序/档位/数量、单号类型（值多时）。
    - 时间选择（多列滚轮）：预约/改约时间段（起—止 时:分）、要求装货时间/预约入园时间、过磅/操作时间。
- **菜单列表项（menu-item）**：通用导航页（功能选择页 Hub）的纵向入口行。列表容器 `.menu-list`（`flex` 列、行间距 12px、padding `16px 16px 0`）；行 `.menu-item`（白底、10px 圆角、padding 16px → 行高 56px、`flex` 两端对齐），左侧 `.menu-item__left`（`.menu-item__icon` 24px 业务图标 + `.menu-item__label` 14px Semibold `color-text-1`），右侧 `.menu-item__arrow`（16px，固定 `assets/icons/select/right_line_black_16px.svg`）。点击整行跳转对应功能页。**【适用范围】仅用于通用导航页（Hub）的列表项**，不用于卡片内部行、Tab 内容区、表单字段行、列表页业务卡片、设置项开关行等（这些场景用对应的卡片/表单/选择器组件，不得借用 menu-item）。

## 按钮组规范

卡片底部按钮区域遵循以下规则：

- 有「x单x件」统计文字时：右侧操作按钮≤3个，超出则在最前显示「更多」文字按钮。
- 无统计文字时：右侧操作按钮≤5个，超出则显示「更多」文字按钮。
- 「更多」点击弹出浮窗（白色，8px 圆角，`0 4px 16px rgba(0,0,0,0.12)` 阴影）。
- 按钮间距 8px，统一使用 `button-primary-small` 样式。

## 图标

图标按尺寸分层，SVG 矢量格式，支持多色变体：

- **48×48px 金刚区图标**：用于首页功能入口网格。含渐变背景+阴影+内容图形。**司机端 13 个**（待到库、待提货、待打卡、待派送、待运抵、待签收、回单上传、送货交接、历史记录、服务反馈/仓库服务反馈中心、拖车业务、异常提报、待办中心）。**管理端金刚区（7 个）见 `Design-admin.md` §3.0**。⚠️「回单上传」「拖车业务」两端同名，「待签收↔签收管理」「异常提报↔超期预警」两端同域——用户未说端时按 SKILL.md 闸门 0 消歧，不得默认。
- **24×24px 通用图标**：search、close、position、phonecall、navigation、tiaoma、pic、password_hide/show 等。颜色变体 gray/green。
- **20×20px 工具图标**：sort、screen、time、new、zuzhi。白色版本用于深色背景（搜索栏图标通过 CSS filter 着色为 `vi-2`）。
- **16×16px 辅助图标**：position、tiaoma、search、close、phonecall、copy、people、list 等。颜色变体 green/gray/white/black。
- **12×12px select 箭头**：方向 down/up/left/right × 样式 line/surface × 颜色 green/gray/black/white。

图标命名规则：`{功能}_{颜色}_{尺寸}px.svg`，方向箭头附加方向前缀。

## 分割线

0.5px 分割线，颜色 `border-1`，支持四种对齐方式：

- **Full Width**：满宽无缩进。
- **Center**：两端各缩进 16px。
- **Left**：左侧缩进 16px。
- **带展开收起**：中间显示文字（10px `text-2`）+ 方向箭头。

## 导航组件

- **定位栏**：48px 高，左侧绿色 pin 图标 + 地址文字 + 右侧筛选按钮。6 种变体（地址行数 × 选中状态）。
- **扫码接单入口**：48px 高，渐变背景 `#F4FFFD→#FFF`，圆形 icon + 操作文字 + 右箭头。
- **展开收起**：62×26px，pill 形状（bg `bg-1`，border `border-1`，圆角 58px），文字 + 箭头图标。

## 列表页构成规范

各业务列表页的组件构成，所有组件均引用组件库中的标准组件：

| 页面 | 组件构成（从上到下） |
|------|---------------------|
| 待到库 | 状态栏+标题栏 → 定位组件 → 扫码接单入口 → 搜索框（有筛选） → 运单卡片 |
| 待提货 | 状态栏+标题栏 → 定位组件 → Tab 切换（待提货/待发运） → 运单卡片 |
| 在途打卡 | 状态栏+标题栏 → 定位组件 → Tab 切换（全部/已超时/已到达未发出） → 运单卡片 |
| 待派送 | 状态栏+标题栏 → 定位组件 → 运单卡片 |
| 待运抵 | 状态栏+标题栏 → 定位组件 → 搜索框（有筛选） → 运单卡片 |
| 待签收 | 状态栏+标题栏 → 定位组件 → 搜索框（有筛选） → 运单卡片 |
| 待办中心 | 状态栏+标题栏 → 扫码接单 → 搜索框（有筛选） → Tab 切换 → 运单卡片 |

**组件引用说明：**
- **状态栏+标题栏** → 系统状态栏 (44px) + 导航栏 (44px, 返回箭头 + 标题 + 小程序胶囊)
- **定位组件** → 定位栏 (48px, bg `bg-1`, 绿色 pin + 地址 + 筛选按钮)
- **扫码接单入口** → 扫码接单组件 (48px, 渐变背景, 圆形 icon + 操作文字 + 右箭头)
- **搜索框（有筛选）** → searchbox 组件 (36px) + 筛选下拉
- **Tab 切换** → tab 组件 (28px 高, 圆角 4px, gap 8px)
- **运单卡片** → card 组件（详见组件 token）

**卡片组件选型**（详见「卡片与功能模块对应关系」）：上表这些列表页（待到库、待提货、待打卡、待派送、待运抵、待签收、待办中心）均用**运单卡片**排版；**拖车业务**的全部列表页用**拖车业务卡片**；**订单管理**列表页用**物流信息卡片**；**待签收**下的整单签收 / 整单拒收 / 回单上传用**签收管理卡片**。

## Logo

- **信小递司机端 Logo（254×130px）**：紧凑版，含图标+文字。渐变色 `#57E8DF→#00AAA6` + 点缀色 `#FF5F00`。适用于启动页、登录页。
- **信小递司机端 Logo 横版（800×200px）**：完整横版，适用于品牌展示、文档头部。

## 页面类型与使用场景

信小递司机端按业务流程，页面分为以下六种 Canonical Layout（标准页型）。每种页型有明确的组件构成与适用场景，选型时先判断"用户在这一步要完成什么任务"。

### 登录页（Auth）

**场景**：用户首次使用或登录态过期时进入。

**结构**：居中布局，品牌 Logo + 输入区（手机号、验证码/密码）+ 主操作按钮。

**组件**：Logo（254×130px）、input-register（48px）、button-primary-large（40px）。

**判据**：需要身份认证时使用。不承载任何业务信息。

### 首页（Home / Dashboard）

**场景**：司机登录后的主入口，概览当前待办任务，快速进入各业务模块。

**结构**：
- 头部渐变区域（品牌氛围 + 用户信息）
- 消息提醒条（有待处理任务时显示，如"有3个柜子已完成装柜，请点击查看"）
- 扫码接单入口（48px，渐变背景，圆形 icon + 文字 + 右箭头）
- 金刚区（48×48px 图标网格，司机端 13 个功能入口：待到库、待提货、待打卡、待派送、待运抵、待签收、回单上传、送货交接、历史记录、服务反馈、拖车业务、异常提报、待办中心；管理端金刚区见 `Design-admin.md`）
- 待办任务快捷区（角标汇总各业务待办数量）——**固定模块，详见《待办任务区固定不动》**
- 浮动按钮（扫码/待办中心，右下角固定定位）

**判据**：用户需要"一眼看到全局状态"并"快速跳转到具体任务"时使用。信小递仅有一个首页。

### 搜索页（Search，**司机端 / 管理端共用页型**）

**场景**：在列表页点击搜索框进入的专用即时搜索页（组件·token·成品两端完全共用同一份 `examples/demo-search.html`，仅实例内容不同）。

**结构**：绿色头部（状态栏白字 + 返回 + 标题「搜索」+ 小程序胶囊）内嵌**白色即时搜索框**（放大镜 `search_gray_16px` + 输入框 + 清除× `close_gray_full_16px`，**无查询按钮**，输入即出结果）→ 正文按输入切换三态。

**四个状态**：
- **默认**：搜索框空（placeholder「请输入收货方编码/名」），正文居中灰字「未找到符合条件的单据」。
- **无结果**：有输入但无匹配 → 同上空状态 + 出现清除×。
- **结果·2 行**：搜索框下右对齐「收货方数据：共N条」+ 列表项两行（编号行 + 地址行单行省略），命中词高亮。
- **结果·1 行**：列表项单行（名称），命中词高亮，可含一条浅绿选中态 `#E8FFFB`。

**规则**：命中关键词高亮用**品牌色 `#00AAA6`**；空状态只用灰字无插画；列表项间 0.5px 分割线；列表页搜索框设 `readonly` + 点击跳本页（「点击搜索框 → 搜索页」的假搜索栏模式）。

### 功能选择页（Function Hub）

**场景**：某业务模块下有多个子功能时，作为二级入口集合。例如拖车业务包含派车、过磅、提柜、落柜、入园、离园、提重柜、返重柜、换车接单、改约、业务监控、异常提报 12 个子功能（图标按中文拼音命名，见 `assets/icons/tuoche/`）。

**结构**：
- 标题栏（返回箭头 + 标题 + 小程序胶囊）
- 当前位置（定位组件）
- 功能球网格（48×48px 图标 + 文字 + 角标）

**判据**：子功能≥3个且各自独立时使用。若子功能≤2个，直接放在首页金刚区或用 Tab 切换。

**参考**：`examples/demo-trailer.html`（拖车业务功能选择页成品，12 个子功能球）。

### 列表页（List）

**场景**：展示同类任务的集合，支持筛选、搜索、批量操作。是信小递最核心的页型——待到库、待提货、在途打卡、待派送、待运抵、待签收、待办中心、提柜列表、入园列表、落柜列表、提重柜列表、离园列表、过磅列表、返重柜列表、改约列表均属于此类。

**结构**（从上到下）：
- 状态栏 + 标题栏
- 定位组件（可选，有地理筛选需求时显示）
- 扫码接单入口（可选，仅待到库/待办中心使用）
- 搜索框（36px，可附加筛选下拉/排序/筛选图标）
- Tab 切换（可选，同类任务有多种状态分组时使用）
- 运单卡片列表（card 组件，间距 12px，支持展开/收起）
- 浮动按钮（可选）

**判据**：用户需要"浏览多条同类数据并选择/操作其中某条"时使用。列表页的数据通常按三层结构组织：地点分组 → 调度单分组 → 运单明细。

**卡片展开规则**：收起态显示摘要信息，展开态显示完整运单详情（订单号、地址、货品、预改约）。

### 操作页（Action / Form）

**场景**：对某条/某批运单执行具体操作，需要用户录入信息并提交。例如提柜操作页（录入柜号 + 上传照片 + 提交）、返重柜操作页、异常提报录入页、变更柜号页。

**结构**：
- 标题栏（返回箭头 + 标题）
- 当前位置（可选）
- 数据展示区（只读，展示选中的运单信息）
- 录入区（输入框、选择器、图片上传区域）
- 底部固定操作栏（提交按钮，button-primary-large）

**判据**：用户需要"针对特定对象录入信息并确认提交"时使用。操作页通常由列表页点击某个操作按钮跳入，提交后返回列表页并刷新数据。

**底部固定操作栏**：用 `.action-bar`（白底 + 顶部 0.5px 细线，sticky 贴底）承载全宽主按钮 `.btn.btn--lg.btn--primary`。

**校验规则**：必填项校验失败时使用 toast 提示（`danger-1` 文字），输入框下方可显示红色错误文字。

**参考**：`examples/demo-trailer-detail.html`（拖车业务提柜详情/操作页：状态栏+标题栏 → 定位栏 → 拖车业务卡片·详情版 → 底部提交栏）。

> **拖车业务卡片·详情页版本**：在列表版基础上，于运单小卡片灰底身（`.card__order-body`）字段下方追加「拍照获取搜索框」（`.searchbox` 拍照获取变体）+「图片上传组件」（`.uploader`，如集装箱号照片/柜号照片，每区最多 9 张）。完全复用已有组件，不新增卡片专属 class；详见 `card.json → 拖车业务卡片结构.detailVariant`。

### 弹窗/面板（Dialog / Panel）

**场景**：轻量级操作，不需要独立页面。例如过磅登记（输入重量）、入园改约（选择日期时间段）、单号查询（输入运单号/柜号）、更多操作菜单。

**结构**：
- 底部弹出面板（圆角顶部，白色背景）
- 标题 + 内容区 + 操作按钮（取消/确定）

**判据**：操作步骤≤2步、无需展示大量数据时使用面板。若操作复杂或需要展示列表，应使用独立操作页。

**弹窗规范**（写入 `.dialog-overlay` / `.dialog`）：
- **遮罩**：色值 `#000000`、透明度 **60%**（`rgba(0,0,0,0.6)`）；**限制在页面宽度内**（设计宽度 375px 居中，不铺满整个浏览器视口；交付移动端 `max-width:100%`）。默认 `display:none`（不拦截点击），用 `XUI.openDialog/closeDialog` 开合。
- **表单字段（输入/选择）统一上下布局**：title（`.dialog__field-label`）在上、输入框（`.input`）/选择框（`.dialog__field-select`）在下，不用左右内联。
- 弹窗容器 320px 白底 8px 圆角，关闭按钮固定右上角。

**参考**：`examples/demo-trailer-weighing.html`（过磅登记弹窗：`.dialog` + `过磅重量` 上下布局 `.input` + KG + 提交）；`examples/demo-trailer-reschedule.html`（入园改约弹窗：预约入园日期只读 `.input` + 预约时间段两个 `.dialog__field-select`（起—止）+ 提交）。均用 `XUI.openDialog/closeDialog` 触发。

---

### 页型选型决策树

```
用户要做什么？
├── 认证身份 → 登录页
├── 概览全局 / 选择入口 → 首页
├── 在多个子功能中选择 → 功能选择页
├── 浏览/筛选/批量操作同类任务 → 列表页
├── 针对某条任务录入信息并提交
│   ├── 操作复杂（多字段/上传照片） → 操作页
│   └── 操作简单（1-2个字段） → 弹窗/面板
└── 查看单条详情（物流轨迹） → 详情页（扩展）
```

---

## 卡片与功能模块对应关系

**硬规则**：每个列表页 / 操作页必须使用与其业务对应的卡片组件排版，不得混用、不得自造。**拖车业务的所有列表页一律用「拖车业务卡片」排版；其余业务列表页用各自对应的卡片组件。**

| 卡片类型 | 使用页型 | 所属功能模块 / 页面 | 说明 |
|---------|---------|------------------|------|
| **拖车业务卡片**（`.card.card--trailer`） | 列表页 | 拖车业务全部列表页：提柜、入园、落柜、提重柜、离园、过磅、返重柜、改约 | 场站头 → 调度单 → 运单小卡片三层结构；逐页字段/场站标签/按钮见 `card.json → 拖车业务卡片结构.pageFieldConfig`；过磅页卡片无场站头 |
| **运单卡片**（`.card`） | 列表页 | 待到库、待提货（含待发运 Tab）、待打卡、待派送、待运抵、待签收、待办中心 | 各模块字段差异见 `card.json → 运单卡片结构.moduleConfig` |
| **物流信息卡片** | 列表页 | 订单管理 | 管理端订单管理列表页使用 |
| **签收管理卡片** | 操作页 | 待签收下的：整单签收、整单拒收、回单上传 | 含签单/回单图片上传与拒收原因选择（图片上传用 `uploader`，拒收原因用 `sheet` 动作面板） |

**司机端首页功能模块**（对应金刚区图标）：
待到库、待提货、待发运、待打卡、待派送、待运抵、待签收、回单上传、送货交接、历史记录、服务反馈、拖车业务、异常提报、订单管理

金刚区图标路径：`assets/shortcuts/icon/home/driver/`（司机端）和 `assets/shortcuts/icon/home/oa/`（管理端）

## 拖车业务页面流程（导航映射）

拖车业务的页面跳转链路，做 demo 时按此直接实现点击交互（机读版见 `scenario-map.json → navigationFlows.拖车业务`）：

```
首页(demo-home) ──点击金刚区「拖车业务」──▶ 拖车业务导航页(功能选择页, demo-trailer)
拖车业务导航页 ──点击各功能球──▶ 对应列表页 ──点击卡片操作按钮──▶ 详情/操作页
```

- **首页金刚区「拖车业务」**：点击进入拖车业务导航页（功能选择页 Hub，`examples/demo-trailer.html`）。
- **拖车业务导航页**：功能球网格，各子功能球点击进入各自列表页。
- **列表页 → 详情/操作页**：点击列表卡片底部的操作按钮进入。例如**提柜列表页点「提柜」按钮 → 提柜详情/操作页**（`demo-trailer-detail`，即前述详情页模板）。
- **各模块 → 列表页 → 详情/操作页** 映射：

| 导航页模块 | 列表页（卡片=拖车业务卡片） | 卡片按钮 | 点击后 |
|---|---|---|---|
| 提柜 | 提柜列表页 | 提柜 | 提柜详情/操作页（`demo-trailer-detail`） |
| 入园 | 入园列表页 | 入园登记 | 入园登记操作页 |
| 落柜 | 落柜列表页 | 落柜登记 | 落柜登记操作页 |
| 提重柜 | 提重柜列表页 | 提重柜登记 | 提重柜登记操作页 |
| 离园 | 离园列表页 | 离园登记 | 离园登记操作页 |
| 过磅 | 过磅列表页（卡片无场站头） | 过磅登记 | 过磅登记（弹窗/面板，输入重量） |
| 返重柜 | 返重柜列表页 | 返重柜 | 返重柜详情/操作页 |
| 改约 | 改约列表页 | 改约 | 改约（弹窗/面板，选时间） |

> 其余子功能：派车、换车接单、业务监控。**异常提报**点击后进入一个「通用导航页」（menu-item 列表，非功能球网格），标题「异常提报」，列表项：**返空柜 / 变更柜号 / 其他异常**（成品见 `demo-exception-report`）。各列表页逐页字段/场站标签/按钮见 `card.json → 拖车业务卡片结构.pageFieldConfig`；详情/操作页模板见 `demo-trailer-detail`。子功能正确命名为 入园/离园/返重柜。

## 该做与不该做

- 用 token 名称引用颜色，不要硬编码 hex 值。
- 用文字色梯度为信息排序：`text-3` 用于主文字，`text-2` 用于辅助，`text-1` 仅用于 placeholder。
- 将品牌色 `vi-2` 保留给主要操作与选中态，不要用于装饰性填充。
- 禁用态统一使用 40% 透明度降低文字/图标，不改变背景色。
- 卡片内嵌内容使用 `bg-1` 底色，不要用 `white`，否则无法区分层级。
- 保持 4px 间距基础刻度，不使用奇数或非 4 倍数的间距值。
- 一个视图内保持统一的圆角家族，不混用不同圆角值。
- 标签颜色承载业务含义（蓝=运单状态，橙=2C/收货点），不要随意替换。
- 不要在按钮内使用 Medium 或 Semibold 字重，按钮统一使用 Regular。
- 不要将 `bg-2` 用作通用背景，它仅用于预改约底部等特定区域。
- 搜索框 placeholder 使用 `color-text-4`（#C9CDD4，旧 text-1），不要使用更深的 `color-text-3`。
- 浮动按钮仅放置在右下角固定定位，不要用于页面内嵌。

---

## Agent 消费速查（落地补充）

> 本节为原 `AGENTS.md` 中**信小递专属**的落地细则下沉而来。跨系统的通用铁律见工程根目录 `AGENTS.md`；本节只讲信小递自己的具体值。

### 品牌与基准

- **平台**：微信小程序（移动端）。**设计宽度 375px**（iPhone X），**内容宽度 343px**（左右各 16px 边距）。
- **品牌色 `#00AAA6`**（vi-2）。**字体唯一 PingFang SC**，按钮文字统一 Regular(400)。
- 设计性格：简洁实用、卡片圆角、克制色彩、清晰层级、操作效率优先。

### 颜色使用规则

| 用途 | Token（新命名） | 值 | 旧别名 |
|------|-------|------|------|
| 深色按钮背景 | brand / primary-6 | #00AAA6 | vi-2 |
| 深色按钮 hover/点击 | brand-active / primary-7 | #009093 | vi-3 |
| 深色按钮悬浮 | brand-hover / primary-5 | #22BBB3 | — |
| 浅色实底按钮背景 | brand-bg / primary-1 | #E8FFFB | vi-1 |
| 半透明浅色按钮 | brand-bg-subtle | rgba(0,170,166,0.1) | — |
| 页面背景 / 卡片内嵌区 | color-fill-2 | #F2F3F5 | bg-1 |
| 预改约底部等特定区域 | color-fill-3 | #E5E6EB | bg-2 |
| 卡片背景 | color-fill-white | #FFFFFF | white |
| 主文字 | color-text-1 | #1D2129 | text-3 |
| 次强调正文 | color-text-2 | #4E5969 | — |
| 辅助/次要文字 | color-text-3 | #86909C | text-2 |
| 占位符 / 置灰 | color-text-4 | #C9CDD4 | text-1 |
| 分割线 / 输入框边框 | color-border-2 | #E5E6EB | border-1 |
| 输入框 focus 边框 | brand | #00AAA6 | vi-2 |
| 错误 / 必填 | danger | #F53F3F | danger-1(旧#EE0A24) |
| 成功 | success | #00B42A | — |
| 警告 | warning | #FF7D00 | — |
| 信息 | info | #165DFF | — |
| 蓝色标签（运单/提货） | blue / arcoblue-6 | #165DFF | blue(旧#3491FA) |
| 橙色标签（2C/收货） | orange / orange-6 | #FF7D00 | orange |
| 紫色标签（电商补货） | purple / purple-6 | #722ED1 | purple |

### 旧 Figma 稿迁移对照（v1.0 → v1.1）

> **何时用这张表**：拿到仍用旧命名（`vi-1`、`text-3` 等）或写死旧色值/旧尺寸的 Figma 稿实现组件时，按"旧稿写的"这一列反查，落地时**统一改写成新命名**。旧别名在 `ui.css` 里仍可用（不会报错），但新代码请写新名。方向与上面《颜色使用规则》相反：那张按"用途"正向查，这张按"旧稿标注"反向查，且覆盖颜色 + 字体 + 间距 + 圆角 + 宽度。

**颜色（注意 text 编号是反的）**

| 旧稿写的 | 落地改写为 | 值 | 备注 |
|------|-----------|------|------|
| vi-1 | primary-1 | #E8FFFB | 浅底（旧 #E6F7F6 微调） |
| vi-2 | brand（= primary-6） | #00AAA6 | 品牌主色，值不变 |
| vi-3 | brand-active（= primary-7） | #009093 | 点击/hover，值不变 |
| text-3 | color-text-1 | #1D2129 | 主文字（编号反转！） |
| text-2 | color-text-3 | #86909C | 辅助/次要（旧 #7C8492） |
| text-1 | color-text-4 | #C9CDD4 | 占位/置灰（旧 #BFC5CC） |
| border-1 | color-border-2 | #E5E6EB | 分割线/输入框边框，值不变 |
| border-2 | color-border-3 | #C9CDD4 | 辅助线（旧 #BFC5CC） |
| bg-1 | color-fill-2 | #F2F3F5 | 页面背景/卡片内嵌（旧 #F3F5F7） |
| bg-2 | color-fill-3 | #E5E6EB | 预改约底部（旧 #EBEDF0） |
| white | color-fill-white | #FFFFFF | 卡片/输入框面 |
| 蓝 #3491FA | blue（= arcoblue-6） | #165DFF | 运单/提货标签 |
| 橙 #FF7D00 | orange（= orange-6） | #FF7D00 | 2C/收货，值不变 |
| 紫 #722ED1 | purple（= purple-6） | #722ED1 | 电商补货，值不变 |
| danger-1 #EE0A24 | danger（= red-6） | #F53F3F | 错误/必填 |
| danger-bg #FDE7E9 | danger-bg（= red-1） | #FFECE8 | 告警底 |

**字体 / 间距 / 圆角 / 宽度**

| 旧稿写的 | 落地改写为 |
|------|-----------|
| 大按钮 `width:303px` + `padding:0 119px` | `.btn--lg`（整行 `width:100%` + 左右内边距 16px），去掉写死宽 |
| 输入框/卡片 `width:303px` / `343px` | 输入框整行 `width:100%`；卡片 `width:100%` + `max-width:343px` |
| 圆角 `pill:58px` | `radius-pill`（999px，真胶囊） |
| 只有大/小两档按钮 | 需要中间态用新增的中按钮 `.btn--md`（36px） |
| 运单号/重量/时间用普通字体 | 用 `.text-number`（Nunito Sans + tabular-nums，等宽对齐） |

**规则**：旧稿标注的具体色值若 Pangea 有对应（如上表），直接换成新值；若旧稿某色 Pangea 没有对应、且明显是特意选的，先停下来跟你确认，不擅自替换。

### 字体规格速查

| 场景 | 字号 | 字重 | 行高 |
|------|------|------|------|
| 页面标题 | 16px | Medium(500) | 22px |
| 卡片标题 | 14px | Semibold(600) | 20px |
| 正文强调 | 14px | Medium(500) | 20px |
| 正文 | 12px | Medium(500) | 18px |
| 辅助信息 | 12px | Regular(400) | 18px |
| 次要/时间 | 10px | Regular(400) | 14px |
| 大按钮 | 16px | Regular(400) | 22px |
| 中按钮 | 14px | Regular(400) | 20px |
| 小按钮 | 14px | Regular(400) | 20px |
| 数字(运单号/重量/时间) | 14px | Medium(500) | 20px |（Nunito Sans, tabular-nums）

### 组件尺寸速查

| 组件 | 高度 | 宽度 | 圆角 |
|------|------|------|------|
| 大按钮 | 40px | block（100%，左右内边距 16px） | 4px |
| 中按钮 | 36px | auto（左右内边距 12px） | 4px |
| 小按钮 | 32px | auto（左右内边距 8px） | 4px |
| 输入框（注册） | 48px | block（100%） | 4px |
| 搜索框 | 36px | block（100%） | 4px |
| 卡片 | auto | block（100%，max-width 343px） | 10px |
| Tab 项 | 30px | auto | 4px |
| 浮动按钮 | 60px | 60px | 50% |
| 弹窗 | auto | 320px | 8px |
| 定位栏 | 48px | 100% | — |

> 宽度不再写死像素：大按钮/输入框/搜索框默认整行（`width:100%`），卡片 `width:100%` + `max-width:343px`，由父容器（内容区 343px）控制上限。需要内容自适应宽度用中/小按钮（`width:auto`）。

### 图标引用

```html
<img src="assets/icons/{功能}_{颜色}_{尺寸}px.svg" style="width:{尺寸}px; height:{尺寸}px;" />
```

尺寸档：48px（金刚区）/ 24px（通用）/ 20px（工具）/ 16px（辅助）/ 12px（箭头）。
颜色变体：gray / green / white / black。金刚区：`assets/shortcuts/icon/home/driver/{功能}.svg`（司机端）、`assets/shortcuts/icon/home/oa/`（管理端）。

示例：`search_gray_24px.svg`、`position_green_16px.svg`、`select/down_surface_green_12px.svg`、`close_gray_24px.svg`。

### 按任务怎么做

- **列表页**（最核心）：状态栏(44) → 标题栏(44) → 定位组件(48,可选) → 扫码接单(48,可选) → 搜索框(36) → Tab(30,可选) → 卡片列表(间距12) → 浮动按钮(可选)。参考 `examples/demo-list.html`。
- **操作页**：标题栏 → 数据展示区(只读) → 录入区(输入/选择/上传) → 底部固定提交按钮(40)。
- **弹窗**：宽 320px，内边距 24px，右上角关闭按钮(24px, top8 right8)；按钮组浅色在左深色在右；蒙层 rgba(0,0,0,0.5)。
- **首页**：渐变顶部(194px) + 扫码接单入口 + 金刚区(48px 图标网格) + 待办快捷区 + 浮动按钮。参考 `examples/demo-home.html`。

### 按钮组规范（卡片底部）

- 有「x单x件」统计文字 → 右侧按钮 ≤ 3 个。
- 无统计文字 → 右侧按钮 ≤ 5 个。
- 超出 → 显示「更多」文字按钮(14px, #00AAA6, 无底色)，点击弹浮窗（白底、8px 圆角、阴影 `0 4px 16px rgba(0,0,0,0.12)`，选项 padding 8px 16px、14px Regular #1D2129）。

### 信小递专属自查项

- [ ] 页面宽度：demo 用 375px 固定宽；交付开发用 `100% + max-width: 750px`（px×2=rpx）。
- [ ] 内容宽度 343px（两侧各 16px）。
- [ ] 间距全部是 4 的倍数（4/8/12/16/20/24/28/32/40/48）。
- [ ] 圆角只用 2/4/8/10/12/50%/pill(999) 这几档，同一视图不混用。
- [ ] 大按钮/输入框/搜索框默认整行（width:100%），不写死像素宽（不再用 303px/119px）。
- [ ] 按钮文字 Regular(400)，不用 Medium/Semibold。
- [ ] 标签颜色：蓝(#165DFF)=运单/提货，橙(#FF7D00)=2C/收货，紫(#722ED1)=电商补货——不可随意替换。
- [ ] 禁用态：只降文字 opacity 40%，不改背景色。
- [ ] placeholder 用 color-text-4(#C9CDD4)，不用 color-text-3。
- [ ] 卡片内嵌区域用 color-fill-2(#F2F3F5，旧 bg-1)，不用白色；color-fill-3(#E5E6EB，旧 bg-2) 仅用于预改约底部。
- [ ] 搜索框高 36px，查询按钮 28px 高 #00AAA6 背景白字。
- [ ] Tab 选中态 #00AAA6 背景白字，未选中白底黑字。
- [ ] Demo 里 `position:fixed` 浮层（弹窗蒙层 `.dialog-overlay`、浮动按钮 `.fab`）已在 `#app` 作用域改为 `position:absolute`，收敛到 375px 手机框内，不溢出到浏览器视口。

### 常见错误

❌ 把 color-fill-3(#E5E6EB，旧 bg-2) 当通用背景 → ✅ 只用于预改约底部
❌ 按钮用 Medium/Semibold 字重 → ✅ 按钮统一 Regular(400)
❌ 给按钮/输入框写死 width:303px 或 padding:0 119px → ✅ 用整行(width:100%) + 内边距 token
❌ 搜索框 placeholder 用 #86909C → ✅ 用 #C9CDD4(color-text-4)
❌ 标签颜色随意选 → ✅ 蓝/橙/紫各有固定业务含义
❌ 浮动按钮放页面中间 → ✅ 只放右下角固定定位
❌ demo 里弹窗蒙层/浮动按钮用 position:fixed 溢出到浏览器视口 → ✅ 在 #app 作用域改 position:absolute，收敛到 375px 手机框
❌ 卡片内嵌区用白色底 → ✅ 用 color-fill-2(#F2F3F5) 区分层级
❌ 用奇数间距(3px/7px/13px) → ✅ 只用 4 的倍数
❌ 圆角混用无规律 → ✅ 用组件级 radius token，同一视图统一圆角家族

---

## 场景匹配评估流程（生成任何 HTML 前必做）

在产出任何原型 HTML 之前，必须先做「场景匹配评估」，依据机读文件 `scenario-map.json`，**逐屏**（不是整个需求一次性）判断，并把评估结论**在对话里向用户汇报**——**不要写进 HTML**（产品经理看到的原型要保持干净，无过程注释）。

步骤：

1. 拆解 PRD，列出要做的每一屏，判断其页型（对照 `scenario-map.json` 的 `pageTypes`）。
2. 对每一屏，与 `scenario-map.json` 的 `examplePages` / `components` 比对，落到三档之一：

| 档位 | 判据 | 路由 |
|------|------|------|
| **高重合** | 命中某 examplePage 页型，且其核心区块覆盖 ≥ 70% | 以该 examplePage 为底板**复制微调** |
| **低重合** | 无现成成品页，但所需区块都能在 components 找到组件 | 用 components 组件 + `ui.css` class **逐块拼装** |
| **零重合** | 页型无成品页，且核心区块在 components 也无对应组件 | **停止生成**，走缺口流程 |

3. **高重合的"微调"允许范围**：替换数据/文案/图标；**隐藏或删除组件里当前场景用不到的子元素**（例如卡片某字段为空就整段不渲染）；增减列表项；复用组件已有状态类（collapsed/expanded/checkbox）。**禁止**：改组件 DOM 骨架、重写组件样式、加规范外装饰。
4. **低重合**：每一区块都要能追溯到某个组件 slug；禁止自造组件、禁止引用 examples 里未回收的页面私有 class。
5. **零重合**：立即停止该屏生成，先输出《缺口报告》（缺哪些组件/页型/图标/token，分别属于哪屏哪块），再询问用户二选一——(A) 人类补齐缺失项后再生成；(B) 同意先自由发挥（产出标记为非规范）。**未得到答复不得擅自发挥。**

评估示例（在对话里汇报的格式）：

> 场景匹配评估：
> - 首页 → 高重合（demo-home，复制微调；隐藏公告条）
> - 提柜列表 → 高重合（demo-list，复制微调）
> - 提柜操作页 → 低重合（用 card + input + button + selector 拼装）
> - XX 特殊页 → 零重合 → 见《缺口报告》，请选择 A/B

### 首页功能入口的歧义确认（必问）

当 PRD / 需求描述**没有说清**一个新功能在首页如何接入时，**必须先停下来向人类确认**，二选一：

1. **在首页金刚区新增功能球**（新增模块）？
2. **在现有某个功能球里改**（复用已有入口）？

确认后按对应方式处理，两种情况**首页都直接引用示例首页 `examples/demo-home.html`，绝不整块重画首页**：

- **新增功能球** → 引用 demo-home，在金刚区（function-grid）里**加一个新图标**（真实 SVG，来自 `assets/shortcuts/icon/home/driver/`；如需角标则叠加），点击进入该功能的功能选择页或列表页。首页其余内容（渐变头部、快捷卡、其余金刚区图标、待办任务、浮动按钮）保持 demo-home 原样。
- **在现有功能球里改** → 同样引用 demo-home，**不新增图标**，点击对应的现有功能球直接进入该功能的列表页；首页其余内容保持不变。

> 反例（禁止）：把首页金刚区改成 emoji、把待办任务换成自造九宫格、去掉渐变头部——这些都属于"整块重画首页"，违反本规则。

### 待办任务区固定不动

首页下方的「待办任务」区（`.section-title`「待办任务」+ 其下方的运单卡片列表，见 `examples/demo-home.html`）是**固定模块**。生成任何基于首页的新原型时：

- 该区**原样复制 demo-home**，不得增删卡片、改文案、换布局、改样式。
- **仅当用户明确要求改动「待办任务」**（如"待办任务改成 XX""待办任务去掉/增加一张卡"）时才可调整；用户未提及即视为不动。
- 改动首页其他区域（金刚区、快捷卡、头部）时，待办任务区同样保持原样，不受牵连。

> 这是对上一节反例"把待办任务换成自造九宫格"的正面细化：不只是禁止换成九宫格，而是该区整体不得擅自改动。

## Figma/PRD 还原前置流程（拿到设计稿第一步必须先查库，不得凭记忆）

当收到以下任一任务时，**禁止直接凭记忆写代码**，必须先执行查库步骤：

- 用户给了 Figma 设计稿链接要求还原页面
- 用户给了 PRD / 截图 / 口头描述要求出原型 demo
- 任何涉及「按设计稿实现」的场景

**前置三步（缺一不可，按顺序执行）：**

### 1. 查 Token 库（`tokens.json`）
- 拿到 Figma 稿里的任意色值、间距、圆角、字号后，**必须先对照《旧 Figma 稿迁移对照》表**（第 620 行）反查对应的语义 token。
- 落地时统一改用**新命名**（如 `primary-6`、`brand`、`color-text-1` 等），不得直接用旧别名（`vi-1`、`text-3` 等），即使用旧别名不报错也不行。
- Figma 稿里的色值若 Pangea 有对应，直接换新值；若明显无对应，停下来跟用户确认，不擅自替换。

### 2. 查 SVG 库（`assets/`）
- Figma 稿里的每个图标，**必须先搜 `assets/` 目录**是否有同名或同类 SVG。
  - 图标引用规范见第 689 行：`<img src="assets/icons/{功能}_{颜色}_{尺寸}px.svg">`
  - 金刚区图标在 `assets/shortcuts/icon/home/{角色}/`
  - 拖车业务图标在 `assets/icons/tuoche/`
- **有现成 SVG → 必须用 `<img>` 引用**，不得手画 `<svg>` path。
- **无现成 SVG → 告知用户缺失**，不擅自手画替代。

### 3. 查组件库（`components/` + `ui.css`）
- 页面涉及的每个 UI 元素（标题栏、定位栏、搜索框、按钮、卡片、Tab、浮动按钮等），**必须先查 `components/*.json` 确认有无对应组件**。
- 有现成组件 → 必须用 `ui.css` 里的 class 实现，不得自造同名 class 或用内联样式重写。
- 无现成组件 → 按 `scenario-map.json` 的 knownGaps 判断是 deferred 缺口还是需新建，再跟用户确认方案。

> **反面案例（2026-07-27，拖车业务定位 icon）**：Figma 稿 Vector fill = `#00aaa6`（主色），未翻迁移表反查，凭记忆写成 `var(--vi-1)`（= `#E8FFFB` 浅底），颜色查错；本地有现成 `position_green_16px.svg`，却手画 `<svg>` path，双重违规。见日志 2026-07-27.md 第五轮。

## 产出后强制校验（机械自检，非声明）

原型产出后，必须逐条**实际核对**（不是口头声明"已复用"）。任一未过即为交付失败，必须返工：

1. **权威源**：原型引用的样式必须指向本 skill 的权威 `references/ui.css`。
2. **class 白名单**：抽取原型里所有 `class="..."` 的类名，逐个在 `ui.css` 与各组件 JSON 的 `cssClasses` 里查；**凡查不到的一律视为"疑似自造"**，必须改用组件类，或在零重合流程里显式报备。
3. **图标**：所有 `<img src>` 必须落在 `references/assets/` 下，不使用自创内联 SVG 图标。
4. **不留过程注释**：HTML 里不写场景评估、路由决策等过程性注释；这些只在对话中向用户汇报。

> 上述校验由 `scripts/verify-prototype.mjs` 自动执行：`node .kiro/skills/xinxiaodi-design/scripts/verify-prototype.mjs <原型HTML绝对路径>`（默认 `--ds references`）。
