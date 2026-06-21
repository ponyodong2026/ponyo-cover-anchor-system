# PONYO Cover Anchor System

小红书 / 公众号封面「信息密度 × 视觉锚点」生成系统。

封面要解决的从来不是“好看”，而是让用户在信息流里 3 秒内决定：这条内容和我有没有关系。

![12 cover cases](examples/cover-cases/preview_12_final.jpg)

## What It Does

输入主题、目标人群和内容类型后，这个 skill 会输出：

- 推荐封面模板
- 锚点位置
- 配色方案
- 字重层级
- 可直接用于 ChatGPT Image 2 / DALL-E 的生图提示词
- 排版指导

## Core Formula

点击率主要由两个变量决定：

- **信息密度**：利益点在缩略图里是否一眼看清
- **视觉锚点**：画面里是否有一个让眼睛停住的位置

## Four Cover Templates

| Template | Formula | Best For |
|---|---|---|
| 冲突型 | 反直觉标题 × 强对比色 × 人物遮罩 | 知识、观点、AI 工具 |
| 数字型 | 大号数字锚点 × 色块分割 × 悬念副标题 | 干货、教程、步骤 |
| 截图型 | 真实截图遮罩 × 手写感标注 × 低饱和底色 | 案例、结果、测评 |
| 情绪型 | 全出血人物图 × 单行大字 × 撞色条 | 情感、生活、故事 |

## Repository Structure

```text
cover-anchor-system/
  SKILL.md
  references/
    template-formulas.md
    image-prompts.md
examples/
  cover-cases/
    preview_12_final.jpg
    01_*.png ... 12_*.png
```

## Install

Copy the `cover-anchor-system` folder into your local skills directory, then call it when designing covers:

```text
~/.codex/skills/cover-anchor-system
```

Or read `cover-anchor-system/SKILL.md` directly and use the prompt library inside `references/image-prompts.md`.

## Size Reference

| Platform | Ratio | Recommended Size |
|---|---:|---:|
| 小红书封面 | 3:4 | 1080 × 1440px |
| 小红书正方 | 1:1 | 1080 × 1080px |
| 公众号头图 | 3:1 | 900 × 383px |
| 公众号次图 | 1:1 | 500 × 500px |

## Example Cases

The `examples/cover-cases` folder contains 12 ChatGPT Image 2 cover examples:

- 3 conflict-style covers
- 3 number-style covers
- 3 screenshot-style covers
- 3 emotional-style covers

These examples are included to show the intended visual output: real social-media covers, not explanatory slides or article illustrations.
