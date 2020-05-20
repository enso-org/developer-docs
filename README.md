# Enso Documentation

This site hosts the internal documentation for developers working on Enso and Enso projects. Most of the documentation is currently drawn from the [Enso engine](https://github.com/luna/enso/tree/master/docs). 

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
- To the target repository, add a [GitHub Action](https://github.com/luna/enso/blob/master/.github/workflows/docs.yml) to automatically checkout the submodule when changes are made. 