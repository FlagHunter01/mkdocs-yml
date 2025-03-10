---
title: Installation
description: Installation de Material for Mkdocs Insiders
---

## Préface

Gardez en mémoire le fait que la documentation officielle [squidfunk.github.io/mkdocs-material/](https://squidfunk.github.io/mkdocs-material/) est bien meilleure que celle-ci et devraient être utilisée de préférence.

N'utilisez ce guide que si vous avez besoin d'un template à copier-coller et que ous comprenez déjà la vraie docupmentation.

!!! warning "Version payante Insiders" 
    Ce guide ne fonctionne qu'avec [Material Insiders](https://squidfunk.github.io/mkdocs-material/insiders/)

!!! info "Environnement"
    **Ce guide sert au self-hosting sur Linux.** Pour les autres méthodes d'implémentation, merci de se référer encore une fois a la [documentation officielle](https://squidfunk.github.io/mkdocs-material/getting-started/). 

## Préparation de l'environnment

### Téléchargements

Voici tous les téléchargements que vous devrez effectuer:

```
apt install python3 libcairo2-dev libfreetype6-dev libffi-dev libjpeg-dev libpng-dev libz-dev pngquant
pip install "mkdocs-material[imaging]"
pip install mkdocs-rss-plugin
pip install mkdocs-git-committers-plugin-2
pip install mkdocs-git-revision-date-localized-plugin
pip install mkdocs-glightbox
```

### Material for Mkdocs Insiders

Achetez Material for Mkfocs insiders. 
La page post-achat ainsi que [celle-ci](https://squidfunk.github.io/mkdocs-material/insiders/access-management/) devraient contenir toutes les informations dont vous avez besoin.

Une fois que vous aurez terminé, rendez vois ici: [Getting started with Insiders](https://squidfunk.github.io/mkdocs-material/insiders/getting-started/). 

## Utiliser Mkdocs

### Commandes

C'est très simple !

Pour commencer, créez un nouveau projet:

```
mkdocs new my-project
cd my-project
```

Dans ce nouveau dossier, vous trouvrez l'arbo basique d'un projet MkDocs. 

C'est ici que vous pouvez copier-coller mon template (cloneable de [https://github.com/FlagHunter01/mkdocs-yml.git](https://github.com/FlagHunter01/mkdocs-yml.git)).

Pour prévisualiser votre site, entrez la commande suivante puis connecez-vous a [localhost:8000](http://localhost:8000):

```
mkdocs serve
```

Une fois que vous avez terminé, vous pouvez générer l'HTML avec:

```
mkdocs buid
```

Le code sera disponible a `\site\`. 

### VSCode

Si vous utilisez [Visual Studio Code](https://code.visualstudio.com/), vous pouvez ajouter deux modules qui amélioreront grandement votre qualité de vie.

#### TODO Highlight v2

Téléchargez TODO Highlight v2 pour souligner tous les tags `TODO:` dans mes fichiers. C'est un moyen simple de se remémorer toutes les options qui doivent être personnalisées avant de commencer a écrire votre documentation.

#### YAML by RedHat

Téléchargez YAML by RedHat et copiez ce qui suit dans vous paramètres JSON pour obtenir le debug officiel de Material for Mkdocs:

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

## Utiliser le markdown

Voici les bases du markdown. 

```md
Texte

*Italique*

**Gras**

# Titre principal (1 par doc)

## Titre

### Sous-titre

[Lien](http://url.com)

![Image](../images/cat.jpg))

| Table | Example |
|-------|---------|
| 1     | Banana  |
| 2     | Apple   |
```

!!! example "Sortie"
    Texte

    *Italique*

    **Gras**

    #Titre principal (1 par doc)

    ## Titre

    ### Sous-titre

    [Lien](http://url.com)

    ![Image](../images/cat.jpg) 

    | Table | Example |
    |-------|---------|
    | 1     | Banana  |
    | 2     | Apple   |

## Note à soi-même - quand les plugins déraillent

Si socials, blog ou projet commencent a retourner des erreurs étranges même après avoir téléchargé la dernière version d'Insiders, essayer ce qui suit:
```
pip install mkdocs-material mkdocs-material-extensions --upgrade
pip install pillow cairosvg --upgrade
```
