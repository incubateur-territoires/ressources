---
description: >-
  À partir de 3.2. Des infrastructures adaptées aux différents usages de la
  donnée
---

# Infrastructure et enjeux autour de data.gouv.fr

Conçu au départ comme un outil pour donner de la visibilité sur les données existantes et rassembler ces données sur un point d’entrée unique, data.gouv.fr est rapidement considéré comme une infrastructure.

> Dans les dispositions du décret n° 2019-1088 du 25 octobre 2019 relatif au système d'information et de communication de l'État et à la direction interministérielle du numérique, data.gouv.fr est indiqué comme "le portail unique interministériel destiné à rassembler et à mettre à disposition librement l'ensemble des informations publiques de l'État, de ses établissements publics et, si elles le souhaitent, des collectivités territoriales et des personnes de droit public ou de droit privé chargées d'une mission de service public".

De par sa conception, l’"infrastructure data.gouv.fr" a offert dès sa création des services pour rassembler l’ensemble des acteurs afin de devenir ce point central de découverte des données publiques. 

* Pour les infrastructures existantes possédant leurs propres catalogues de données, data.gouv.fr offre des **services de moissonnage** dans une vision fédératrice \(74% des jeux de données proviennent de moissonnage, 40% des collectivités possédant une infrastructure sont régulièrement moissonnées\). 
* En parallèle il propose aux administrations et notamment aux collectivités qui ne peuvent se permettre d’investir dans de la compétence et des technologies, des **services simples de dépôt de données, de documentation et de mise en relation** avec les réutilisateurs, dans une vision d’infrastructure communautaire.

### Services connexes facilitant exposition et appropriation des données :

* Api.gouv.fr propose un **catalogue des API** des administrations. 
  * Le service api.gouv.fr référence des API dont l’accès est restreint aux administrations habilitées. La multiplication des jeux de données \(plus de 35000 à ce jour\) impose de faire monter le moteur de recherche en échelle et de répondre au besoin de simplicité et de pertinence attendu des usagers. Le travail éditorial est d’autant amplifié.
* Geo-datagouv permet de **moissonner les catalogues compatibles avec les principes de la directive INSPIRE**, essentiellement des infrastructures de données géographiques.
  * Le service Geo.data.gouv.fr n’est plus maintenu. Des plateformes régionales d’informations géographiques compatibles avec les principes INSPIRE ne sont actuellement plus moissonnées. Il conviendrait d’organiser la remontée des informations en lien avec le ministère de la transition écologique en charge de la mise en œuvre de la directive INSPIRE, et avec le bureau de recherches géologiques et minières \(BRGM\) qui entretient le géocatalogue, point focal des données géographiques entrant dans le champ de la directive en charge d’alimenter le rapportage européen annuel de la France.
* Schéma.gouv.fr offre la possibilité aux administrations de r**éférencer les schémas des bases de données** que data.gouv.fr relaie dans une logique de qualité vertueuse d’adéquation des données au schéma qui les structure pour en faciliter l’appropriation et en permettre l’agrégation.
* Enfin, l’expérience de transport.data.gouv.fr démontre la faisabilité de bénéficier des briques de service de l’infrastructure \("le **back-end**"\) **dans une approche décentralisée**. C’est une approche mise en avant par Etalab.

### Chantiers possibles

L’offre de service de data.gouv.fr ne suffit pas aux besoins de découverte. Ce point unique ne doit pas se contenter de ne cataloguer que les données ouvertes, mais il doit aussi rendre compte des données partageables sous conditions, les données accessibles ou consultables voire des données fermées des administrations si elles le souhaitent. Savoir qu’une donnée existe et pour quelle raison elle n’est pas publiée fait gagner le temps d’une recherche vaine \(on peut penser par exemple aux bases de données des services statistiques ministériels couvertes par le secret statistique\).

Il existe des chantiers ouverts à Etalab mais cela demande des ressources : 

* s’intéresser aux données "sources" pour permettre de rejouer des algorithmes, 
* travailler sur la montée en qualité des données exposées
* améliorer la visibilité des contenus, notamment en investissant dans l’éditorialisation - en particulier pour les espaces de données non sectorielles, qui échappent à l'animation des communautés sectorielles. 

