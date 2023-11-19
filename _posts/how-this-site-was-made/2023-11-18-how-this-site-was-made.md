---
layout: post
title: How this site was born 👶
date: 2023-11-18
tags: [github actions, ruby]
categories: project
---

#### TLDR;

The website was made using Jekyll an open source static website generator, and a simple theme, [klisé](https://github.com/piharpi/klise).

The source code for my site was placed on my [github](https://github.com/jeffmur/dev) repository and [github pages](https://pages.github.com/) for hosting the website. For deployments, I wrote a [workflow](https://github.com/jeffmur/dev/blob/main/.github/workflows/gh-pages.yml) that deploys an artifact, static files, to github-pages.

The domain is owned through [domains.google.com](https://domains.google.com/), now owned by Squarespace. The CNAME, jeffur.dev, points to jeffmur.github.io and static IP addresses where the static website is hosted.

<hr>

### Getting Started 🚀

So, before we start create a site, you need some tools, you can self paced for how to installing each tools, on this guide i'm just want to show you how to install jekyll and deploying to github pages.

#### Prerequisites

Requirements before we doing magic show .

- [Ruby](https://www.ruby-lang.org/en/downloads/) programming language; [gem](https://rubygems.org/) package manager
- [Bundler](https://bundler.io)
- [Github](https://github.com) account and [Git](https://git-scm.com) (version control)
- [Domain](https://domains.google.com) (optional)

### Installation

First, you need a static site generator, [SSG](https://www.staticgen.com/), there are many kinds, but I'm using Jekyll. For Windows, good luck 🤞. 

For Linux + MacOS, use your terminal:

```bash
$ gem install bundler # may need sudo
$ bundle install jekyll # installing jekyll in your machine
$ jekyll new my-site && cd my-site # create new jekyll project
$ bundle exec jekyll serve --force_polling # run jekyll server with live updates
```

Now, jekyll is running on your local machine, open your browser and go to `localhost:4000` is default address from jekyll, press <kbd>CTRL</kbd> + <kbd>C</kbd> to stop the jekyll server.

#### Adding remote repository

Before we adding remote repository, you must have [github](https://github.com/new) repository, or you can fork my [repository](https://github.com/jeffmur/dev/fork).

Once you have a repository setup, add github remote address to your working directory, with the following commands:

```bash
$ git init # initializing project folder
$ git remote add origin git@github.com:USERNAME/REPO.git
$ git add -A && git commit -m "init" && git push -u origin main # push code to github
```

Now check your github repository, make sure the files is uploaded correctly.

#### Deploying to gitub-pages

With a public repository, private github-pages requires a Pro github account, you'll need to [create](https://docs.github.com/en/actions/deployment/targeting-different-environments/using-environments-for-deployment#creating-an-environment) a deployment enviornment before the github action will run:

1. Select "New environment" -> Name: "github-pages"
2. Add protection rule for your "main" branch
3. Update [gh-pages.yaml](https://github.com/jeffmur/dev/blob/main/.github/workflows/gh-pages.yml#L40C7-L40C31) environment url to point to your github pages domain, not mine.

```yaml
environment:
    name: github-pages
    url: ${{ steps.deployment.outputs.page_url }}
```

4. Optional, setup a custom domain with any provider, and update [github-pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)


