# Publy Theme Gallery

**English** · [中文](README.zh-CN.md)

This repository hosts previews and a descriptive index of Publy's built-in article and image-card themes. The index is gallery data; it is not an installation registry, and the current Publy development CLI lists local themes without fetching it.

## Standalone article themes

Publy is preparing a content-only, versioned JSON bundle format for article themes. This feature is in the unreleased development candidate; check the [Publy user guide](https://github.com/turlamai/publy/blob/main/docs/USER-GUIDE.md) for what is available in the version you use. The gallery does not currently provide downloads, automatic updates, verified authors, or a signed catalogue. External card theme bundles are not supported by this format.

In a build that supports bundles, a theme author can validate and package scoped CSS with:

```sh
publy theme pack my.css --id my-style --theme-version 1.0.0 --name "My style" --license MIT --output my-style.json
```

Share the resulting file with its licence and a preview. A user can install a locally obtained bundle with `publy theme add ./my-style.json` and preview it with `publy theme preview my-style`. For an HTTPS file, `--sha256` must be supplied from a trusted independent source: the hash checks bytes, not author identity. Bundle validation accepts a restricted subset of CSS scoped to `#publy`; it does not execute theme packages.

The external submission process and gallery distribution are not open yet. Do not submit npm packages as theme bundles.
