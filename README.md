
<!-- README.md is generated from README.Rmd. Please edit that file -->

# COGiter

COGiter fournis des fonctions, des données et des fonds de carte pour
permettre des analyses territoriales sur le territoire français.

## Installation

Installer le package depuis [github](https://github.com/) ou
[gitlab](https://gitlab.com)

``` r
remotes::install_github("MaelTheuliere/COGiter")
remotes::install_github("dreal-datalab/COGiter")
```

## A propos

Ce package R vise à mettre à disposition :

  - les tables du COG 2019 de l’Insee en RData;
  - une table de passage des COG historiques vers le COG millésimé 2019;
  - les couche géomatiques correspondantes au COG 2019.
  - des fonctions d’aide à au passage de jeu de données veres le
    millésime du COG 2019

Le tout avec des règles de nommage identiques pour faciliter les
appariements.

Le package [COGUGAISON](https://github.com/antuki/COGugaison) rempli en
partie la même fonction et nous vous invitons à privilégier son
utilisation. Ce présent package visant à répondre à des besoins
spécifiques du [DREAL datalab Pays de la
Loire](http://www.pays-de-la-loire.developpement-durable.gouv.fr/dreal-centre-de-service-de-la-donnee-r1957.html)
et est par ailleurs non stabilisé.

## Les données sources

### Le COG Insee 2019

  - <https://www.insee.fr/fr/information/2560452>

### Admin Express

  - <http://professionnels.ign.fr/adminexpress#tab-3>

## Description du package

Voir la [page de
référence](https://maeltheuliere.github.io/COGiter/reference/index.html)

## Exemple d’usage

Voir la
[vignette](https://maeltheuliere.github.io/COGiter/articles/cogiter.html)
