---
title: git & github
author: ben best | [ucsb data science](http://ucsb-data-science.github.io/)
date: 2015-07-16 | [bbest.github.io/ds-git](http://bbest.github.io/ds-git)
---

# introduction

## outline

1. introduction
    - why bother?
    - workflow
    - fork & pull model
    - github features

1. exercises
    1. hello world
        - `http://github.com/[user]/hello-world`
    1. create a website repo
        - `http://[user].github.io`
    1. fork & pull a repo
        - `stevejbrown/rss_article_recommender`

## why bother?
- **backup** to offsite archive (ie github.com)
- **rewind** changes (ie versioned files)
- **document** file changes with issues and messages
- **collaborate** with others
- **publish** to free web site

## example workflow
1. **sign up** at github.com _(1x/user)_
1. **install** git _(1x/machine)_
1. **create** [or **fork**] a repository, aka "repo" _(1x/repo)_
1. **clone** from web to your local desktop _(1x/repo)_
1. [**branch** copy for isolated development of a feature _(1x/feature)_
1. **commit** changes locally
1. **push** changes to your repo
1. [**pull request** changes from your repo to source repo that was forked)]

## models of development

- **fork & pull**: open-source / big teams
    - fork a source repo (**read only**)
    - push changes to a personal repo
    - pull request to commit to a source repo

- **shared**: small teams
    - push changes directly to a repo (**read + write**)

- **branching**: sandbox changes with either of above modes
    - See [flow](https://guides.github.com/introduction/flow/)

## fork & pull model

|       | `github.com/[user0]/[repo]` <br> (orig, web)  | `github.com/[user]/[repo]` <br> (you, web) |   `~/github/[repo]` <br> (you, local) |
|-------|-----------------------------------------------|--------------------------------------------|---------------------------------------|
| <span  + class="mega-octicon octicon-arrow-right"></span> (1x) |         | <span  + class="mega-octicon octicon-arrow-right"></span> [**fork**](https://help.github.com/articles/fork-a-repo) <span  + class="mega-octicon octicon-repo-forked"></span> | <span  + class="mega-octicon octicon-arrow-right"></span> [**clone**](https://help.github.com/articles/fetching-a-remote) <span  + class="mega-octicon octicon-cloud-download"></span> |
| <span  + class="mega-octicon octicon-arrow-down"></span>   |                                               |          | <span  + class="mega-octicon octicon-arrow-down"></span> [**commit**](http://git-scm.com/docs/git-commit) <span  + class="mega-octicon octicon-git-commit"></span> |
| <span  + class="mega-octicon octicon-arrow-down"></span>   |                                               |          | <span  + class="mega-octicon octicon-arrow-down"></span> [**branch**](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/) <span  + class="mega-octicon octicon-git-branch"></span> |
| <span  + class="mega-octicon octicon-arrow-left"></span>    |                                               |             | <span  + class="mega-octicon octicon-arrow-left"></span> [**push**](https://help.github.com/articles/pushing-to-a-remote/) <span  + class="mega-octicon octicon-cloud-upload"></span> |
| <span  + class="mega-octicon octicon-arrow-left"></span>    | [**merge**](https://help.github.com/articles/merging-a-pull-request) <span  + class="mega-octicon octicon-git-merge"></span> | <span  + class="mega-octicon octicon-arrow-left"></span> [**pull request**](https://help.github.com/articles/creating-a-pull-request/) <span  + class="mega-octicon octicon-git-pull-request"></span> | |

where:

> - `[user0]` is the original user or organization
> - `[repo]` is a repository
> - `[user]` is your github username (eg `bbest`)

## github features

- track changes, issues, etc. free for public repos
- max: 1GB per repo, 100MB per file. so larger files (and binary) on file server, with remote vpn option
- render [markdown](https://guides.github.com/features/mastering-markdown/), eg `README.md`
- special rendering of various popular file formats (txt/md, png/jpg, csv/tsv, geojson/topojson) ...

## github rendering: text

**Track Changes** view with "Rendered" button to view differences between versions of a text file: additions in green, removals in red strikethrough. Details: [Rendering differences in prose documents](https://help.github.com/articles/rendering-differences-in-prose-documents/)

![Source](./fig/github_rendered_bar_sized.png)

![Rendered](./fig/github_rendered_text_sized.png)

## github rendering: images

**Image** view show differences in 3 ways: 2-up, swipe and onion skin views. Details: [Rendering and diffing images](https://help.github.com/articles/rendering-and-diffing-images/)

![Onion Skin](https://help.github.com/assets/images/help/repository/images-onion-view.gif)

## github rendering: csv

**CSV** view allow for on the fly tabular view, searching for text, and linking to specific rows of data. Details: [Rendering CSV and TSV data](https://help.github.com/articles/rendering-csv-and-tsv-data/).

![select rows, URL to select](https://camo.githubusercontent.com/e3ee38c92016c9efc4e6694cf2f6edf6c4d28f12/68747470733a2f2f662e636c6f75642e6769746875622e636f6d2f6173736574732f3238323735392f3937363436342f33363064646537342d303638642d313165332d393363632d6138623465333930353236352e676966)

![search](https://camo.githubusercontent.com/04fd5aead6d72487c8616d4a8799497beb774016/68747470733a2f2f662e636c6f75642e6769746875622e636f6d2f6173736574732f3238323735392f3937363436332f33343839626230652d303638642d313165332d383132312d3863386133303733386461372e676966)

## github rendering: geo

**Geographic** view of GeoJSON or topojson files render automatically as a map. Details: [Mapping geoJSON files on GitHub](https://help.github.com/articles/mapping-geojson-files-on-github/)

<script src="https://embed.github.com/view/geojson/datasets/geodata/master/topojson/us_states.topojson"></script>
interactive map with zoom, click on details, [OpenStreetMap](http://www.openstreetmap.org)

# exercises

## ex 1: hello world

<span class="mega-octicon octicon-mark-github"></span>  Create a hello-world repository and tour some of Github's most useful features. You only need a web browser and Github account (no git or other desktop software required).

1. [Sign up](https://help.github.com/articles/signing-up-for-a-new-github-account/) for a new GitHub account

1. Follow the GitHub Guide [Hello World](https://guides.github.com/activities/hello-world/) to walk through essentials of: repositories, branches, commits, issues and pull requests.

## ex 2: create a website repo

<span class="mega-octicon octicon-file-code"></span> Create a website repository in Github.  You only need a web browser and Github account (no git or other desktop software required).

1. [Create repo](https://help.github.com/articles/create-a-repo/) `[user].github.io`, where `[user]` is your github username
    - [Commit your first change](https://help.github.com/articles/create-a-repo/#commit-your-first-change) on README.md
1. [Create pages](https://help.github.com/articles/creating-pages-with-the-automatic-generator/)
    - Have fun picking a theme!

- This is how we created the website for the **ucsb-data-science**:
    - _edit_: [github.com/ucsb-data-science/ucsb-data-science.github.io](https://github.com/ucsb-data-science/ucsb-data-science.github.io)
    - _view_: [ucsb-data-science.github.io](http://ucsb-data-science.github.io)

## ex 3: fork & pull a repo

<span class="mega-octicon octicon-repo-forked"></span> Fork the repo [stevejbrown/rss_article_recommender](https://github.com/stevejbrown/rss_article_recommender).

1. [Set up git](https://help.github.com/articles/set-up-git/) if you haven't already
    - git + github applications recommended
1. [Fork the repo](https://help.github.com/articles/fork-a-repo/)
    1. Fork this repository: [https://github.com/stevejbrown/rss_article_recommender](stevejbrown/rss_article_recommender)
    1. Clone your forked repo to your desktop
        ```bash
        mkdir ~/github
        cd ~/github
        git clone https://github.com/[user]/rss_article_recommender.git
        cd rss_article_recommender
        ```
    1. Edit files. For the sake of testing, create a new file `[user].txt` where `[user]` is your Github username. We'll start with each of us editing different files so as to avoid [merge conflicts](https://help.github.com/articles/resolving-merge-conflicts/).
    1. [Commit](https://guides.github.com/activities/forking/#making-changes) changes and push

# extra

## md to html slideshow

This presentation was created in markdown (see [index.md](https://github.com/bbest/ds-git/blob/gh-pages/index.md)) and rendered as an HTML slideshow with [pandoc](http://pandoc.org). Details: [Producing slide shows with Pandoc](http://pandoc.org/demo/example9/producing-slide-shows-with-pandoc.html). To render the HTML, the content was placed in the **gh-pages** branch of the [ds-git](https://github.com/bbest/ds-git) repo.

Here's some code to get the idea:

```bash
# clone "ds-git" repository made on github.com to local machine
cd ~/github
git clone https://github.com/bbest/ds-git.git

# create new "gh-pages" branch
cd ds-git
git checkout -b gh-pages

# create document index.md in editor like http://atom.io

# convert from markdown (*.md) to html slidy with options
pandoc \
  -t slidy \
  --self-contained --incremental --slide-level=2 \
  --css=octicons/octicons.css \
  index.md \
  -o index.html

# check status, note untracked files
git status

# add files for git tracking, and commit changes locally
git add *
git commit -a -m 'initial presentation'

# push to remote, set upstream (1x)
git push -u origin gh-pages

# push (after 1x)
git push
```

To see all the pandoc options:

```bash
pandoc --help
```

Also [set the default branch](https://help.github.com/articles/setting-the-default-branch/) to gh-pages, since master not otherwise being used.

## further resources

- [Good Resources for Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)
    - [GitHub Guides](https://guides.github.com/)
        - [Making Your Code Citable](https://guides.github.com/activities/citable-code/)
- [Git and GitHub with RStudio](http://r-pkgs.had.co.nz/git.html)
