# Sélection de variables multivariée en R — Analyse protéomique

Projet réalisé en équipe dans le cadre du Master 2 à l’Université Paris Cité, pour le cours *Questions de sciences des données*.

## Présentation

Ce projet étudie l’influence des conditions expérimentales — **température** et **stade d’imbibition** — sur l’abondance des protéines de graines fraîchement récoltées (FH).

L’objectif est d’identifier les associations les plus pertinentes entre protéines et conditions expérimentales, à l’aide de méthodes de **statistique multivariée** et du package R **MultiVarSel**.

## Démarche

1. **Exploration des données** : analyse descriptive, transformation logarithmique, standardisation, ACP et visualisations.
2. **Modélisation** : construction d’un modèle linéaire multivarié `Y = XB + E` pour les combinaisons température × stade d’imbibition.
3. **Prise en compte des corrélations** : estimation de la structure de covariance résiduelle et blanchiment des données.
4. **Sélection de variables** : utilisation de `MultiVarSel` et d’une procédure de sélection stable.
5. **Analyse des résultats** : interprétation des effets retenus et visualisations par cartes de chaleur et boîtes à moustaches.

## Résultats

Le jeu de données comprend **27 échantillons** et **494 variables protéiques**.

Avec un seuil de fréquence de sélection de **0,93**, l’analyse retient **223 associations protéine–condition expérimentale**. Les conditions de température élevée, notamment aux stades DS et LI, ressortent parmi les groupes présentant le plus d’associations sélectionnées.

## Technologies

**R · MultiVarSel · Quarto · ACP · Modélisation linéaire multivariée · Sélection de variables**

## Fichiers du projet

- `Analyse_proteome_FH.qmd` : rapport Quarto contenant le code R, les analyses et les visualisations.
- `Table_proteome_FH_all.csv` : jeu de données utilisé pour l’étude.

Le rapport peut être ouvert dans **RStudio** ou rendu avec **Quarto**, après installation des packages R nécessaires. Certains chemins locaux et fichiers de résultats intermédiaires peuvent nécessiter une adaptation pour relancer l’ensemble des calculs.
