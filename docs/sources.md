# Sources de données — Projet emploi et chômage en France

Ce document décrit les sources de données utilisées dans le cadre du projet
d’analyse de l’évolution de l’emploi et du chômage en France, leur périmètre,
leurs apports analytiques et leurs limites.

L’objectif est de garantir une utilisation rigoureuse et transparente des données,
en précisant clairement ce qu’elles permettent — et ne permettent pas — d’analyser.

---

## Dataset 1 — Activité, emploi et chômage  
### Enquête emploi en continu — INSEE

### Source
- Producteur : INSEE
- Lien : https://www.data.gouv.fr/datasets/activite-emploi-et-chomage-enquete-emploi-en-continu
- Format : CSV
- Fréquence : trimestrielle (diffusion annuelle par millésime)

### Périmètre
- Période couverte : 2018 – 2023
- Champ géographique : France
- Unité statistique : individu enquêté
- Nature : enquête statistique par sondage

### Nature des variables (description conceptuelle)
Ce dataset repose sur des variables décrivant :
- le statut d’activité des individus (emploi, chômage, inactivité),
- des caractéristiques sociodémographiques (âge, sexe),
- des informations professionnelles codées (statut, catégorie socioprofessionnelle),
- une dimension temporelle structurée par année et trimestre.

Les variables sont majoritairement codées selon des nomenclatures statistiques
propres à l’INSEE.

### Ce que ce dataset permet d’analyser
- le contexte général du marché du travail (emploi / chômage),
- la structure de la population active observée,
- les évolutions macroéconomiques récentes,
- des éléments de contexte utiles à l’interprétation des données administratives.

### Ce que ce dataset ne permet PAS d’analyser
- des volumes exhaustifs de population (données d’enquête),
- des trajectoires individuelles dans le temps,
- des reconversions professionnelles à l’échelle individuelle,
- des transitions directes d’un métier à un autre.

### Limites et points d’attention
- données issues d’une enquête et non de fichiers administratifs exhaustifs,
- rupture observée dans le volume d’individus enquêtés selon les périodes,
- changements méthodologiques possibles selon les millésimes,
- en conséquence, ces données sont utilisées dans ce projet à des fins de
  contextualisation uniquement, et non pour produire des volumes comparables
  dans le temps.

---

## Dataset 2 — Inscrits à France Travail  
### Stock de demandeurs d’emploi — DARES

### Source
- Producteur : DARES (France Travail)
- Lien : https://www.data.gouv.fr/datasets/inscrits-a-france-travail-stock-france-trimestrielles-brutes
- Format : CSV
- Fréquence : trimestrielle

### Périmètre
- Période couverte : 1996 – 2025
- Champ géographique : France
- Unité statistique : stock agrégé de demandeurs d’emploi inscrits
- Nature : données administratives

### Nature des variables (description conceptuelle)
Ce dataset contient des variables décrivant :
- le nombre de demandeurs d’emploi inscrits à France Travail,
- des caractéristiques sociodémographiques agrégées (sexe, tranche d’âge),
- des éléments liés au profil professionnel (qualification, métier recherché
  lorsque disponible),
- une dimension temporelle structurée par année et trimestre.

Les données sont agrégées et ne permettent pas le suivi individuel des personnes.

### Ce que ce dataset permet d’analyser
- l’évolution du nombre de demandeurs d’emploi dans le temps,
- les dynamiques de long terme et les ruptures conjoncturelles,
- les comparaisons par sexe et par tranche d’âge,
- les effets macroéconomiques des crises sur le chômage,
- des tendances globales du marché du travail pouvant servir de base à des
  analyses ultérieures sur la mobilité ou la reconversion professionnelle.

### Ce que ce dataset ne permet PAS d’analyser
- les parcours individuels de reconversion,
- les transitions professionnelles individuelles,
- les changements effectifs de métier ou de secteur,
- les durées et trajectoires complètes de retour à l’emploi.

### Limites et points d’attention
- données agrégées, sans suivi longitudinal des individus,
- certaines dimensions (métier, formation) peuvent être incomplètes ou
  hétérogènes selon les périodes,
- nécessité de vérifier les changements de nomenclature sur longue période,
- présence de catégories « Total » pouvant conduire à des doubles comptages
  si elles ne sont pas traitées avec précaution.

---

## Rôle des données dans le projet

Dans ce projet :
- les données **DARES** constituent la source principale d’analyse, permettant
  d’étudier l’évolution du nombre de demandeurs d’emploi sur le long terme ;
- les données **INSEE** sont mobilisées uniquement comme source de contexte
  et de contrôle méthodologique, afin d’éclairer les limites et le cadre
  d’interprétation des résultats issus des données administratives.

Les reconversions professionnelles ne sont pas traitées dans ce projet et feront
l’objet d’une analyse spécifique dans un projet distinct, mobilisant des sources
de données dédiées (formation, insertion, trajectoires).