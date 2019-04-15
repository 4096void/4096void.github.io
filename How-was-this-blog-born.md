---
layout: default
---

## Way too easy, man.

### Local setup.
```bash
# Maybe you need to install Ruby first.

# Up an running.
gem install jekyll bundler
jekyll new blog
cd blog
bundle exec jekyll serve

# Open localhost:4000 to see your browser.

# Switch to a new tab.
# Add jekyll-theme-minimal to Gemfile.
# gem add jekyll-theme-minimal

# Modify _config.yml's to theme: jekyll-theme-minimal.
# Install jekyll-theme-minimal.
# bundle install
# Reload browser, you'll see it.
```

### Put into repository.
```bash
git init
# ignore these files or directories:
#   _site
#   .sass-cache
#   .jekyll-metadata
#   *.gem
#   Gemfile.lock
emacs .gitignore

# Create username.github.io github repository:
# Add origin.
git remote add origin git@github.com:yourname/yourname.github.io

# Push.
git add --all
git commit -m 'blog init'
git push origin master

# Goto https://yourname.github.io/
```
