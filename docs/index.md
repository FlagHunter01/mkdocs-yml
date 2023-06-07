---
title: Setup guide and propotype
description: Quick reference page that helps setting up  Material for MkDocs and using advanced markdown functionnalities
icon: material/test-tube
status: new
subtitle: Good luck.
---

# Setup guide and reference

## Setup

!!! info "Announcement bar"
    [Read this](https://squidfunk.github.io/mkdocs-material/setup/setting-up-the-header/#announcement-bar) for announcement bars!

### Dependancies

For better performance and to avoid compatibility issues, install the lates [Python]()

```title="Installing dependancies"
pip install pillow cairosvg
apt install libcairo2-dev libfreetype6-dev libffi-dev libjpeg-dev libpng-dev libz-dev
apt install pngquant
pip install mkdocs-rss-plugin
pip install mkdocs-git-committers-plugin-2
pip install mkdocs-git-revision-date-localized-plugin
pip install mkdocs-glightbox
```


### GitHub Pages

### YAML for VSCode

## Reference

### Admonition

!!! note "Title"
    Body

    !!! note "Nested note"
        Body

!!! note ""
    Title delete

!!! note "Body delete"

??? note "Collapsible note"
    This is invis by default.

???+ note "Collapsible expanded note"
    This is vis by default but can be hidden.

!!! note inline "Inline"

Text

!!! note inline end "Inline end"

Text

!!! note

!!! abstract

!!! info 

!!! tip

!!! success

!!! question

!!! warning

!!! failure

!!! danger

!!! bug

!!! example

!!! quote

### Annotations

Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
{ .annotate }

1.  :man_raising_hand: I'm an annotation! (1)
    { .annotate }

    1.  :woman_raising_hand: I'm an annotation as well!

Those can go in admonitions, content tabs of anything else. 

### Buttons

[Primary button](#){ .md-button .md-button--primary }
[Pesant button](#){ .md-button }
[:rocket:](#){ .md-button }

### Code 

`#!python inline()`

```py title="python block" linenums="1" hl_lines="3 4"
# (1)!
import ExternalFile as ef

if 1 + 1 != 3:
    material_is_best = true
```
1. The `!` deletes the comment tag

### Content tabs

=== "Windows :windows:"

    Windows

=== "Linux :linux:"

    Linux

### Tables

| Number | Description | Comment |
|:---:|:---|---:|
1| Banana | Yellow

[Also take a look at this](https://squidfunk.github.io/mkdocs-material/reference/data-tables/#import-table-from-file)

### Footnotes

Text[^1]

[^1]: I'm a footnote

### Formatting

{--deleted--}
{++added++}
{~~1~>One~~}
{==highlight==}
{>>Comment<<}
{^^Inserted^^}
{~~deleted~~}

{==

    Works with blocks

==}

H~2~0
x^2^

++ctrl+alt+del++

### Grids

<div class="grid cards" markdown>

- :fontawesome-brands-html5: __HTML__ for content and structure
- :fontawesome-brands-js: __JavaScript__ for interactivity
- :fontawesome-brands-css3: __CSS__ for text running out of boxes
- :fontawesome-brands-internet-explorer: __Internet Explorer__ ... huh?

</div>



<div class="grid cards" markdown>

-   :material-clock-fast:{ .lg .middle } __Set up in 5 minutes__

    ---

    Install [`mkdocs-material`](#) with [`pip`](#) and get up
    and running in minutes

    [:octicons-arrow-right-24: Getting started](#)

-   :fontawesome-brands-markdown:{ .lg .middle } __It's just Markdown__

    ---

    Focus on your content and generate a responsive and searchable static site

    [:octicons-arrow-right-24: Reference](#)

-   :material-format-font:{ .lg .middle } __Made to measure__

    ---

    Change the colors, fonts, language, icons, logo and more with a few lines

    [:octicons-arrow-right-24: Customization](#)

-   :material-scale-balance:{ .lg .middle } __Open Source, MIT__

    ---

    Material for MkDocs is licensed under MIT and available on [GitHub]

    [:octicons-arrow-right-24: License](#)

</div>
<div class="grid cards" markdown>

-   :material-clock-fast:{ .lg .middle } __Set up in 5 minutes__

    ---

    Install [`mkdocs-material`](#) with [`pip`](#) and get up
    and running in minutes

    [:octicons-arrow-right-24: Getting started](#)

-   :fontawesome-brands-markdown:{ .lg .middle } __It's just Markdown__

    ---

    Focus on your content and generate a responsive and searchable static site

    [:octicons-arrow-right-24: Reference](#)

-   :material-format-font:{ .lg .middle } __Made to measure__

    ---

    Change the colors, fonts, language, icons, logo and more with a few lines

    [:octicons-arrow-right-24: Customization](#)

-   :material-scale-balance:{ .lg .middle } __Open Source, MIT__

    ---

    Material for MkDocs is licensed under MIT and available on [GitHub]

    [:octicons-arrow-right-24: License](#)

</div>

<div class="grid" markdown>

:fontawesome-brands-html5: __HTML__ for content and structure
{ .card }

:fontawesome-brands-js: __JavaScript__ for interactivity
{ .card }

:fontawesome-brands-css3: __CSS__ for text running out of boxes
{ .card }

> :fontawesome-brands-internet-explorer: __Internet Explorer__ ... huh?

</div>

### Images

![Image title](https://dummyimage.com/600x400/eee/aaa){ align=left }

<figure markdown>
  ![Image title](https://dummyimage.com/600x400/){ width="300" }
  <figcaption>Image caption</figcaption>
</figure>

![Image title](https://dummyimage.com/600x400/){ loading=lazy }

### Lists

 - A
 - B
 - C

1. A
2. B
    1. C
    2. D

`Lama`

:   Fine creature from Earth

`Zerg`

:   Lame parasite from Char

 - [x] A
 - [ ] B

### Tooltips

[Hover me](https://example.com "I'm a tooltip!")

:material-information-outline:{ title="Important information" }

The HTML specification is maintained by the W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium


