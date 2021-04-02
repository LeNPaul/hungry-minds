---
layout: post
title:  "How to Customize a Jekyll Theme"
categories: [ tutorial ]
tags: [ blogging ]
image: assets/images/how-to-customize-a-jekyll-theme.jpg
description: "How to Customize a Jekyll Theme"
featured: false
hidden: false
comments: false
---

This guide outlines how to fully customize your Jekyll site. It includes all of the common changes that are typically made, such as how to use your own custom domain name when hosting your Jekyll site on GitHub Pages, to more complicated changes to the look of your site.

For an introduction to Jekyll and GitHub Pages, please check out the *[The Ultimate Guide to Managing a Personal Website or Blog with Jekyll and GitHub Pages]({% post_url 2021-02-16-the-ultimate-guide-to-managing-a-personal-website-or-blog-with-jekyll-and-github-pages %})*.

For a guide on how to start a blog or personal website using Jekyll and GitHub pages, please check out *[How to Start a Blog or Personal Website Using Jekyll and GitHub Pages]({% post_url 2021-02-23-how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages %})*.

### Table of Contents

1. [Using a Custom Domain Name](#using-a-custom-domain-name)

2. [Changing Fonts](#changing-fonts)

3. [Using Google Fonts](#using-google-fonts)

4. [Changing Colours](#changing-colours)

5. [Adding New Pages](#adding-new-pages)

6. [Changing Page and Post Layouts](#changing-page-and-post-layouts)

7. [Modifying Menu Layouts](#modifying-menu-layouts)

8. [Troubleshooting Build Errors](#troubleshooting-build-errors)

#### Using a Custom Domain Name

By default, when you set up a Jekyll site hosted on GitHub Pages, GitHub will provide your site with a unique URL. If you name your repository `<username>.github.io`, then your URL will be `https://<username>.github.io`. If you name your repository anything else, then your URL will be `https://<username>.github.io/<repository name>`.

GitHub Pages allows you to bring your own domain name and host your Jekyll site through that domain name. The way that this is achieved is dependent on what your domain name provider is. The following is a list of tutorials for using a custom domain name from popular domain name providers:

1. [Namecheap](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages/)

2. [GoDaddy](https://jinnabalu.medium.com/godaddy-domain-with-github-pages-62aed906d4ef)

3. [AWS Route 53](https://benwiz.com/blog/deploy-github-pages-with-aws-route-53-and-https/)

#### Changing Fonts

Most Jekyll themes do not directly provide a means to change fonts and colours. However, because we have direct access to the CSS files, we are able to change many style attributes, such as font.

Within a Jekyll theme, there are typically multiple font families used, such as one for titles, headings, and body text. The easiest way to find where the font families are set is by doing a global search on you Jekyll theme files (I am using [Atom](https://atom.io/) here):

![Changing Fonts]({{ site.baseurl }}{{ "/assets/images/how-to-customize-a-jekyll-theme-1.png" }})

You can change the font family for the different components of your Jekyll theme (here, `html` refers to the default font, and `h1, h2, h3, h4, h5, h6` refers to the headings font):

![Changing Fonts]({{ site.baseurl }}{{ "/assets/images/how-to-customize-a-jekyll-theme-2.png" }})

#### Using Google Fonts

[Google Fonts](https://fonts.google.com/) is a popular source of fonts that are used by many Jekyll themes. From the home page, choose a font that you would like to use, and select all of the styles that you need (you will usually need a regular, bold, an italicized style). Once you have your font styles selected, on the top right, there is a menu that you can click on that will slide out:

![Changing Fonts]({{ site.baseurl }}{{ "/assets/images/how-to-customize-a-jekyll-theme-3.png" }})

On the right slide-out menu, copy the code snippet into the `<head>` of your html. In most Jekyll themes, the best place to place this will be in the `_layouts/default.html` file:

![Changing Fonts]({{ site.baseurl }}{{ "/assets/images/how-to-customize-a-jekyll-theme-4.png" }})

#### Changing Colours

Similar to changing fonts, we are able to change the colour of many elements of Jekyll themes by changing the CSS files. To find where the change can be made, right-click on any element of your Jekyll theme that you would like to change the colour of, and click on "Inspect". On Google Chrome, this will bring up Chrome DevTools, which will show where in the CCS file the styling of the element comes from:

![Changing Colours]({{ site.baseurl }}{{ "/assets/images/how-to-customize-a-jekyll-theme-5.png" }})

#### Adding New Pages

Besides the home page and posts, most Jekyll themes have additional pages such as "Contact" and "About" pages. You can also add additional pages by adding markdown files in the root directory of your Jekyll theme, with `layout: page` at the top:

![Adding New Pages]({{ site.baseurl }}{{ "/assets/images/how-to-customize-a-jekyll-theme-6.png" }})

You can then access these pages with the URL `<site baseurl>/<filename>`. If you place your markdown files in a directory, then the URL will be `<site baseurl>/<directory name>/<filename>`.

#### Modifying Page and Post Layouts

Every Jekyll theme should have three layouts, a `default.html`, `page.html`, and `post.html` layout. The default layout is the base layout that the page and post layouts are built on. Pages typically do not have a date associated with them and are used for pages such as "Contact" and "About" pages, and posts are used for blog posts that have a date associated. Typically, you may want to modify the `post.html` layout if you want to change how your blog posts look. The following are some examples of changes you may want to make:

##### Showing Date Published

The following code snippet is an example on how to show the date that a post was published:

```
{% raw %}<span class="post-date">Published on {{ page.date | date: "%B %-d, %Y" }}</span>{% endraw %}
```

##### Showing Related Posts

The following code snippet is an example on how to show the top three related posts to the current blog post:

```
{% raw %}<div class="related">
  <h2>Related Posts</h2>
  <ul class="related-posts">
    {% for post in site.related_posts limit:3 %}
      <li>
        <h3>
          <a href="{{ site.baseurl }}{{ post.url }}">
            {{ post.title }}
            <small>{{ post.date | date_to_string }}</small>
          </a>
        </h3>
      </li>
    {% endfor %}
  </ul>
</div>{% endraw %}
```

#### Modifying Menu Layouts

Jekyll themes typically have some kind of menu or navigation bar. This is usually defined as an "includes" component in the `_includes` directory. For example, it may be called `_includes/sidebar.html`. Depending on the theme, the menu elements in the sidebar may be hard coded, or it may be configured in a yaml file somehwere. In this case, the menu items are configured in the `_data/settings.yml` file. Combined with [adding new pages](#adding-new-pages), you can create a wide variety of menu pages.

![Modifying Menu Layouts]({{ site.baseurl }}{{ "/assets/images/how-to-customize-a-jekyll-theme-7.png" }})

#### Troubleshooting Build Errors

Whenever you make a change to your Jekyll site and push that change to GitHub Pages, your Jekyll site will be rebuilt. Occassionally, you will come across a build error indicating that there was an error due to a change that you had made. You will usually be sent an email, and if you look at your commit on GitHub there will be a red sign indicating a build error:

![Troubleshooting Build Errors]({{ site.baseurl }}{{ "/assets/images/how-to-customize-a-jekyll-theme-8.png" }})

Unfortunately, the error log that is sent in these emails is usually not very helpful. To mitigate build errors, you should make changes to your site with your Jekyll site running locally so that any errors will be caught immediately. If you come across a build error, compare your previous commit with the changes that you had made.
