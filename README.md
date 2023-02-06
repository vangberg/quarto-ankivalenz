# <%= title %> Format

## Installing

```bash
quarto add vangberg/quarto-ankivalenz
```

This will install the extension.

## Using

Set the `format` metadata to `ankivalenz` in your document's YAML header:

```yaml
---
title: "My Document"
format:
  ankivalenz-html: default
---
```

Render your document as usual:

```bash
quarto render my-document.qmd
```

The output will be a HTML file, that can be used with [Ankivalenz](https://github.com/vangberg/ankivalenz).
