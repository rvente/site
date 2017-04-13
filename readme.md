## agenda

* add a ton of articles in
* For reference, I plan to upload this to `/guide/`
* ~add opinion and sports sections in the sidebar and to the homepage~
* add the sidebar to the section page
* ~complete the front page for all of the section categories~

## Adding a post

Adding a new article is done in three easy steps:

1. Go to [`/ink/docs/_posts`](https://github.com/tblslatineer/ink/tree/master/docs/_posts) by clicking that link.
2. Title your new article using the format `yyyy-mm-dd-postname.md.` d is the day, m is the month, y is the year. **this is important because the page won't accept changes if the date is wrong** If the date is only in single digits, supply a leading zero. eg. `2017-04-03` is April 3rd 2017. This part is important as the posting date is needed by the site to know how to order things.
3. Paste in your text. No extra formatting is needed. If you do want to know how to make your articles pop with meaningful formatting, you can learn about [Markdown](#markdown) later in this document. Then, scroll to the bottom and hit `commit.` Your entire article will propogate through in about 5 minutes.

---

All posts go in `/ink/docs/_posts` regardless of category. They should be files with the `.md` suffix. Each post gets one file each file gets one post. The name of the file should be the current date with dashes as separators. eg `2010-02-05-post-name.md`

## Authors

The [authors page](https://github.com/tblslatineer/ink/blob/master/docs/_data/authors.yml) is what gives pages with a defined author a unique sidebar entry, not just the default latineer one.

[Here](https://github.com/tblslatineer/blob/master/docs/.docs/09-authors.md) are the guidlines.

## Front Matter

This is what the website uses to organise everything. Copy it into the *begining* of the document before anything else.

```
---
title: "Post title"
excerpt: "a short sentence that describes the subject matter"
modified: 2016-11-03T11:12:40-04:00
categories:
  - features
  - news
  - entertainment
  - sports
  - opinion
author: FIRSTNAME  LASTNAME as defined in /_data/authors.yml
---
```
## Markdown

Markdown is the name of the language you will use to write content in this website. [Here](https://tblslatineer.github.io/ink/markup/markup-html-tags-and-formatting/) is what all of the levels are and how they actually look on the site.

You can see the complete guide [here](https://github.com/tblslatineer/ink/blob/master/docs/_posts/2013-01-11-markup-html-tags-and-formatting.md). But for immediate reference:

```
## Title / Header

paragraph *italic* **bold** ***bold italic*** People think focus means saying yes to the thing you've got to focus on. But that's not what it means at all. It means saying no to the hundred other good ideas that there are. You have to pick carefully. I'm actually as proud of the things we haven't done as the things I have done. Innovation is saying no to 1,000 things.

Multi line blockquote with a cite reference:

> People think focus means saying yes to the thing you've got to focus on. But that's not what it means at all. It means saying no to the hundred other good ideas that there are. You have to pick carefully. I'm actually as proud of the things we haven't done as the things I have done. Innovation is saying no to 1,000 things.

<cite>Steve Jobs</cite> --- Apple Worldwide Developers' Conference, 1997
{: .small}
```
renders to

## Title / Header

paragraph *italic* **bold** ***bold italic*** People think focus means saying yes to the thing you've got to focus on. But that's not what it means at all. It means saying no to the hundred other good ideas that there are. You have to pick carefully. I'm actually as proud of the things we haven't done as the things I have done. Innovation is saying no to 1,000 things.

Multi line blockquote with a cite reference:

> People think focus means saying yes to the thing you've got to focus on. But that's not what it means at all. It means saying no to the hundred other good ideas that there are. You have to pick carefully. I'm actually as proud of the things we haven't done as the things I have done. Innovation is saying no to 1,000 things.

<cite>Steve Jobs</cite> --- Apple Worldwide Developers' Conference, 1997
{: .small}


## Structure 

This describes the structure of the site. If you need to find a file, there's no need to dig for it in the folders.

```
/ink/docs
├── _data                      # data files for customizing the theme
|  ├── authors.yml             # define each author and their side bar
|  ├── navigations.yml         # main navigation links
|  └── ui-text.yml             # text used throughout the theme's UI
├── _includes
|  ├── analytics-providers     # snippets for analytics (Google and custom)
|  ├── comments-providers      # snippets for comments (Disqus, Facebook, Google+, and custom)
|  ├── footer                  # custom snippets to add to site footer
|  ├── head                    # custom snippets to add to site head
|  ├── base_path               # site.url + site.baseurl shortcut
|  ├── feature_row             # feature row helper
|  ├── gallery                 # image gallery helper
|  ├── group-by-array          # group by array helper for archives
|  ├── nav_list                # navigation list helper
|  ├── toc                     # table of contents helper
|  └── ...
├── _layouts
|  ├── archive-taxonomy.html   # tag/category archive for Jekyll Archives plugin
|  ├── archive.html            # archive listing documents in an array
|  ├── compress.html           # compresses HTML in pure Liquid
|  ├── default.html            # base for all other layouts
|  ├── home.html               # home page
|  ├── single.html             # single document (post/page/etc)
|  └── splash.html             # splash page
├── _sass                      # SCSS partials
├── assets
|  ├── css
|  |  └── main.scss            # main stylesheet, loads SCSS partials from _sass
|  ├── fonts
|  |  └── fontawesome-webfont  # Font Awesome webfonts
|  ├── images                  # image assets for posts/pages/collections/etc.
|  ├── js
|  |  ├── plugins              # jQuery plugins
|  |  ├── vendor               # vendor scripts
|  |  ├── _main.js             # plugin settings and other scripts to load after jQuery
|  |  └── main.min.js          # optimized and concatenated script file loaded before </body>
├── _config.yml                # site configuration
├── Gemfile                    # gem file dependencies
├── index.html                 # paginated home page showing recent posts
└── package.json               # NPM build scripts
```

