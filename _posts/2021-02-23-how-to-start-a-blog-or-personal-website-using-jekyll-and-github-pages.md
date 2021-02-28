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

At the end of this guide you will have a personal website or blog that looks something like [this](https://lenpaul.github.io/Lagrange/). It will be under a unique domain name, and you will have complete control over your site.

This guide will walk you through the process from beginning to end of creating your GitHub account, choosing a Jekyll theme, making changes to your Jekyll theme, and adding publishing blog posts. Programming ability is not required for this guide.

For an introduction to Jekyll and GitHub Pages, please check out [the previous post in this series]({% post_url 2021-02-16-the-ultimate-guide-to-managing-a-personal-website-or-blog-with-jekyll-and-github-pages %}).

### Table of Contents

1. [Create a GitHub account](#create-a-github-account)

2. [Install GitHub Desktop](#install-github-desktop)

3. [Create a Repository on GitHub](#create-a-repository-on-github)

4. [Find a Jekyll Theme](#find-a-jekyll-theme)

5. [Import Your Jekyll Theme](#import-your-jekyll-theme)

6. [Enable GitHub Pages](#enable-github-pages)

7. [Personalize Your Site](#personalize-your-site)

8. [Publish Blog Posts](#publish-blog-posts)

9. [Conclusion](#conclusions)

10. [FAQ](#faq)

#### Create a GitHub account

In order to get your Jekyll site hosted on GitHub Pages, you will need to create a GitHub account if you do not have one already. Navigate to [GitHub](https://github.com/) and click on "Sign up" at the top right to create your account. [The free pricing plan](https://github.com/pricing) is more than enough for our purposes.

![GitHub Home Page]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-1.png" }})

#### Install GitHub Desktop

[GitHub Desktop](https://desktop.github.com/) allows you to interface with your GitHub repositories without having to use the command line. We will be using GitHub Desktop to import our Jekyll theme make changes to the site, and publish blog posts.

Once you have [downloaded and installed GitHub Desktop](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/installing-github-desktop), navigate to the "Preferences" screen and ensure that you are logged into your GitHub account.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-7.png" }})

#### Create a Repository on GitHub

Once you are logged into your GitHub account, create the repository that will contain your Jekyll site by navigating to [this link](https://github.com/new) or clicking on the dropdown menu at the top right of any page while logged into GitHub and clicking on "New repository".

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-2.png" }})

You will need to name your repository `<username>.github.io`, where `<username>` is your GitHub username. For example, since my GitHub username is `lenpaul`, I would name my repository `lenpaul.github.io`.

Ensure that your repository is public. All of the checkboxes under "Initialize this repository with" should also be unchecked. Once created, your repository should be empty.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-3.png" }})

The next step is to set up your repository on your local computer. If your repository is empty, then you can do that by clicking on "Set up in Desktop" while in your repository.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-9.png" }})

If you end up with files in your repository, then you can set up your repository on your local computer by clicking on the green "Code" button and clicking "Open with GitHub Desktop".

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-10.png" }})

Choose a directory that you would like to use to store your repository on your computer and click "Clone".

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-11.png" }})

#### Find a Jekyll Theme

Jekyll has a massive community of Jekyll fanatics that create their own themes. There are [plenty of professional looking themes that you can use for free](https://jekyllrb.com/docs/themes/). For this guide, we will be using [Lagrange](https://lenpaul.github.io/Lagrange/), my own Jekyll theme that I created that is currently my most popular.

![Lagrange Screenshot]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-4.png" }})

However, this guide will work the same for any Jekyll theme that is hosted on GitHub with a working demo. Usually, when  you find a theme through one of the recommended [Jekyll theme showcase sites](https://jekyllrb.com/docs/themes/), they will have links to the GitHub repository and a live demo of the Jekyll theme.

![Jekyll Theme]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-5.png" }})

For example, [Michael Rose of Made Mistakes](https://mademistakes.com/) has released several amazing Jekyll themes. As long as they have their own [GitHub repository](https://github.com/mmistakes/jekyll-theme-basically-basic), and there is a [live demo](https://mmistakes.github.io/jekyll-theme-basically-basic/) of the theme, this guide will work for that theme.

#### Import Your Jekyll Theme

The Jekyll theme that you choose should have a GitHub repository that you can find and download. For this guide, you can find the GitHub repository for Lagrange [here](https://github.com/LeNPaul/Lagrange). Once you have found the GitHub repository, you will want to download a ZIP of the repository by clicking on the green "Code" button at the top right of the repository and clicking on "Download ZIP".

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-6.png" }})

Once you have downloaded your repository ZIP, you can go ahead and unzip that file to get your Jekyll site files. They should look something like the following.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-8.png" }})

Copy all of these files, and paste them to [the directory that you had created on your local computer with GitHub Desktop when you created your repository](#create-a-repository-on-github). When you view your repository on GitHub Desktop, it should look something like the following.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-12.png" }})

In the bottom left, add a summary of your commit and click the "Commit to master" button. You may also need to click on "Publish Branch" after.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-13.png" }})

Once that has been done, your repository on GitHub should no longer be empty and should have the Jekyll theme files that we had imported.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-14.png" }})

#### Enable GitHub Pages

Now that you have your Jekyll theme imported to your repository, you will need to enable GitHub Pages to get your site running. Navigate to the settings page for your repository, and scroll down to the "GitHub Pages" section. Under "Source", select the "master" branch, ensure that "/(root)" is selected, and click "Save".

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-15.png" }})

Refresh the page, and you should see that your site is ready to be published at a URL. You may need to wait a few minutes before your site is available, but if you click on that URL, you will [see your site in action](https://lenpaul.github.io/Lagrange/).

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-16.png" }})

#### Personalize Your Site

You should now have [a site running that is powered by Jekyll and GitHub Pages](https://lenpaul.github.io/Lagrange/). The next step is to begin personalizing your site.

By default, your Jekyll theme will have a `_config.yml` file that contains general configurations such as the title of your site and the name of the author. You can change this by navigating to that file in your GitHub repository, and clicking on the pencil icon, which will allow you to edit the `_config.yml` file.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-17.png" }})

Change some configuration parameters such as the title and the description, and commit your change. Your change should take effect after a few minutes.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-18.png" }})

#### Publish Blog Posts

Although you can just as easily add blog posts through GitHub like we did above, we will go through the steps of publishing blog posts using GitHub Desktop.

Using your text editor of choice (in this case I am using [Atom](https://atom.io/)), navigate to your Jekyll repository. There will be a directory called `_posts`. This is where all of your blog posts will be placed. Usually, there will be a few sample posts that you can use as a starting point.

Open up one of the sample posts, add your own content, and save your changes.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-19.png" }})

Once you have your first blog post saved, open up GitHub Desktop and navigate to your Jekyll repository. It should show you what files you had just changed.

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-20.png" }})

GoCommit those changes, and push those changes to your GitHub repository by clicking on "Push origin".

![GitHub Adding New Repository]({{ site.baseurl }}{{ "/assets/images/how-to-start-a-blog-or-personal-website-using-jekyll-and-github-pages-21.png" }})

After a few minutes, your blog post should show up on your site.

#### Conclusion

Congratulations, you have started a blog using Jekyll and GitHub Pages! For now, we are sticking to [updating some configurations](#personalize-your-site) for your Jekyll site and [publishing blog posts](#publish-blog-posts). Check out the article on *[How to Customize a Jekyll Theme]()* for more details on how to fully customize your Jekyll site, such as using a custom domain name, and changing the look of your site.

#### FAQ

##### My site URL looks different from yours

If you name your repository `<username>.github.io`, then your URL will be `https://<username>.github.io`. If you name your repository anything else, then your URL will be `https://<username>.github.io/<repository name>`.

##### The Jekyll theme I like doesn't have a GitHub repository.

Jekyll themes that you find from any of the sites linked on the [Jekyll documentation site](https://jekyllrb.com/docs/themes/) should have a GitHub repository referenced. If you are unable to find one, it may not be compatible with GitHub Pages.

##### Do I need to learn how to program to work with Jekyll and GitHub Pages?

If you are content with using a Jekyll theme as-is, you do not need to learn how to program. Even making basic changes to your theme does not require advanced programming ability. You can get by just fine with the steps outlined in this guide, and you will be able to customize pages and publish blog posts.
