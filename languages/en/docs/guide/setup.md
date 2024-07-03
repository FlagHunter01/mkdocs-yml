---
title: Setup
description: Setting up Material for Mkdocs Insiders
---

## Preface

Please keep in mind that the official documentation at [squidfunk.github.io/mkdocs-material/](https://squidfunk.github.io/mkdocs-material/) is way better and should be used instead of this. 

Only use this guide if you want to have a working example to copy-paste once you understand the real documentation.

!!! warning "Insiders paid version" 
    This guide only works with [Material Insiders](https://squidfunk.github.io/mkdocs-material/insiders/)

!!! info "Environment"
    **This guide is for self-hosting on Linux.** For other hosting and deployment options, please refer to [the offical doc](https://squidfunk.github.io/mkdocs-material/getting-started/) once again. 

## Preparing the environment

### Downloads

Here are all the downloads you'll need to do.

```
apt install python3 libcairo2-dev libfreetype6-dev libffi-dev libjpeg-dev libpng-dev libz-dev pngquant
pip install "mkdocs-material[imaging]"
pip install mkdocs-rss-plugin
pip install mkdocs-git-committers-plugin-2
pip install mkdocs-git-revision-date-localized-plugin
pip install mkdocs-glightbox
```

### Material for Mkdocs Insiders

Aquire Material for Mkfocs insiders. 
The post-bill GitHub page along [this one](https://squidfunk.github.io/mkdocs-material/insiders/access-management/) should have all the information you need. 

Once you're done, proceed with [Getting started with Insiders](https://squidfunk.github.io/mkdocs-material/insiders/getting-started/). 

## Using Mkdocs

### linux commands

It's extemely simple !

First, create a new project:

```
mkdocs new my-project
cd my-project
```

Inside the new folder, you will find the basic layout of an Mkdocs project. 

This is where you can copy-paste my template (cloneable from [https://github.com/FlagHunter01/mkdocs-yml.git](https://github.com/FlagHunter01/mkdocs-yml.git)).

In order to preview your site, use the following command and go to [localhost:8000](http://localhost:8000):

```
mkdocs serve
```

Once ou're done, generate the HTML with:

```
mkdocs buid
```

The code will be availible at `\site\`. 

### VSCode

If you are using [Visual Studio Code](https://code.visualstudio.com/), you can add two modules that will greatly enhance your experience.

#### TODO Highlight v2

Download TODO Highlight v2 to highlight all the `TODO:` tags in my files. It's an easy way to keep in mind all the options that need to be customized befor you start writing your documentation.

#### YAML by RedHat

Download YAML by RedHat and paste the following in the JSON settings in order to have the official Material for Mkdocs debug:

```json
{
    "yaml.schemas": {
        "https://squidfunk.github.io/mkdocs-material/schema.json": "mkdocs.yml"
    },
    "yaml.customTags": [ 
        "!ENV scalar",
        "!ENV sequence",
        "tag:yaml.org,2002:python/name:material.extensions.emoji.to_svg",
        "tag:yaml.org,2002:python/name:material.extensions.emoji.twemoji",
        "tag:yaml.org,2002:python/name:pymdownx.superfences.fence_code_format"
    ]
}
```

## Using markdown

Here are some basics of markdown. 

```md
Text

*Italic*

**Bold**

# Main title (1 per doc)

## Title

### Subtitle

[Link](http://url.com)

![Image](images/cat.png)

| Table | Example |
|-------|---------|
| 1     | Banana  |
| 2     | Apple   |
```

!!! example "Output"
    Text

    *Italic*

    **Bold**

    # Main title (1 per doc)

    ## Title

    ### Subtitle

    [Link](http://url.com)

    ![Image](images/cat.png)

    | Table | Example |
    |-------|---------|
    | 1     | Banana  |
    | 2     | Apple   |
