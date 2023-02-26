---
date: 2023-02-24
description: "A lesson on Static Site Generators and Hugo"
featured_image: "http://localhost:1313/images/postBG9.jpg"
tags: ["webdev"]
title: "How did we make this site? pt 1"
disable_share: false
---

## What is a Static Site Generator?

A static site generator is a tool that takes a set of files and generates a static website from them. The files are usually written in a markup language like Markdown or HTML. The generator then takes these files and generates a website from them. The website is then hosted on a web server. The website is easily updated by simply updating the files and re-running the generator.

## Why use a Static Site Generator?

There are many reasons to use a static site generator. The main reason is that it is easy to update. Students, mentors and others can now easily update the website by simply updating the content files and re-running the generator. This is much easier than having to update the website directly. While we have historically used web development as a way to teach CSS, HTML and JS to our team, it slows down the process of updating the website year after year. It also makes it easier for new students to get involved with the website.

## What is Hugo?

Hugo is a static site generator written in Go. Sites made with Hugo will be based off of a theme. The theme is a set of files that define the look and feel of the website. Hugo will take the content files and the theme and generate a static website. The websites files can be previewed locally before being uploaded to the web server. Hugo is a very popular static site generator and is used by many large companies. All of the content on this site is written in Markdown. A guide to Markdown can be found [here](https://www.markdownguide.org/).

## How do I use Hugo?

Hugo is a command line tool. To install Hugo, follow the instructions [here](https://gohugo.io/getting-started/installing/). Once Hugo is installed, you can run the following command to create a new site:

```bash
hugo new site mysite
```

This will create a new directory called `mysite` with the following structure:

```bash
mysite
├── archetypes
├── config.toml
├── content
├── data
├── layouts
├── static
└── themes
```

The `archetypes` directory contains templates for new content. The `config.toml` file contains the configuration for the site. The `content` directory contains the content for the site. The `data` directory contains data files that can be used in the site. The `layouts` directory contains the templates for the site. The `static` directory contains static files that will be copied to the output directory. The `themes` directory contains the themes for the site.

To add a theme to the site, run the following command:

```bash
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git /themes/ananke
```

This will add the theme to the `themes` directory. To use the theme, add the following to the `config.toml` file:

```toml
title = "Website name"
languageCode = "en-us"
theme = ["ananke"]
resourceDir = "../resources"

DefaultContentLanguage = "en"
SectionPagesMenu = "main"
Paginate = 3 # this is set low for demonstrating with dummy content. Set to a higher number
googleAnalytics = ""
enableRobotsTXT = true

[languages]
  [languages.en]
    title = "FRC 453 Website"
    weight = 1
    contentDir = "content/en"
    # languageDirection = 'rtl' for Right-To-Left languages

[sitemap]
  changefreq = "weekly"
  priority = 0.5
  filename = "sitemap.xml"

[params]
  text_color = ""
  author = ""
  favicon = "/images/favicon.ico"
  site_logo = "/images/banner1.png"
  # choose a background color from any on this page: https://tachyons.io/docs/themes/skins/ and preface it with "bg-"
  background_color_class = "bg-near-black"
  recent_posts_number = 3

[[params.ananke_socials]]
name = "twitter"
url = "https://twitter.com/urlName"
```

To add content to the site, run the following command:

```bash
hugo new post/article1.md
```

This will create a new file in the `content` directory. The file will have the following structure:

```markdown
---
title: "Article1"
date: 2023-02-24T15:25:00-05:00
draft: true
---

```

To preview the site, run the following command from the root directory of the site:

```bash
hugo server
```

This will start a local web server that will serve the site. The site can be accessed at `localhost:1313` from a web browser. At this point you should be able to see the site. To add content to the site, simply edit the files in the `content` directory. To update the site, simply run the following command:

```bash
hugo
```

This will generate the site and place the files in the `public` directory. The files in the `public` directory can then be uploaded to the web server.

## How can we adjust the theme?

The theme can be adjusted by editing the files in the `layouts` directory. The theme can also be adjusted by editing the files in the `themes` directory. You can create new 'partials' in your `layouts` directory and then use them in your `layouts` files. For example, you can create a new partial called `footer.html` in the `layouts/partials` directory. Then you can use the partial in the `layouts/_default/baseof.html` file by adding the following line:

```html
{{ partial "footer.html" . }}
```

This can also be used to add css and js files to the site. For example, you can add a css file to the site by adding the following line to the `layouts/_default/baseof.html` file:

```html
<link rel="stylesheet" href="/css/style.css">
```

This will add the `style.css` file to the site. You can also add js files to the site by adding the following line to the `layouts/_default/baseof.html` file:

```html
<script src="/js/script.js"></script>
```

This will add the `script.js` file to the site.

## What is the difference between a theme and a template?

A theme is a set of files that define the look and feel of the site. A template is a file that defines the layout of a page. A theme can contain multiple templates. For example, the `ananke` theme contains the following templates:

```bash
ananke
├── archetypes
├── assets
├── config.toml
├── content
├── data
├── layouts
├── LICENSE.md
├── README.md
├── resources
├── static
└── themes
```

The `ananke` theme contains the following templates:

```bash
layouts
├── _default
│   ├── baseof.html
│   ├── list.html
│   └── single.html
├── index.html
├── partials
│   ├── footer.html
│   ├── head.html
│   ├── header.html
│   ├── menu.html
│   ├── post.html
│   ├── post_meta.html
│   ├── post_nav.html
│   ├── post_summary.html
│   ├── post_tags.html
│   ├── post_title.html
│   ├── recent_posts.html
│   ├── scripts.html
│   └── social.html

```

The `baseof.html` file is the base template for the site. The `list.html` file is the template for the list of posts. The `single.html` file is the template for a single post. The `index.html` file is the template for the home page. The `partials` directory contains the partials that are used in the templates.

## Whats next?

Part 2 of this tutorial is [here](../ssglesson2/).

If you are interested in learning more about Hugo, you can check out the following resources:

* [Hugo Documentation](https://gohugo.io/documentation/)
* [Hugo Themes](https://themes.gohugo.io/)
* [Hugo Tutorials](https://gohugo.io/getting-started/quick-start/)
* [Hugo Tutorials on YouTube](https://www.youtube.com/results?search_query=hugo+ssg+tutorial)

### What are some other FRC sites that use Hugo?

* [FRC Zero](https://frczero.org)