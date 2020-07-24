---
layout: post
title: Add a Fancier Theme To Your GitHub Account
---

So, you're tired of the basic GitHub Pages theme and you want something more
exciting. Using a third party jekyll theme from websites like

- [jekyllthemes.io/](https://jekyllthemes.io/)
- [jekyll-themes.com](https://jekyll-themes.com/)
- or others from a [full list](https://jekyllrb.com/docs/themes/)

require something a bit more complicated than GitHub, but in essence it just
involves adding a couple of lines of code.

1. Open
 - ``_config.yml``
 - ``Gemfile``
2. In ``_config.yml``

```yml
remote-theme: [github-organization]/[theme-name]
```
3. In ``Gemfile`` replace everything with

```ruby
source 'https://rubygems.org'

# gem 'jekyll', '3.8.5'
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
 gem 'jekyll-remote-theme'

end
```
