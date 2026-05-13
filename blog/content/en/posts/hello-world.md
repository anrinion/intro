---
date: '2026-05-13T12:34:33+02:00'
draft: false
title: 'Hello World!'
---
Testing Hugo for static site rendering.

As I'm considering starting a blog, looking for something more advances than my simple self-written setup. For cost and time efficiency, the hosting remains on Cloudflare Pages, which means I'm limited to static content.

Hugo randomly poped out in the search results, and looks pretty promising, so I'm giving it a try.

### Log / How-To:

- install Hugo (Windows, other platforms [here](https://gohugo.io/installation/))
```
winget install Hugo.Hugo.Extended
```
- run Hugo to create project structure
```
hugo new project blog --format yaml
```
- Select a theme [here](https://themes.gohugo.io). I selected PaperMod, added it as submodule
```
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git blog/themes/PaperMod
```
- set `theme: ["PaperMod"]` in `hugo.yaml`
- configure everything in `hugo.yaml` (using [sample](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation#sample-hugoyml))
- start live server to preview changes
```
hugo server --buildDrafts
```
- move existing static content (images) to `blog/static`
- move robots.txt to `blog/layouts/robots.txt`
- re-create existing static pages as markdown (one page in my case, `blog/content/about.md`) or as posts.
- change Cloudflare deployment settings: build command `hugo`, root directory `blog`, build output `public`
- set `HUGO_VERSION` variable to `0.161.1` (my current Hugo version; the point is to set the minimum required version as Cloudflare's default is too old)

## Resources:
- [Hugo Quick Start](https://gohugo.io/getting-started/quick-start/)
- [Theme (Hugo PaperMode)](https://github.com/adityatelange/hugo-PaperMod)
- A nice [walkthrough](https://janneaa.com/posts/creating-a-blog-with-hugo-and-cloudflare-pages/) on how to start from scratch and host on Cloudflare Pages.
