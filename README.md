---
layout: docs-index
title: README
tags: [readme]
order: 0
---

# Enso Documentation

This site hosts the internal documentation for developers working on Enso and Enso projects. Most of the documentation is currently drawn from the [Enso engine](https://github.com/enso-org/enso/tree/main/docs).

If you want to add documentation for another project, see the instructions below.

## Installation and usage

The site is built with Jekyll, and hosted on GitHub Pages. The content is mostly hosted in other repositories via Git submodules.

```markdown
bundle install 
git submodule update --init --recursive
bundle exec jekyll build
```

## Adding new documentation

To add new documentation:

- Add a new submodule under `_submodules`.
- Create a symlink to the desired repository at the root.
- To the target repository, add a [GitHub Action](https://github.com/luna/enso/blob/main/.github/workflows/docs.yml) to automatically checkout the submodule when changes are made.
- If you want fine-grained control over presentation and order of the documents, you can [add a yaml frontmatter block](https://jekyllrb.com/docs/front-matter/) to your files. See the [engine docs](https://github.com/luna/enso/blob/main/docs/enso-philosophy.md) for an example.

## Deploying to enso.org

## Attribution & License

This site uses the [Gitbook](https://github.com/sighingnow/jekyll-gitbook) Jekyll theme, by [sighingnow](https://github.com/sighingnow).
