# jakecurran Theme

[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)][LICENSE]

Zola theme for personal website and blog, [jakecurran.com].

![Theme Screenshot](./screenshot.png)

## Contents

- [Usage](#usage)
- [Options](#options)

## Usage

Requirements:

- Zola >= 0.7

First download this theme to your themes directory:

```bash
$ cd themes
$ git clone https://github.com/jakecurran/jakecurran-theme.git
```

and then enable it in your `config.toml`:

```toml
theme = "jakecurran"
```

## Options

### Navigation Bar

Set a field in `extra` with a key of `jakecurran_menu`:

```
[extra]
jakecurran_menu = [
    { name = "Home", url = "$BASE_URL" },
    { name = "Blog", url = "$BASE_URL/blog" },
]
```

Each link needs to have a `url` and a `name`.

### KaTeX math formula support
This theme contains math formula support using KaTeX, which can be enabled by
setting `katex_enable = true` in the extra section of `config.toml`:

```toml
[extra]
katex_enable = true
```

After enabling this extension, the katex short code can be used in documents:

- `{{ katex(body="\KaTeX") }}` to typeset a math formula inlined into a text,
  similar to `$...$` in LaTeX
- `{% katex(block=true) %}\KaTeX{% end %}` to typeset a block of math formulas,
  similar to `$$...$$` in LaTeX

#### Automatic rendering without short codes

Optionally, `\\( \KaTeX \\)` inline and `\\[ \KaTeX \\]` / `$$ \KaTeX $$`
block-style automatic rendering is also supported, if enabled in the config:

```toml
[extra]
katex_enable = true
katex_auto_render = true
```

[LICENSE]: https://raw.githubusercontent.com/jakecurran/jakecurran-theme/master/LICENSE
[jakecurran.com]: https://jakecurran.com
