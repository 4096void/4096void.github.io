---
layout: default
---

## Way too easy, man.

### Local setup.
```bash
# Maybe U need 2 install ruby first.
gem install jekyll bundler
jekyll new blog
cd blog
bundle exec jekyll serve
# Now open localhost:4000 in your browser.

# Switch to a new terminal tab.
# Add jekyll-theme-minimal to Gemfile.
# Modify _config.yml's theme to jekyll-theme-minimal.
# Install jekyll-theme-minimal.
# Now refresh your browser, you'll see it.
```

### Put into repository.
```bash
git init
# Add _site, .sass-cache, .jekyll-metadata, *.gem and Gemfile.lock
emacs .gitignore
git add --all
git commit -m 'blog init'

# Create username.github.io with your Github account.
# Sync our newly created repository to Github.
git remote add origin git@github.com:yourname/yourname.github.io
```
