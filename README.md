# Ingenuous

A simple [Hexo](https://hexo.io/) theme for engineering blogs based on a brand new default theme [Landscape](https://github.com/hexojs/hexo-theme-landscape).

[Demo](http://chopschips.net/)

* Optimized mobile layout that to show more information in narrow display.
  * Most of changes of layout are intended to fit with engineering blogs.
* Added link to scroll to widget in mobile nav.
* Added shared counts display at each post header.
* Added Hatena Bookmark(social bookmark service in Japan) button and remove some buttons in share tags.
* Added about widget to sidebar.
* Added pagination in archives page.
* Supported keywords meta tag in front-matter(just for compatibility to octopress: even maybe legacy feature ;-)
* Supported TOC(table of contents) insertion to article. (enable in front-matter)
* Removed top banner and modified layout only a little.
* Be able to disable searh form by _config.yml.

## Installation

### Install

``` bash
$ git clone https://github.com/kwhrtsk/hexo-theme-ingenuous.git themes/ingenuous
```

**Ingenuous requires Hexo 2.4 and above.**

### Enable

Modify `theme` setting in `_config.yml` to `ingenuous`.

### Update

``` bash
cd themes/ingenuous
git pull
```

## Configuration

``` yml
# Header
menu:
  Home: /
  Archives: /archives
rss: /atom.xml

# Content
excerpt_link: Read More
fancybox: true

# Sidebar
sidebar: right

# Search form
search: true

widgets:
- about
- category
- tag
- tagcloud
- archives
- recent_posts

# Miscellaneous
google_analytics:
google_adsense:
favicon: /favicon.png
twitter:
google_plus:

aboutme:
about:
  author: true
  twitter: true
  aboutme: true
  description: true

common_keywords:
```

These are default values.

If you want to override in your settings, you must add settings to your `_config.yml` like the followings:

```
theme_config:
  rss: /feed.xml
  fancybox: false
```

**NOT LIKE THIS:**

```
rss: /feed.xml
fancybox: false
```

### Configuration Items

- **menu** - Navigation menu
- **rss** - RSS link
- **excerpt_link** - "Read More" link at the bottom of excerpted articles. `false` to hide the link.
- **fancybox** - Enable [Fancybox]
- **sidebar** - Sidebar style. You can choose `left`, `right`, `bottom` or `false`.
- **search** - Enable or disable search form.
- **widgets** - Widgets displaying in sidebar
- **google_analytics** - Google Analytics ID
- **google_adsense** - Google Adsense script tags to put into head
- **favicon** - Favicon path
- **twitter** - Twiiter ID
- **google_plus** - Google+ ID
- **aboutme** - Text to display on about widget
- **about** - Enable switches for contents in about widget
- **common_keywords** - Default keywords included in keyword meta tag. (typically, blog title and author)

## Features

### Fancybox

Ingenuous uses [Fancybox] to showcase your photos. You can use Markdown syntax or fancybox tag plugin to add your photos.

```
![img caption](img url)

{% fancybox img_url [img_thumbnail] [img_caption] %}
```

### Sidebar

You can put your sidebar in left side, right side or bottom of your site by editing `sidebar` setting.

Ingenuous provides 6 built-in widgets:

- about
- category
- tag
- tagcloud
- archives
- recent_posts

All of them are enabled by default. You can edit them in `widget` setting.

## Development

### Requirements

- [Grunt] 0.4+
- Hexo 2.4+

### Grunt tasks

- **default** - Download [Fancybox] and [Font Awesome].
- **fontawesome** - Only download [Font Awesome].
- **fancybox** - Only download [Fancybox].
- **clean** - Clean temporarily files and downloaded files.

[Hexo]: http://zespia.tw/hexo/
[Fancybox]: http://fancyapps.com/fancybox/
[Font Awesome]: http://fontawesome.io/
[Grunt]: http://gruntjs.com/
[Landscape]: https://github.com/hexojs/hexo-theme-landscape
