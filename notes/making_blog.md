## How I Made This Blog

# Setup
I first followed:
- [Getting Started with Github Pages](https://guides.github.com/features/pages/)

After that I got my site up and running at my domain:
[dataontherocks](https://jeffery-do.github.io/)

I wanted a better theme so I looked here:
- [Adding a Jekyll theme to your GitHub Pages site](https://help.github.com/articles/adding-a-jekyll-theme-to-your-github-pages-site/)

But I'm not familiar with Ruby, so I didn't know what a Gemfile was.
I decided to look at this:
- [What is a Gemfile](http://tosbourn.com/what-is-the-gemfile/)

Humm, it looks like I need to install bundler, and jekell to get the control that I want.
- [Setting up your GitHub PAges site locally with Jekyll](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/)

Since I use Macos, I had to refer to this to update Ruby:
Oh, and additionally while installing bundler, apparently it required a newer version of bash:
- [Related Github Issue](https://github.com/Homebrew/homebrew-core/issues/5799)
- [Setup Ruby On Rails on macOS 10.12 Sierra](https://gorails.com/setup/osx/10.12-sierra) I actually didn't set up Rails here. I added rbenv, and set my global ruby to 2.4.0..

**Actually, ignore the theme parts below, as I was unable to actually get the below to work. It appears that gitpages has the jekyll repos on their side of their servers. As such, if you wish to just use, `theme: beautiful-jekyll-theme`, it won't work.
I chose a nice theme from [jekyll-theme search](https://rubygems.org/search?utf8=%E2%9C%93&query=jekyll-theme).**
I then proceeded to follow more of the setup github pages with jekyll page.

my Gemfile ended up being:
``` ruby
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
gem 'beautiful-jekyll-theme'
```

I followed that by doing
``` bash
bundle install
```
