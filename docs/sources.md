# Sources de données — Projet emploi & reconversions

Ce document décrit les sources de données utilisées dans le projet,
leur périmètre, et ce qu’elles permettent (ou non) d’analyser.


## Dataset 1 : Activité emploi et chômage - enquête emploi en continu - INSEE

### Source
- Producteur : INSEE
- Lien : https://www.data.gouv.fr/datasets activite-emploi-et-chomage-enquete-emploi-en-continu
- Format : CSV
- Fréquence : annuelle

### Périmètre
- Période couverte : 2020 - 2023
- Granularité : France entière
- Unité statistiques : individu, actif occupé, chômeur

### Nature des variables (description conceptuelle)
Le dataset repose sur des indicateurs décrivant :
- le statut d’activité (emploi, chômage, inactivité)
- l’évolution temporelle de ces statuts
- des caractéristiques socio-professionnelles agrégées
- des déclinaisons territoriales possibles

Les noms exacts des variables et leur format seront validés lors de la phase
d’ingestion et d’exploration des données (J3).

### Ce que ce dataset permet d’analyser
- l’évolution de l’emploi et du chômage sur longue période
- les tendances structurelles du marché du travail
- les effets de cycles économiques ou de crises
- le contexte macro des reconversions professionnelles

### Ce que ce dataset ne permet PAS d’analyser
- les parcours individuels de reconversion
- les transitions métier à l’échelle individuelle

### Limites et points d’attention
- données issues d’une enquête (et non de fichiers administratifs)
- reconversion mesurée de manière indirecte
- nécessité de vérifier la stabilité des définitions dans le temps


## Dataset 2 — Inscrits à France Travail - Stock - France (trimestrielles, brutes)

### Source
- Producteur : DARES
- Lien : https://www.data.gouv.fr/datasets/inscrits-a-france-travail-stock-france-trimestrielles-brutes
- Format : CSV
- Fréquence : trimestrielle

### Périmètre
- Période couverte : 1996 – 2025
- Champ géographique : France (déclinaisons possibles selon variables)
- Unité statistique : stock agrégé de demandeurs d’emploi inscrits à France Travail

### Nature des variables (description conceptuelle)
Le dataset contient des variables décrivant :
- le nombre de demandeurs d’emploi inscrits
- des caractéristiques sociodémographiques (sexe, tranche d’âge)
- des caractéristiques liées au profil professionnel (qualification, métier recherché lorsque disponible)
- des découpages temporels (année, trimestre)

### Ce que ce dataset permet d’analyser
- l’évolution du nombre de demandeurs d’emploi dans le temps
- les dynamiques par sexe et par tranche d’âge
- les variations selon le niveau de qualification
- des tendances indirectes de mobilité ou de reconversion professionnelle

### Ce que ce dataset ne permet PAS d’analyser
- les parcours individuels de reconversion
- les transitions d’un métier vers un autre à l’échelle individuelle
- les durées de reconversion ou les trajectoires complètes

### Limites et points d’attention
- données agrégées (pas de suivi individuel)
- certaines dimensions (métier, formation) peuvent être incomplètes selon les périodes
- les changements de catégories ou de nomenclature doivent être vérifiés sur longue période