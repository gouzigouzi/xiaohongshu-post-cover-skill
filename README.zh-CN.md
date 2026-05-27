# xiaohongshu-post-cover-skill

[English](README.md) | 简体中文

`xiaohongshu-post-cover` 是一个面向 Codex 的小红书内容创作 skill，用于将零散经历、观点、教程素材或产品体验整理成中文帖子。

它默认生成带适量 emoji、适合继续修改和发布的文案；用户明确提出或确认需要时，还可以继续生成竖版封面图。

## 支持的帖子类型

- 经验分享帖
- 工具或产品测评帖
- 避雷与吐槽帖
- 教程与学习总结帖
- 推荐种草帖
- 用户确实想征集意见时的求助讨论帖
- 可选的小红书竖版封面图

## 写作行为

- 默认加入适量 emoji、可选标题备选和相关话题标签。
- 先识别文章意图，再选择结尾方式。
- 保留用户的具体经历和原始立场。
- 不会把所有内容都改写成“求助讨论”。
- 用户没有明确提出或确认图片需求时，不会自动生成封面图。

## 项目结构

```text
xiaohongshu-post-cover-skill/
  README.md
  README.zh-CN.md
  LICENSE
  skills/
    xiaohongshu-post-cover/
      SKILL.md
      agents/
        openai.yaml
```

## 使用示例

将 AI 工具体验整理成带 emoji 的中文小红书帖子：

```text
用 $xiaohongshu-post-cover 把下面的 AI 工具体验整理成一篇带 emoji 的小红书帖子：……
```

将学习复盘写成教程型帖子，不写成求助讨论：

```text
用 $xiaohongshu-post-cover 把这份学习复盘写成教程总结型帖子，不要写成求助讨论。
```

生成测评文案并制作可选封面图：

```text
用 $xiaohongshu-post-cover 为这篇测评生成文案，并制作一张竖版封面图。
```

## 安装

在 Codex 中提出安装请求：

```text
请从 GitHub 安装这个 skill：
https://github.com/gouzigouzi/xiaohongshu-post-cover-skill/tree/main/skills/xiaohongshu-post-cover
```

安装完成后，重启 Codex 以加载新 skill。

也可以手动将 [skills/xiaohongshu-post-cover](skills/xiaohongshu-post-cover) 目录复制到 `$CODEX_HOME/skills/` 下。

## Skill 集成

仓库中的 Codex skill 位于 [skills/xiaohongshu-post-cover/SKILL.md](skills/xiaohongshu-post-cover/SKILL.md)。

它会指导 Codex：

- 在写作前判断帖子意图
- 合理使用 emoji，避免文案显得拥挤
- 仅在适合时加入互动问题
- 何时询问或生成封面图

## 说明

- 该 skill 默认生成简体中文的小红书文案。
- 封面图生成依赖当前 Codex 会话中可用的图像生成能力。
- 发布前仍建议人工检查文案，尤其是涉及具体产品、平台或个人经历描述时。

## License

[MIT License](LICENSE)
