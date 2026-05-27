# Xiaohongshu Post Cover Skill

[中文](#中文) | [English](#english)

## 中文

一个面向 Codex 的小红书内容创作 skill：将零散经历、观点、教程素材或产品体验，整理成带 emoji、适合直接修改发布的中文帖子；需要时再生成竖版封面图。

### 能做什么

- 生成经验分享、工具测评、避雷吐槽、教程总结、推荐种草和求助讨论等不同类型的帖子
- 默认加入适量 emoji、标题备选和话题标签
- 根据素材判断文章意图和结尾方式，不会把所有内容都写成“求助讨论”
- 仅在用户明确提出或确认后生成封面图

### 使用示例

```text
用 $xiaohongshu-post-cover 把下面的 AI 工具体验整理成一篇带 emoji 的小红书帖子：……
```

```text
用 $xiaohongshu-post-cover 把这份学习复盘写成教程总结型帖子，不要写成求助讨论。
```

```text
用 $xiaohongshu-post-cover 为这篇测评生成文案，并制作一张竖版封面图。
```

### 安装

在 Codex 中提出安装请求：

```text
请从 GitHub 安装这个 skill：
https://github.com/gouzigouzi/xiaohongshu-post-cover-skill/tree/main/skills/xiaohongshu-post-cover
```

安装完成后，重启 Codex 以加载新 skill。

也可以手动将 [`skills/xiaohongshu-post-cover`](skills/xiaohongshu-post-cover) 目录复制到 `$CODEX_HOME/skills/` 下。

### 目录结构

```text
skills/xiaohongshu-post-cover/
├── SKILL.md
└── agents/
    └── openai.yaml
```

### 设计原则

- 真实表达优先：保留用户的原始态度和具体经历。
- 意图匹配优先：先识别分享、测评、教程或求助等目标，再决定文章结构。
- 可读性优先：emoji 用于分段和强调，不堆砌。
- 图文解耦：文本可以独立完成，封面生成始终是可选动作。

## English

A Codex skill for drafting Xiaohongshu (RED) posts in Chinese. It transforms rough experiences, opinions, tutorial notes, and product reviews into emoji-enhanced, publish-ready copy, with an optional vertical cover image when requested.

### Features

- Supports experience sharing, tool reviews, cautionary posts, tutorial summaries, recommendations, and help-seeking discussions
- Adds a moderate amount of emoji, optional title variants, and relevant hashtags by default
- Identifies the post's intent before choosing its conclusion, instead of turning every post into a request for advice
- Generates a cover image only when the user explicitly requests or confirms it

### Usage Examples

```text
Use $xiaohongshu-post-cover to turn the following AI tool experience into an emoji-rich Xiaohongshu post in Chinese: ...
```

```text
Use $xiaohongshu-post-cover to rewrite this study reflection as a tutorial-summary post, not a help-seeking discussion.
```

```text
Use $xiaohongshu-post-cover to draft copy for this product review and create a vertical cover image.
```

### Installation

Ask Codex to install the skill from GitHub:

```text
Install this skill from GitHub:
https://github.com/gouzigouzi/xiaohongshu-post-cover-skill/tree/main/skills/xiaohongshu-post-cover
```

Restart Codex after installation to load the skill.

Alternatively, copy [`skills/xiaohongshu-post-cover`](skills/xiaohongshu-post-cover) into `$CODEX_HOME/skills/` manually.

### Repository Layout

```text
skills/xiaohongshu-post-cover/
├── SKILL.md
└── agents/
    └── openai.yaml
```

### Design Principles

- Preserve authenticity: keep the user's original stance and concrete experience.
- Match intent first: distinguish between sharing, reviewing, teaching, recommending, and asking for input.
- Favor readability: use emoji to structure and highlight content, not to crowd it.
- Keep images optional: the text output stands on its own; cover generation is always opt-in.

## License

[MIT License](LICENSE)
