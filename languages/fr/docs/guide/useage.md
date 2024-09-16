---
title: Utilisation
description: Cette page contient la plupart des options markdown offertes par Material Insiders. 
subtitle: Seulement pour Material for Mkdocs Insiders
---

## Metadonnées

Chaque page contient des données configurables, qui peuvent être définies comme suit:

```md
---
title: Utilisation
subtitle: Seulement pour Material for Mkdocs Insiders
description: Cette page contient la plupart des options markdown offertes par Material Insiders. 
status: new (Je n'utilise pas les status)
---
```

## Avertissements

!!! note 
    Ceci est une note simple.

!!! note ""
    Ceci est une note sans titre.

!!! note "Ceci est une note avec un titre et un corps"
    TCeci est le corps de la note avec un titre et un corps.

!!! note "Tout peut s'emboiter dans les notes"
    !!! example "Comme d'autres notes"

    ```md title="Ou des blocs de code"
    !!! note "Tout peut s'emboiter dans les notes"
        !!! example "Comme d'autres notes"
    ```

??? note "Ceci est une note fermable"
    Son corps est caché. 

???+ note "Ceci est une note fermable ouverte"
    Son corps est visible par défaut.

!!! note inline end "Cette note est contenue sur une ligne, à la fin de la ligne"

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

## Annotations

On peut annoter le texte (1)
{ .annotate }

1.  Tout peut être imbriqué dans les annotations, comme des avertissements ou du code. 

!!! note annotate "Les annotations peuvent être mises partout (1)"

1.  Comme ici !

## Boutons

[Bouton principal](#buttons){ .md-button .md-button--primary }
[Bouton de paysan](#buttons){ .md-button }

## Code 

`Ceci est une ligne de code`

```
Ceci est un bloc de code
```

```c title="Bloc de code toutes options" linenums="1" hl_lines="4-5"
if (a == b)
{
    Tim = llama // (1)!
    // Ceci est surligné
}
```

1. Utilisez `!` derrière l'annotation pour faire disparaitre le symbole de commentaire devant !

## Tableaux de contenu

=== "A"

    Ceci est du contenu

=== "B"

    Et ceci est un autre contenu

Les tableaux de contenu peuvent être liés. Par exemple, choisir "B" affectera tous les tableaux.

=== "A"

    Vous ne devriez pas voir ceci si vous avez sélectionné "B".

=== "B"

    Vous devriez voir ceci si vous avez sélectionné "B". 

Vous pouvez tout imbriquer dans les tableaux, et les tableaux peuvent être imbriqués partout.

## Tableaux

| Tableau | Simple |
|--------|---------|
| Sucre  | Mauvais |
| Eau    | Bon     |


| Aligné à gauche| Aligné au centre| Aligné a droite |
|:-------------|:--------------:|--------------:|
| Test         | Test           | Test          |


## Diagrammes

Material prend en charge des diagrammes cool, mais je ne les utilise pas vraiment. 

## Foornotes

The footnote is at the foot of the page [^1].

[^1]: Duh. 

With Insiders they can be displayed as tooltips. 

## Formatting

Text can be {--deleted--} and replacement text {++added++}. This can also be
combined into {~~one~>a single~~} operation. {==Highlighting==} is also
possible {>>and comments can be added inline<<}.

{==

Formatting can also be applied to blocks by putting the opening and closing
tags on separate lines and adding new lines between the tags and the content.

==}

- ==This was marked (highlight)==
- ^^This was inserted (underline)^^
- ~~This was deleted (strikethrough)~~

- H~2~O
- A^T^A

++ctrl+alt+del++

## Grids

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

<div class="grid" markdown>

:fontawesome-brands-html5: __HTML__ for content and structure
{ .card }

:fontawesome-brands-js: __JavaScript__ for interactivity
{ .card }

:fontawesome-brands-css3: __CSS__ for text running out of boxes
{ .card }

> :fontawesome-brands-internet-explorer: __Internet Explorer__ ... huh?

</div>

<div class="grid" markdown>

=== "Unordered list"

    * Sed sagittis eleifend rutrum
    * Donec vitae suscipit est
    * Nulla tempor lobortis orci

=== "Ordered list"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci

``` title="Content tabs"
=== "Unordered list"

    * Sed sagittis eleifend rutrum
    * Donec vitae suscipit est
    * Nulla tempor lobortis orci

=== "Ordered list"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci
```

</div>

## Emojis :smile:

[Search emojis :material-arrow-right-thick:](https://squidfunk.github.io/mkdocs-material/reference/icons-emojis/#search){ .md-button }

## Images

![Image](https://dummyimage.com/600x400/eee/aaa)

![Image with alignment](https://dummyimage.com/600x400/eee/aaa){ align=left }

<figure markdown="span">
  ![Image with caption](https://dummyimage.com/600x400/){ width="300" }
  <figcaption>Image caption</figcaption>
</figure>

![Image with lazy loading](https://dummyimage.com/600x400/){ loading=lazy }

![Image title](https://dummyimage.com/600x400/f5f5f5/aaaaaa#only-light)
![Image title](https://dummyimage.com/600x400/21222c/d5d7e2#only-dark)

## Lists

- Nulla et rhoncus turpis. Mauris ultricies elementum leo. Duis efficitur
  accumsan nibh eu mattis. Vivamus tempus velit eros, porttitor placerat nibh
  lacinia sed. Aenean in finibus diam.

    * Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    * Nam vulputate tincidunt fringilla.
    * Nullam dignissim ultrices urna non auctor.


1.  Vivamus id mi enim. Integer id turpis sapien. Ut condimentum lobortis
    sagittis. Aliquam purus tellus, faucibus eget urna at, iaculis venenatis
    nulla. Vivamus a pharetra leo.

    1.  Vivamus venenatis porttitor tortor sit amet rutrum. Pellentesque aliquet
        quam enim, eu volutpat urna rutrum a. Nam vehicula nunc mauris, a
        ultricies libero efficitur sed.

    2.  Morbi eget dapibus felis. Vivamus venenatis porttitor tortor sit amet
        rutrum. Pellentesque aliquet quam enim, eu volutpat urna rutrum a.

        1.  Mauris dictum mi lacus
        2.  Ut sit amet placerat ante
        3.  Suspendisse ac eros arcu

`Lorem ipsum dolor sit amet`

:   Sed sagittis eleifend rutrum. Donec vitae suscipit est. Nullam tempus
    tellus non sem sollicitudin, quis rutrum leo facilisis.

`Cras arcu libero`

:   Aliquam metus eros, pretium sed nulla venenatis, faucibus auctor ex. Proin
    ut eros sed sapien ullamcorper consequat. Nunc ligula ante.

    Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    Nam vulputate tincidunt fringilla.
    Nullam dignissim ultrices urna non auctor.

- [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque

## Tooltips

### Tooltips

[Hover me](https://example.com "I'm a tooltip!")

For other objects, proceed as follows: :smile:{ title="Important information" }

### Abbreviations

The HTML specification is maintained by the W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium




