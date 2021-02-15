---
layout: post
title:  "How to Start a Blog or Personal Website Using Jekyll and GitHub Pages"
categories: [ tutorial ]
tags: [ blogging ]
image: assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages.jpg
description: "How to Start a Blog or Personal Website Using Jekyll and GitHub Pages"
featured: true
hidden: true
comments: false
---

At the end of this guide you will have a personal website or blog that looks something like [this](https://lenpaul.github.io/Lagrange/). It will be under a unique domain name and you will have complete control over your site.

This guide will walk you through the process from beginning to end of creating your GitHub account, choosing a Jekyll theme, making changes to your Jekyll theme, adding blog posts, and publishing your site through your own domain. Programming ability is not required for this guide.

For an introduction to Jekyll and GitHub Pages, please check out [the previous post in this series]({% post_url 2021-02-16-the-ultimate-guide-to-managing-a-personal-website-or-blog-with-jekyll-and-github-pages %}).

#### Create a GitHub account

In order to get your Jekyll site hosted on GitHub Pages, you will need to create a GitHub account if you don't have one already. Navigate to [GitHub](https://github.com/) and click on "Sign Up" at the top right to create your account. [The free pricing plan](https://github.com/pricing) is more than enough for our purposes.

![GitHub Home Page]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-1.png" }})

#### Create a Repository on GitHub

Once you are logged into your GitHub account, you can create the repository that will contain your Jekyll site. You can do that by navigating to [this link](https://github.com/new) or clicking on the dropdown menu at the top right of any page when you are logged into GitHub and clicking on "New Repository".

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-2.png" }})

You will need to name your repository `<username>.github.io`, where `<username>` is your GitHub username. For example, my GitHub username is `lenpaul`, and I would name the repository `lenpaul.github.io`. Ensure that your repository is public. Once created, your repository should be empty.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-3.png" }})

#### Find a Jekyll Theme

Jekyll has a massive community of Jekyll fanatics that create their own themes. There are [plenty of professional looking themes that you can use completely for free](https://jekyllrb.com/docs/themes/). For this guide, we will be using [Lagrange](https://lenpaul.github.io/Lagrange/), my own Jekyll theme that I created that is currently my most popular.

![Lagrange Screenshot]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-4.png" }})

However, this guide will work the same for any Jekyll theme that is hosted on GitHub with a working demo. Usually, when  you find a theme on one of the sites that showcases Jekyll themes, they will have links to the GitHub repository and the live demo of the Jekyll theme.

![Jekyll Theme]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-5.png" }})

For example, [Michael Rose of Made Mistakes](https://mademistakes.com/) has release several amazing Jekyll themes. As long as they have their own [GitHub repository](https://github.com/mmistakes/jekyll-theme-basically-basic), and there is a [live demo](https://mmistakes.github.io/jekyll-theme-basically-basic/) of the theme, this guide will work for that theme.

#### Import Your Jekyll Theme

The Jekyll theme that you choose should have a GitHub repository that you can find and download. For this guide, you can find the GitHub repository for Lagrange [here](https://github.com/LeNPaul/Lagrange). Once you have found the GitHub repository, you will want to download a ZIP of the repository by clicking on the green "Code" button at the top right of the repository and clicking on "Download ZIP".

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-6.png" }})
