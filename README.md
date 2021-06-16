# thoughts

> A collection of my thoughts and longer-form writings.

## Setup

```
brew install pandoc
brew install pandoc-sidenote
```

## Using

You might have to `dropbox stop` on Linux for inotify problems.

```
bundle exec jekyll serve --drafts

bundle exec octopress new draft my-slug

bundle exec jekyll build
bundle exec octopress publish

bundle exec octopress new page
```
