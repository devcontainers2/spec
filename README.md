# Development Containers specification

💻 Formal specification for Development Containers

<p align=center>
  <img width=600 src="https://i.imgur.com/gGOKNZC.png">
</p>

👀 You might be looking for [devcontainers.org/spec]. 😉

A development container allows you to use a container as a full-featured
development environment. It can be used to run an application, to separate
tools, libraries, or runtimes needed for working with a codebase, and to aid in
continuous integration and testing.

The Development Containers Specification seeks to find ways to enrich existing
formats with common development specific settings, tools, and configuration
while still providing a simplified, un-orchestrated single container option – so
that they can be used as coding environments or for continuous integration and
testing.

The first format in the specification, `devcontainer.json`, was born out of
necessity. It is a structured JSON with Comments (jsonc) metadata format that
tools can use to store any needed configuration required to develop inside of
local or cloud-based containerized coding.

We envision that this same structured data can be embedded in images and other
formats – all while retaining a common object model for consistent processing.
For example, some of this same metadata can be added to a
`devcontainer.metadata` image label to tie settings directly to a container
image.

Beyond repeatable setup, these same development containers provide consistency
to avoid environment specific problems across developers and centralized build
and test automation services. You can use the [open-source CLI reference
implementation] either directly or integrated into product experiences to use
the structured metadata to deliver these benefits. It currently supports
integrating with Docker Compose and a simplified, un-orchestrated single
container option – so that they can be used as coding environments or for
continuous integration and testing.

A GitHub Action and an Azure DevOps Task are available in [devcontainers/ci] for
running a repository's dev container in continuous integration (CI) builds. This
allows you to reuse the same setup that you are using for local development to
also build and test your code in CI.

You may also review proposed references in the
[proposals folder](https://github.com/devcontainers/spec/tree/main/proposals).

The icon for [@devcontainers] is from the [Fluent icon library].

## Contributing and Feedback

If you are interested in contributing, please check out the
[How to Contribute](contributing.md) document or
[start a discussion](https://github.com/devcontainers/spec/discussions).

Please report issues in the following repositories:

<!-- prettier-ignore -->
- Reference implementation Features and templates: [devcontainers/features](https://github.com/devcontainers/features), [devcontainers/templates](https://github.com/devcontainers/templates)
- CLI reference implementation and non-spec related feature requests: [devcontainers/cli](https://github.com/devcontaineres/cli)
- GitHub Action and Azure DevOps Task: [devcontainers/ci](https://github.com/devcontainers/ci)

## Development

To get started, make sure you have [Bikeshed] installed, then run these commands
in **two separate terminals** (so that they're running simultaneously):

```sh
bikeshed watch
python -m http.server 8000
```

In VS Code you can click the <kbd>[|]</kbd> button in the terminal to split it
into two.

ℹ Bikeshed supports all of CommonMark, but not GFM. For instance, [table must be
HTML `<table>` elements] instead of `|`-delimited Markdown tables. But don't let
that fool you! It's auto-linking features _vastly_ surpass plain Markdown. Make
sure you use `[=hello=]` to autolink to `<dfn>hello</dfn>`!

<!-- prettier-ignore-start -->
[devcontainers.org/spec]: https://devcontainers.org/spec
[Bikeshed]: https://speced.github.io/bikeshed/
[table must be HTML `<table>` elements]: https://github.com/speced/bikeshed/issues/1128#issuecomment-388907059
[open-source CLI reference implementation]: https://github.com/devcontainers/cli
[devcontainers/ci]: https://github.com/devcontainers/ci
[@devcontainers]: https://github.com/devcontainers
[Fluent icon library]: https://github.com/microsoft/fluentui-system-icons/blob/master/assets/Cube/SVG/ic_fluent_cube_32_filled.svg
<!-- prettier-ignore-end -->
