
<!-- README.md is generated from README.Rmd. Please edit that file -->

# COGifier

The goal of COGifier is to provide functions, data and map to help
people to analyse french territorial data.

## Installation

You can install the released version of COGifier from
[github](https://https://github.com/) with:

``` r
devtools::install_github("MaelTheuliere/COGifier")
```

## A propos

Ce package R vise à mettre à disposition :

  - les tables du COG 2018 de l’Insee en RData;
  - une table de passage des COG historiques vers le COG millésimé 2018;
  - les couche géomatiques correspondantes au COG 2018.
  - des fonctions d’aide à au passage de jeu de données veres le
    millésime du COG 2018

Le tout avec des règles de nommage identiques pour faciliter les
appariements.

Le package [COGUGAISON](https://github.com/antuki/COGugaison) rempli en
partie la même fonction et nous vous invitons à privilégier son
utilisation, ce présent package visant à répondre à des besoins
spécifiques du DREAL datalab Pays de la Loire. \#\# Les données sources

### Le COG Insee

  - Liste des communes de la métropole et Dom (toutes les communes ayant
    existé depuis 1943) :
    <https://insee.fr/fr/information/3363419#titre-bloc-3>
  - Liste des communes existantes au 1er janvier 2018 :
    <https://insee.fr/fr/information/3363419#titre-bloc-7>
  - Liste des départements :
    <https://insee.fr/fr/information/3363419#titre-bloc-23>
  - Liste des régions :
    <https://insee.fr/fr/information/3363419#titre-bloc-26>
  - Liste des intercommunalités :
    <https://insee.fr/fr/information/2510634>

### Admin Express

  - Admin express : <http://professionnels.ign.fr/adminexpress#tab-3>

## Description du package

Le package contient

### 12 dataframes

  - **communes** : la table des communes existants au 1er janvier 2018
  - **epci** : la table des EPCI existants au 1er janvier 2018
  - **departements** la table des départements existants au 1er janvier
    2018
  - **regions** : la table des régions existants au 1er janvier 2018
  - **table\_passage\_com\_epci** : une table listant la composition des
    communes de chaque Epci
  - **table\_passage\_com\_historique** : une table de passage entre
    l’historique des communes ayant déjà existé un jour et les
    communes existants au 1er janvier 2018
  - **communes\_geo** : géométrie des communes métropolitaines
  - **epci\_geo** : géométrie des epci métropolitains
  - **departements\_geo** : géométrie des départements métropolitains
  - **regions\_geo** : géométrie des regions métropolitaines
  - **zonage\_abc\_r52** : table d’attribution du zonage abc aux
    communes 2018
  - **zonage\_pinel\_r52** : table d’attribution du zonage Pinel aux
    communes 2018
  - **liste\_zone** : table d’attribution d’une liste de régions
    d’appartenance pour les régions, départements, epci,communes

### 2 fonctions

  - **passer\_au\_cog\_a\_jour()** : permet d’attribuer un code commune
    à jour à une table communale
  - **cogifier()** : permet d’aggréger les données d’une table communale
    pour avoir les totaux par communes,epci,départements, région et
    france sur le millésime 2018

## Exemple d’usage

Le package contient une table Insee de recensement de la population à la
commune sur le millésime 2015.

``` r
pop2015<-data("pop2015")
pop2015_COG2018<-passer_au_cog_a_jour(pop2015)
pop2015_COGIFIEE<-cogifier(pop2015)
```
