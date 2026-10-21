# Engineering Playbook

End to end engineering concepts explained (how technology works). Live at [playbook.isidd.dev](https://playbook.isidd.dev).

## How it works
- **Home page:** every entry, newest first, **12 per page**. Older entries continue on `/page2/`, `/page3/` and so on, with page numbers and Newer / Older links at the bottom.
- **Each entry** opens its own page at `playbook.isidd.dev/<title>/`, with the date, reading time and author (Siddharth Singh) at the top.
- **Search** in the top bar looks through every entry's title, tags and date, across all pages.
- Black on white, EB Garamond only (monospace is used inside code blocks).

## Add an entry
Create `_posts/YYYY-MM-DD-title-with-hyphens.md`:

```markdown
---
layout: post
title: "How transformers pay attention"
subtitle: "One-line summary"   # optional
tags: [AI, LLM]
read: 9                        # optional, otherwise counted automatically
---

Your explanation here. Use ## for section headings.
```

The file name decides the address: `2026-10-22-how-transformers-pay-attention.md` → `playbook.isidd.dev/how-transformers-pay-attention/`.
Always close the top block with `---` on its own line.

## Settings
`_config.yml`: `paginate: 12` sets how many entries show per page. Pagination uses `jekyll-paginate`, which GitHub Pages supports out of the box.

Fonts: EB Garamond (SIL OFL, self-hosted). MIT [LICENSE](LICENSE).
