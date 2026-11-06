# Sélection de variables multivariée en R - Analyse protéomique (FH)

**Projet académique réalisé en équipe** dans le cadre du Master 2 à l’Université Paris Cité, pour le cours *Questions de sciences des données*.

## Objectif

Étudier les associations entre l’abondance des protéines de graines fraîchement récoltées (FH) et deux facteurs expérimentaux : la **température** (Low, Medium, Elevated) et le **stade d’imbibition** (DS, EI, LI).

L’approche repose sur une modélisation linéaire multivariée et sur une sélection de variables tenant compte des dépendances entre les mesures protéiques.

## Méthodologie

1. **Exploration et préparation des données** : transformation logarithmique, standardisation, analyse en composantes principales (ACP) et visualisations.
2. **Modélisation multivariée** : formulation du modèle `Y = XB + E` pour les groupes expérimentaux température × stade d’imbibition.
3. **Prise en compte des corrélations** : étude de la covariance résiduelle et blanchiment (*whitening*) avec le package R `MultiVarSel`.
4. **Sélection stable des variables** : identification des associations entre protéines et conditions expérimentales.
5. **Interprétation** : réestimation des effets sélectionnés et visualisations (cartes de chaleur et boîtes à moustaches).

## Principaux résultats

L’analyse porte sur **27 échantillons** et **494 mesures protéiques**.

Avec un seuil de fréquence de sélection de **0,93**, le rapport identifie **223 couples « protéine–condition expérimentale »**. Ce nombre ne correspond donc pas à 223 protéines distinctes.

Les conditions de température élevée, notamment aux stades DS et LI, figurent parmi celles présentant le plus d’associations sélectionnées.

Ces résultats restent **exploratoires**, compte tenu du faible nombre d’échantillons par rapport au nombre de variables. Les associations observées ne démontrent pas de lien de causalité biologique.

## Technologies utilisées

- **R** : analyses statistiques et visualisations.
- **MultiVarSel** : sélection de variables dans un cadre multivarié.
- **Quarto** : rédaction du rapport et intégration du code et des résultats.

## Contenu du dépôt

- `Analyse_proteome_FH.qmd` : fichier Quarto original contenant le code R, la démarche d’analyse et les interprétations.
- `.gitignore` : exclusion des données pédagogiques et de certains fichiers de résultats locaux.

## Données et reproductibilité

Le fichier `Table_proteome_FH_all.csv` a été **fourni par l’enseignant** dans le cadre du cours. Il n’est pas diffusé dans ce dépôt public, faute d’autorisation explicite de redistribution.

Le fichier de résultats intermédiaires `Freqs_FH.rds` n’est pas non plus publié, dans l’attente d’une vérification des conditions de partage des résultats dérivés.

Pour reproduire l’analyse, il faut disposer du jeu de données par une voie autorisée, installer les packages R nécessaires (dont `MultiVarSel`) et **adapter les chemins locaux** présents dans le fichier Quarto. L’exécution complète de cette version publique n’a pas été vérifiée indépendamment.

## Travail en équipe et crédits

Projet réalisé en équipe par **Adam Aabadli, Fatoumata Ndour et Myriam Abouda**.

Le jeu de données et le cadre pédagogique ont été fournis par l’équipe enseignante. Ce dépôt ne revendique ni la création du package `MultiVarSel` ni celle du jeu de données d’origine.

## Remarque

Ce projet est présenté à des fins pédagogiques et de valorisation des compétences en **statistiques multivariées, sélection de variables et programmation R**.
