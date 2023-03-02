# quarto-ankivalenz

A [Quarto extension](https://quarto.org/docs/extensions/) for rendering Quarto documents to HTML
that can be used with [Ankivalenz](https://github.com/vangberg/ankivalenz) to generate [Anki](https://apps.ankiweb.net/)
cards.

## Installation

Install the extension to your Quarto project:

```bash
quarto add vangberg/quarto-ankivalenz
```

Create an Ankivalenz configuration file:

```bash
ankivalenz init
```

### Quarto Document

Set the `format` metadata to `ankivalenz-html` in your document's YAML header:

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

The file will be rendered as `my-document.ahtml`. Add `"input_ext": "ahtml"` to
`ankivalenz.json`, and run Ankivalenz to generate an Anki deck:

```bash
ankivalenz run .
```

### Quarto Book

Add the `ankivalenz-html` format to your book's `formats` list in `_quarto.yml`:

```yaml
formats:
  ankivalenz-html: default
```

Add `input_ext` and `input_dir` to `ankivalenz.json`:

```json
{
  "deck_id": 123456789,
  "deck_name": "My Deck",
  "input_ext": "ahtml",
  "input_dir": "_book"
}
```

Render your book as usual:

```bash
quarto render my-book.qmd
```

Generate the Anki deck:

```bash
ankivalenz run .
```
