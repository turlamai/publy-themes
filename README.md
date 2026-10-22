# Publy Theme Registry

**English** · [中文](README.zh-CN.md)

Curated index of Publy themes (article themes for Markdown → WeChat HTML, card themes for image-post 3:4 PNG decks). `publy theme ls` reads `index.json` from this repo.

## Format

```json
{
  "version": 1,
  "themes": [
    { "id": "my-theme", "kind": "article | card", "source": "builtin | npm", "npm": "@scope/publy-theme-my-theme", "description": "..." }
  ]
}
```

## Submitting a theme

1. Publish your theme as an npm package named `publy-theme-*` (article theme: CSS scoped under `#publy`; card theme: a `CardTheme` style config module).
2. Include a rendered preview image in the package README.
3. Open a PR adding an entry to `index.json`.

External theme submission opens with M4; until then the registry lists the built-ins.
