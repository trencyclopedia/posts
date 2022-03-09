---
layout: post
title: "post workflow"
date: 2022-01-31
categories: programing
tags: jekyll front-end 
author: Eric
mathjax: true
---
* content
{:toc}


This ariticle will describe the template and workflow used to setup this post website. Specifically, it includes:
- jekyll
- directory layout
- [HyG](https://gaohaoyang.github.io/) theme
- key features




## jekyll
Generally speaking, [Jekyll ](https://jekyllrb.com/)is the tool to transform your markdown posts into a static website, by adding necessary components (e.g. html, css, directory structure) from built-in templates. This tool is also recommended by github to build [github pages](https://pages.github.com/)  for blogging. It has some free themes and simplify the process to create a website especially for novice people like me.  Besides, it is also possible to design and customize the theme if you are familiar with HTML and CSS, so it is flexible and extensible.  

### My learning process
I have a electrical engineering backgound with some hands-on programming skills like C, Python, git.  My initial purpose was to just create my personal website,  and then maybe add a few more project websites later. And I started to learn the tool by following some examples( [JMcGlone]([jmcglone.com](http://jmcglone.com/ "jmcglone.com")),  ), then tried to tune and tailor the template to my own  needs by twitching the codes patch by patch while I was learning the syntax of html and css. In this way, I created my first github website in two months. As I became more familiar with the programing languages, I started to learn and use more advanced templates and themes ([MkDocs](https://www.mkdocs.org), [sphinx](https://www.sphinx-doc.org/en/master/),[HyG](https://gaohaoyang.github.io/) ) , then I build up another three project websites using these templates in less than a month. 

### Jekyll workflow

In this section, I will briefly descibe the workflow to use jekyll, launch a website locally on your computer and remotelly on github. 

#### 1. Install ruby and jekyll environment

To test your webiste locally on your computer and ensure there is nothing wrong before pushing to the github., you should install ruby environment and jekyll. 

The Windows users can directly use [RubyInstaller](http://rubyinstaller.org/) to install ruby environment. Follow the prompts while installing.

Then install jekyll using this command:

```
gem install jekyll
```

For more details, you can view the jekyll official website.

#### 2. Create/clone a template website 

You can either create a new website using the built-in templates of jekyll or clone a customized jekyll website elsewhere:

##### A. Use the commands below to create and launch a new jekyll website:
``` 
jekyll new my-awesome-site
cd my-awesome-site 
jekyll serve ##launch it locally
```

##### B. Clone the theme code elsewhere

if you find a good template on github, you can also use it as a starting point.

For example, you can clone [HyG](https://gaohaoyang.github.io/) , which is a jekyll website cusomized for hosting posts. 
```
clone https://github.com/Gaohaoyang/gaohaoyang.github.io.git renamed_folder
cd renamed_folder
jekyll serve ##launch it locally

```

#### 3. Customize a template website
Depending on which template you choose, you may have to change different parts of the code. Nonetheless, there is a big chance that they will share many common structures.  I give one example below. 
#####  Add new posts on a jekyll website:
A basic jekyll website has a [directory structure](https://jekyllrb.com/docs/structure/) like this:
```
.
├── _config.yml
├── _data
│   └── members.yml
├── _drafts
│   ├── begin-with-the-crazy-ideas.md
│   └── on-simplicity-in-technology.md
├── _includes
│   ├── footer.html
│   └── header.html
├── _layouts
│   ├── default.html
│   └── post.html
├── _posts
│   ├── 2007-10-29-why-every-programmer-should-play-nethack.md
│   └── 2009-04-26-barcamp-boston-4-roundup.md
├── _sass
│   ├── _base.scss
│   └── _layout.scss
├── _site
├── .jekyll-cache
│   └── Jekyll
│       └── Cache
│           └── [...]
├── .jekyll-metadata
└── index.html # can also be an 'index.md' with valid front matter

```
you can put your posts into the \_posts folder and the name of post files should follow  the format: `YEAR-MONTH-DAY-title.MARKUP`.

A more detailed examplaintion fo these different files/folders and their functions can be accessed here: https://jekyllrb.com/docs/structure/


#### 4. Launch locally and push to Github

After you have made some changes, you can see their effects by lauch your webiste locally first using this command:
```
jekyll serve
```

Then if satisfied, you can push it to your Github repository. 
Note that Github has two kinds of gitpages: one for your personal/company website, project websites;

Each account can only have one personal/company website，and it should use your account name as your repository. You should push it to the remote master branch. 

Nonetheless， you can create many project  websites, and you should push it to the remote gh-pages branch. 



## key features of [HyG](https://gaohaoyang.github.io/) theme

### Home

Index page show 5 posts excerpt as a default. Readers can click article title or read more button to see full post. There are recent posts area, categories area and tags area at the right part of the index page. You can also add an area at this part, if you change the file `index.html`.

### Archives

Archive post according to the year.

### Categories

Show posts according to the category.

### Tags

Show posts according to the tags.

### Collections

The user can collect their favorite article links with `markdown` syntax.

### Comments

This theme supports both [disqus](https://disqus.com/) and [多说评论 duoshuo comments](http://duoshuo.com/). It's very easy to config your comments module.

### Post Contents

The post contents is fixed at the right side while page is scrolling. There will be a scroll bar on contents while it is outside the window height.