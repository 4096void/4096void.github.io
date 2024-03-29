+++
title = 'How This Blog Come Into Place'
date = 2024-03-29T21:47:26+08:00
tldr = 'yet another blog setup guide'
description = 'setup a blog at local & on GitHub'
tags = ['manual']
+++

## What if you need a blog
- my choice is HUGO
  - write blog(s) at local
    - `brew install hugo` or [else](https://gohugo.io/installation/), smoke test `hugo version`
    - find a place to init your blog `hugo new site ${your_blog_name}`, then `cd` into it
    - let Git be in charge of your blog history `git init`
    - create `.gitignore` and add `public` which built content stored within
    - [find a theme you like](https://themes.gohugo.io/), I like `archie` and download it
      - `git submodule add https://github.com/athul/archie.git themes/archie`
    - `touch hugo.toml` to config: [see]()
      - theme `echo "theme = 'archie'" >> hugo.toml`
      - light & dark mode
      - subtitle of your blog
      - blabla ...
    - checkout our blog at local `hugo server`
    - [all blogs stored in "content/posts" directory](https://gohugo.io/getting-started/quick-start/#add-content)
      - create blog with date comes in place via cli `hugo new content posts/${name-for-your-post}.md` with `date`
      - write down your thought
  - upload to Github
    - create a Github repo, matching against `${your_GH_name}.github.io`
    - push to Github
      - `git remote add origin git@github.com:${your_GH_name}/${your_GH_name}.github.io.git`
      - `git branch -M main`
      - `git push -u origin main`
    - add workflow
      - goto `https://github.com/${your_GH_name}/${your_GH_name}.github.io/settings/pages`'s Build and deployment section, select source as `Github Actions`
    - create `.github/workflows/hugo.yaml` with content from [hosting & deploy on Github](https://gohugo.io/hosting-and-deployment/hosting-on-github/)'s Step 6
    - commit hugo.yaml with msg "add workflow"

## references
- HUGO https://gohugo.io/
- HUGO installation https://gohugo.io/installation/
- HUGO themes https://themes.gohugo.io/
- HUGO add content https://gohugo.io/getting-started/quick-start/#add-content
- GitHub Pages https://pages.github.com/
- Host on GitHub Pages https://gohugo.io/hosting-and-deployment/hosting-on-github/
- Configure your GitHub repo build & deployment source at https://github.com/${your_GH_name}/${your_GH_name}.github.io/settings/pages (which need to replace with your GitHub acountname first)