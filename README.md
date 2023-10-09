<p align=center><b><a href="https://devcontainers.org/spec/">You're probably looking for devcontainers.org/spec 😉</a></b></p>

# Development Containers specification

💻 Formal specification for Development Containers

<p align="center">
  <img width="600" src="https://i.imgur.com/gGOKNZC.png" />
</p>

## Development

To get started, make sure you have [Bikeshed] installed, then run these commands
in **two separate terminals** (so that they're running simultaneously):

```sh
bikeshed watch
python -m http.server
```

<sup>If you're on Linux you can use the `&` operator</sup>

In VS Code you can click the <kbd>[|]</kbd> button in the terminal to split it
into two.

ℹ Bikeshed supports all of CommonMark, but not GFM. For instance, [tables must be
HTML `<table>` elements] instead of `|`-delimited Markdown tables. But don't let
that fool you! It's auto-linking features _vastly_ surpass plain Markdown. Make
sure you use `[=hello=]` to autolink to `<dfn>hello</dfn>`!

If you want to add a big text minimap marker, do this:

```html
<!-- Big Text: My new section -->

# My new section
```

```sh
bikeshed source --big-text
```

<!-- prettier-ignore-start -->
[Bikeshed]: https://speced.github.io/bikeshed/
[tables must be HTML `<table>` elements]: https://github.com/speced/bikeshed/issues/1128#issuecomment-388907059
<!-- prettier-ignore-end -->
