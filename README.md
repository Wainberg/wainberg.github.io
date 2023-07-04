# wainberglab.org
Lab website of the Wainberg Lab at the Prosserman Centre for Population Health 
Research. 

This site is based on the [template](https://github.com/znamlab/znamlab.github.io)
provided by the [Znamenskiy Lab](https://znamlab.org), which is itself largely 
based on the [template](https://github.com/mpa139/allanlab) provided by the 
[Allan lab](http://www.allanlab.org) and includes some code adapted from the website 
of the [Bedford lab](https://bedford.io). It is powered by 
[Jekyll](https://jekyllrb.com) and uses some [Bootstrap](http://www.getbootstrap.com), 
[Bootswatch](http://www.bootswatch.com), and [Font Awesome](https://fontawesome.com/). 
The website is hosted on GitHub Pages (https://pages.github.com/). 
Website source code is freely available under MIT License.

The home page image was generated with Midjourney (https://www.midjourney.com)
using the prompt "Human brain sprouting multiple DNA double helix --aspect 885:309".
Each image on the Research page was generated using the corresponding heading as the 
prompt, with --aspect 4:3.

## Modifying the website
You can make edits to the website either directly on Github or by cloning the
repo, editing it on your local machine, and then pushing the changes. The latter
approach is recommended as it lets you preview any changes that you've made
before updating the public website. To do that you will need to install
[Jekyll](https://jekyllrb.com/).

Once you have Jekyll setup, simply navigate to the
repo directory in terminal and type `bundle exec jekyll serve`, which will
build the site and start a local HTTP server so that you can view it in your
browser.

## Updating your personal info
You will find your personal page under `people/_posts`. The file name should start
with your start date in the lab - this is to ensure that lab members appear on
the team page in order of joining.

The lab member files have the following header format:

```
---
layout: member
title: Firstname Lastname
photo: Firstname.jpg
info: Group Leader
email: your.email@website.org
github: github_username
twitter: twitter_username
scholar: "https://scholar.google.com/citations?user=qwertyuiop"
link_to_page: yes
---
```

Any of the fields except `title` and `info` can be omitted or left blank, in which
case the relevant item wont appear on the website. If you omit `link_to_page`
or leave it blank, the [people page](https://wainberglab.org/people/) won't link to 
your personal page.

Photos should be square and placed under `images/members` in the repo.
