---
layout: docs-index
title: Enso Developer Documentation
title: README
tags: [summary, readme]
order: 0
---

# Enso Documentation
This site contains the documentation for the two major sub-projects of Enso, the engine, and the IDE.

- [Engine](./enso)
- [IDE](./ide)
- [Rust-Libs](./rust-lib)

## Contributing to the Docs

### Installation and Usage

The site is built with Jekyll, and hosted on GitHub Pages. The content is mostly hosted in other repositories via Git submodules.

```markdown
bundle install
git submodule update --init --recursive
bundle exec jekyll build
```

### Adding New Documentation

To add new documentation:

- Add a new submodule under `_submodules`.
- Create a symlink to the desired repository at the root.
- To the target repository, add a [GitHub Action](https://github.com/luna/enso/blob/main/.github/workflows/docs.yml) to automatically checkout the submodule when changes are made.
- If you want fine-grained control over presentation and order of the documents, you can [add a yaml frontmatter block](https://jekyllrb.com/docs/front-matter/) to your files. See the [engine docs](https://github.com/luna/enso/blob/main/docs/enso-philosophy.md) for an example.

### Deploying to enso.org

The docs are deployed to enso.org via the `docs-publish.yml` GitHub Action. They get put in the `docs/developer` subfolder of the `gh-pages` branch. This gets deployed alongside the other enso docs pages.

### Attribution & License

This site uses the [Gitbook](https://github.com/sighingnow/jekyll-gitbook) Jekyll theme, by [sighingnow](https://github.com/sighingnow).
