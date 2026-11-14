# 🎨 Refactoring UI 原则 / Refactoring UI Principles

把界面视觉质量变成可执行清单的 Agent Skill —— 写、改或走查页面、dashboard、落地页和组件时，按 20 条规则检查层级、间距、排版、色彩和空状态。

An Agent Skill that turns UI polish into an actionable checklist: 20 visual rules from *Refactoring UI* covering hierarchy, spacing, typography, color, and empty states, applied when building or reviewing product interfaces.

遵循 [Agent Skills 开放标准](https://agentskills.io)，兼容 Claude Code、Cursor、GitHub Copilot、Codex、Windsurf、Gemini CLI、Perplexity Computer 等 AI Agent 平台。

## 安装 / Install

```bash
npx skills add Ficere/refactoring-ui-skill
```

> 需要 Node.js。安装后 Agent 会自动发现并按需加载该技能。
>
> Requires Node.js. Once installed, your agent will auto-discover and load this skill when relevant.

<details>
<summary>其他安装方式 / Alternative methods</summary>

**手动安装 / Manual install：**

```bash
git clone https://github.com/Ficere/refactoring-ui-skill.git refactoring-ui-principles
# 将整个目录复制到你的 Agent 的 skills 目录下即可
# Copy the directory to your agent's skills folder:
#   Claude Code:  ~/.claude/skills/
#   Cursor:       .cursor/skills/
#   Copilot:      .github/skills/
#   Codex:        ~/.codex/skills/
#   Gemini CLI:   .gemini/skills/
```

**Perplexity Computer：**

下载本仓库 zip → 在 [Skills 管理页面](https://www.perplexity.ai/computer/skills) 上传。

</details>

## 使用 / Usage

安装后直接用自然语言触发，无需任何配置：

```
帮我走查一下这个设置页，看看视觉层级哪里有问题
```

```
这个 dashboard 看着很乱，按 Refactoring UI 的原则改一版
```

```
给这张用户卡片重新设计样式：头像、姓名、职务、邮箱、电话
```

```
这个列表还没有数据时该怎么展示？帮我设计空状态
```

```
Review this landing page against Refactoring UI rules and fix what fails
```

做网页前端时，建议同时加载 [`frontend-design`](https://github.com/anthropics/skills/tree/main/skills/frontend-design)：前者定审美方向，本 skill 管细节规则。

```bash
npx skills add anthropics/skills --skill frontend-design
```

## 规则覆盖 / Features

| 模块 | 规则 | 说明 |
|------|------|------|
| **动手之前** | 1–2 | 定一种个性并贯彻到底；先灰度把主次做清楚，再上色 |
| **视觉层级** | 3–6 | 用颜色和字重而非只靠字号；弱化次要元素；省掉多余标签；每页只有一个主按钮 |
| **空间与布局** | 7–10 | 从过度留白开始收紧；内容不拉满；组间距大于组内距；跨断点不等比缩放 |
| **排版** | 11–12 | 行高随行长和字号调整；混合字号按基线对齐 |
| **色彩与无障碍** | 13–15 | 准备完整色阶；徽章用浅底深字；状态不只靠颜色 |
| **质感与图片** | 16–18 | 强调色边点到为止；图上文字先改背景；图标与截图保持自然尺寸 |
| **细节** | 19–20 | 少用 1px 边框；优先设计空状态 |
| **出手前自检** | — | 7 项交付前检查清单 |

<details>
<summary>20 条规则一览 / All 20 rules</summary>

| # | 规则 |
|---|------|
| 1 | 先定一种个性，并一贯到底 |
| 2 | 先灰度，后上色 |
| 3 | 不要只靠字号拉层级 |
| 4 | 用弱化来凸显重点 |
| 5 | 展示数据时，非必要不用标签 |
| 6 | 按页面主次设按钮，不要按操作语义 |
| 7 | 从过度留白开始，再逐步收紧 |
| 8 | 不要因为画布宽就把内容拉满 |
| 9 | 组间距必须大于组内距 |
| 10 | 不要跨断点等比缩放一切 |
| 11 | 行高跟行长成正比，跟字号成反比 |
| 12 | 同行近距离的不同字号按基线对齐 |
| 13 | 五色方案做不了真实产品 |
| 14 | 徽章、提示条优先浅底深字 |
| 15 | 不要只靠颜色传递状态 |
| 16 | 用一道强调色边给平淡布局加焦点 |
| 17 | 图片上的文字，先改背景再改字 |
| 18 | 图标和截图用自然尺寸，不要随意拉伸 |
| 19 | 先别画 1px 灰色边框 |
| 20 | 依赖用户内容的功能，优先设计空状态 |

每条规则的具体数值与例外见 [`SKILL.md`](SKILL.md)。

</details>

## 目录结构 / Structure

```
refactoring-ui-skill/
├── SKILL.md      # 技能入口（Agent 自动读取）：20 条规则 + 出手前自检
└── README.md
```

## 来源与版权 / Credits

规则精炼自 Adam Wathan 与 Steve Schoger 的 [*Refactoring UI*](https://www.refactoringui.com/)，取材口径参考龙海的文章 [人人都是 UI 设计师](https://x.com/longhaiqwe123/status/2106216781174251724)。

本仓库是操作清单，不是原文摘录。《Refactoring UI》的版权属于原作者；请不要把原书或文章大段复制进产品或文档。

Rules are distilled from *Refactoring UI* by Adam Wathan and Steve Schoger. This repo is an actionable checklist, not an excerpt; all rights to the book belong to its authors.
