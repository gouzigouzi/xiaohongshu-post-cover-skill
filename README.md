# xiaohongshu-post-cover-skill

English | [简体中文](README.zh-CN.md)

`xiaohongshu-post-cover` is a Codex skill for drafting Xiaohongshu (RED) posts in Chinese from rough experiences, opinions, tutorial notes, and product reviews.

It produces emoji-enhanced, publish-ready Chinese copy and can optionally generate a vertical cover image when the user requests or confirms one.

## What It Creates

- Experience-sharing posts
- Tool and product reviews
- Cautionary or complaint posts
- Tutorial and study-summary posts
- Recommendations
- Help-seeking discussions when the user actually wants reader input
- Optional vertical cover images for the post

## Writing Behavior

- Adds a moderate amount of emoji, optional title variants, and relevant hashtags by default.
- Identifies the post's intent before choosing its conclusion.
- Preserves the user's concrete experience and original stance.
- Does not turn every post into a help-seeking discussion.
- Does not generate an image unless the user explicitly asks for one or confirms it.

## Project Layout

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

## Usage Examples

Draft an emoji-rich Chinese post from an AI tool experience:

```text
Use $xiaohongshu-post-cover to turn the following AI tool experience into an emoji-rich Xiaohongshu post in Chinese: ...
```

Write a tutorial-style post without turning it into a request for advice:

```text
Use $xiaohongshu-post-cover to rewrite this study reflection as a tutorial-summary post, not a help-seeking discussion.
```

Generate post copy plus an optional cover image:

```text
Use $xiaohongshu-post-cover to draft copy for this product review and create a vertical cover image.
```

## Installation

Ask Codex to install the skill from GitHub:

```text
Install this skill from GitHub:
https://github.com/gouzigouzi/xiaohongshu-post-cover-skill/tree/main/skills/xiaohongshu-post-cover
```

Restart Codex after installation to load the skill.

Alternatively, copy [skills/xiaohongshu-post-cover](skills/xiaohongshu-post-cover) into `$CODEX_HOME/skills/` manually.

## Skill Integration

The repository contains the Codex skill at [skills/xiaohongshu-post-cover/SKILL.md](skills/xiaohongshu-post-cover/SKILL.md).

The skill tells Codex:

- how to classify the post intent before writing
- how to use emoji without overcrowding the copy
- when interaction questions are appropriate
- when to ask about or generate a cover image

## Notes

- The skill writes Xiaohongshu post copy in Simplified Chinese by default.
- Cover image generation depends on image-generation capability being available in the Codex session.
- Generated copy should still be reviewed before publishing, especially when it mentions specific products, platforms, or personal claims.

## License

[MIT License](LICENSE)
