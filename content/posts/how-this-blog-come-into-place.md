+++
title = 'How This Blog Come Into Place'
date = 2024-03-29T21:47:26+08:00
tldr = 'yet another blog setup guide'
description = 'setup a blog on your machine & GitHub'
tags = ['manual']
+++

# I need a blog
- my choice is [HUGO](https://gohugo.io/)
    - `brew install hugo` or [else](https://gohugo.io/installation/)
        - smoke test `hugo version`
        - init blog `hugo new site ${your_blog_name}`
        - cd to your blog's directory
        - `git init` let Git be in charge of current folder's history
        - add the theme you like, I like `archie` theme
          - `git submodule add https://github.com/athul/archie.git themes/archie`
        - config via `hugo.toml`
          - add the above you just install `echo "theme = 'archie'" >> hugo.toml`
          - light & dark mode
          - subtitle for your blog
        - up & run `hugo server`
        - all blogs go in `content/posts` directory, [see](https://gohugo.io/getting-started/quick-start/#add-content)
          - `hugo new content posts/${name-for-your-post}.md`

<!-- references links -->
<!-- upload to github -->
<!-- add github actions -->