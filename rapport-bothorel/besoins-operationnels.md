---
description: 1.2. Des données de qualité au service des différents usages
---

# Besoins opérationnels \[DRAFT\]

## **Normaliser à des fins d’interopérabilité des données**

L’interopérabilité recouvre la capacité à agréger des données issues de sources différentes et nécessite que les données se standardisent. Cette convergence sur des structurations compatibles, comporte en particulier :

* une sémantique et une syntaxe partagée ;
* une structuration commune pour des données semblables ;
* des dictionnaires et registres pour remplir les champs des données et des métadonnées ;
* une même projection cartographique pour les données géographiques ;
* un même carroyage ou des carroyages compatibles pour des données agrégées ou résultantes d’opérations statistiques.

> Le référencement, la création et la validation de schéma de données est capital lorsque plusieurs producteurs de données produisent des jeux de données sur un même sujet, afin que ces jeux de données puissent être facilement croisés.

* Au sein de l’infrastructure mise en œuvre par la DINUM : schema.data.gouv.fr 
* Des travaux sont en cours pour intégrer au mieux ces outils à la plateforme data.gouv.fr.

**Consolider un catalogage des données**

* Chaque infrastructure possède son propre catalogue des données hébergées, produit à partir des métadonnées accompagnant les jeux de données. 
* Il apparaît impossible de constituer un catalogue unique des données publiques ouvertes ou non, notamment du fait de redondances des données dans différents catalogues, d’obsolescence et de métadonnées déficientes.

> Il s’agit de répondre aux questions : - existe-t-il une base de données qui répond à mon besoin ? – où se trouve sa version la plus aboutie/légitime ? – qui en est propriétaire ?, quelles sont les informations de qualité, de confidentialité, de licence ? Ces informations devraient être disponibles pour les bases de données publiques ouvertes comme pour les bases de données publiées en diffusion restreintes.

* La présence de données dans data.gouv.fr ne signifie pas qu’il s’agit de la base de données la plus fraiche, la plus légitime.

## **Moissonnage et de syndication**

* La syndication permet à une infrastructure d’informer des "abonnés" des changements concernant ses bases de données. Cette information est récapitulée et poussée par l’infrastructure vers les abonnés.
* Le moissonnage permet à une infrastructure de charger automatiquement des ressources \(métadonnées, données\) à partir du catalogue de données d’une autre infrastructure. 
* Via les métadonnées, on peut construire un catalogue "général" de données par moissonnage. Il n’y a pas besoin de charger les données : la connaissance des métadonnées permet à une infrastructure d’accéder aux données d’une autre infrastructure selon ses besoins par l’intermédiaire d’API.
* Nécessité de combiner deux approches : 
  * d’une part la définition au niveau de la DINUM d’une politique interministérielle d’interopérabilité et de qualité de la donnée
  * d’autre part, sa mise en œuvre au niveau de chaque communauté de travail, pour avoir des règles communes de travail acceptées par tous.

{% hint style="info" %}
**Recommandation** : Définir et mettre en œuvre une politique interministérielle d’interopérabilité et de qualité de la donnée \(démarches de standardisation, notamment des codes sources, label FAIR, doctrine sur les métadonnées, catalogage\)
{% endhint %}

{% hint style="info" %}
**Recommandation** : Encourager les écosystèmes à définir des principes de gouvernance de la qualité, en désignant un référent qualité et en créant des communautés de réutilisation avec participation active des producteurs de la donnée
{% endhint %}

## \*\*\*\*

