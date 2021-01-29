---
description: 1.2. Des données de qualité au service des différents usages
---

# Besoins opérationnels

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

**Un catalogage des données à consolider**

Le catalogage, au niveau agrégé, des données disponibles en open data est particulièrement problématique. En effet, à chaque infrastructure appartient un catalogue des données hébergées. Celui-ci est produit à partir des métadonnées accompagnant les jeux de données. Or si l’on observe l’ensemble des infrastructures de données comme une infrastructure nationale, il apparaît impossible de constituer un catalogue unique des données publiques ouvertes ou non, notamment du fait de redondances des données dans différents catalogues, d’obsolescence et de métadonnées déficientes.

Il s’agit de répondre aux questions : - existe-t-il une base de données qui répond à mon besoin ? – où se trouve sa version la plus aboutie/légitime ? – qui en est propriétaire ?, quelles sont les informations de qualité, de confidentialité, de licence ? Ces informations devraient être disponibles pour les bases de données publiques ouvertes comme pour les bases de données publiées en diffusion restreintes.

Ainsi, la présence de données dans data.gouv.fr ne signifie pas qu’il s’agit de la base de données la plus fraiche, la plus légitime. Par exemple, par le moissonnage des catalogues de données des DDT, de nombreux documents d’urbanisme sont accessibles sur data.gouv.fr. Toutefois, il n’est pas garanti qu’il s’agit des documents les plus récents qui font foi, ceux-ci étant disponibles en mairie.

Ainsi, lors du hackathon sur les données d’urbanisme organisé en février 2017 par le ministère en charge du logement, des aménageurs témoignaient de la part trop importante de temps consacré à la recherche des données les plus fiables lors d’une étude d’aménagement qu’ils estimaient à 80 %.

**Les concepts de moissonnage et de syndication**

Les nombreuses infrastructures décrites dans ce rapport ne sont pas toutes indépendantes, il existe de nombreux liens permettant sous une forme normalisée d’échanger des informations de métadonnées et d’échanger des données.

La syndication permet à une infrastructure d’informer des "abonnés" des changements concernant ses bases de données. Ainsi, il n’y a pas besoin de consulter régulièrement un portail ou une plateforme pour savoir ce qui a changé ou l’ajout d’une nouvelle donnée, cette information est récapitulée dans une information envoyée par l’infrastructure. En ce sens, le Géoportail de l’Urbanisme mis en place par la DHUP informe ses abonnés des nouvelles publications de documents d’urbanisme sur le territoire national à l’aide de flux conformes au protocole ATOM\[9\].

Le moissonnage permet à une infrastructure de charger automatiquement des ressources \(métadonnées, données\) à partir du catalogue de données d’une autre infrastructure. Là aussi, il existe des protocoles bien rodés. Ainsi data.gouv.fr propose aux administrations de moissonner leurs sites\[10\]. Via les métadonnées, on peut construire un catalogue "général" de données par moissonnage. C’est le cas du Géocatalogue mis en œuvre par le BRGM pour le compte de l’infrastructure voulue par la directive INSPIRE. Il n’y a pas besoin de charger les données : la connaissance des métadonnées permet à une infrastructure d’accéder aux données d’une autre infrastructure selon ses besoins par l’intermédiaire d’API.

Le graphe ci-après, construit par le projet de recherche GEOBS\[11\] illustre l’activité de moissonnage entre IDG \(infrastructures de données géographiques\) en France en 2018. On perçoit le caractère fractal des infrastructures de données mais aussi l’activité intense d’échange entre ces infrastructures.

Schéma du moissonnage des infrastructures de données géographiques \(DIG\)

Source : Projet Geobs \(CNRS 2017\).

Dans ce contexte, la mission souhaite mettre l’accent sur la nécessité de combiner deux approches : d’une part la définition au niveau de la DINUM d’une politique interministérielle d’interopérabilité et de qualité de la donnée et d’autre part, sa mise en œuvre au niveau de chaque communauté de travail, pour avoir des règles communes de travail acceptées par tous.

**Recommandation** : Définir et mettre en œuvre une politique interministérielle d’interopérabilité et de qualité de la donnée \(démarches de standardisation, notamment des codes sources, label FAIR, doctrine sur les métadonnées, catalogage\)

**Recommandation** : Encourager les écosystèmes à définir des principes de gouvernance de la qualité, en désignant un référent qualité et en créant des communautés de réutilisation avec participation active des producteurs de la donnée

**Les API : un outil utile, mais qui ne doit pas conduire à limiter les réutilisations**

Le choix du mode de diffusion de la donnée détermine beaucoup la liberté de réutilisation et la variété des usages qui peuvent en être fait. En particulier, la diffusion peut se faire sous forme de formats "plats" \(données dans un tableau par exemple\) ou par le biais d’une API \(Application Programming Interface\), interface qui rend disponible les données et des fonctionnalités d’une application existante, à destination d’une application cliente. Physiquement, les bases de données sont stockées à distance \(chez leur propriétaire par exemple\) et l’accès aux données souhaitées se fait par le biais de l’API, au moment où l’application cliente en a besoin, par requête, selon des protocoles.

Le choix de recourir à une API est le plus souvent justifié par des contraintes techniques, comme la volumétrie de la donnée mise à disposition et des réutilisations, le degré de sécurité, la fréquence de mise à jour ou la granularité des données \(par exemple dans le cas de la base SIRENE, exploitée par de nombreux réutilisateurs, comme exposé dans le cas d’usage spécifique\).

L’API présente ainsi à la fois des avantages et des inconvénients pour l’utilisateur, et son utilisation doit donc être justifiée par ce bilan d’opportunité, entre la facilitation du service, et la restriction des usages. Si la donnée est un bien non rival, c’est-à-dire que son utilisation par un nouvel utilisateur ne limite pas l’utilisation qui est faite par les autres utilisateurs, ce n’est pas vrai de l’API, sorte de "pont du XXIème siècle ", infrastructure d’accès à la donnée dont l’utilisation engendre des coûts.

Par ailleurs, il convient de souligner que l’API suppose d’avoir les moyens de recourir à une application qui interroge l’API et récupère les données, ce qui n’est pas à la portée de l’usager non expert, mais ce qui facilite l’appropriation de la donnée pour les réutilisateurs qui souhaitent exploiter la donnée par le biais d’une application.

Le choix d’une API détermine notamment la disponibilité des champs de données et les séries temporelles. En mettant à disposition les données les plus "fraîches", elle permet une mise à jour en continue des données pour l’utilisateur, mais elle rend aussi impossible l’accès aux anciennes données, sauf dans le cas où les paramètres de l’API le permettent. Par exemple, dans le champ de l’environnement, Hub’eau est un portail d’API qui expose de façon simplifiée les données du SI eau.

L’API "Hydrométrie" expose les observations de hauteur d’eau du réseau de mesure français, à partir de la plateforme du service central d’hydrométéorologie et d’appui à la prévision des inondation \(SCHAPI\), mises à jour toutes les deux minutes, avec 24 heures de profondeur, et maintient un historique d’un mois. Cela permet le développement d’applications visant à informer en temps réel des risques d’inondation.

En théorie, une API pourrait permettre au client d’accéder à l’intégralité des champs, sur l’intégralité de la période temporelle et l’intégralité du champ géographique disponible, mais ce service représenterait un coût en infrastructure disproportionné par rapport au besoin. Ainsi, la structure des données transmises par API est le plus souvent simplifiée et se concentre sur les champs identifiés par les principaux usages. Cela permet aussi d’en simplifier l’usage par les développeurs, qui ne sont pas obligés de maîtriser le schéma originel des données pour les exploiter.

L’API permet également de suivre et de réguler les accès des utilisateurs, et présente à cet égard l’avantage pour le diffuseur de pouvoir gérer des fonctions de sécurité ou de contrat, en exigeant que ces informations juridiques soient envoyées dans la requête \(URL, IP, clé de licence, par exemple\). L’API permet également de gérer les débits d’un client afin d’éviter la saturation des services de diffusion. Elle permet ainsi de garder une trace des appels et de mieux comprendre l’usage des données, ce que ne permet pas une diffusion de fichiers, qui plus quand quand ils peuvent être à leur tour rediffusés.

À titre d’exemple, Pôle Emploi a présenté à la mission une "trajectoire d’APIsation", qui répond à la fois "aux orientations stratégiques concernant l’évolution des offres de services de Pôle emploi et à la nécessaire synergie avec \[ses\] partenaires de proximité qui agissent en complémentarité au bénéfice \[des\] usagers ", comme les besoins d’échanges liés à l’emploi des jeunes \(API avec les missions locales\) ou à la mobilité des demandeurs sur les territoires \(API pour favoriser l’accès aux aides aux transports\).

Pour pallier ces inconvénients, en particulier l’impossibilité de reconstituer la base de données complète \(avec tous ses objets et ses champs\), il semble raisonnable d’envisager toujours, en complément de la mise à disposition par API, la mise à disposition de la base de données en format de fichier "plat ", au moins en partie \(comme c’est le cas pour la base SIRENE\).

Finalement, recourir à une API n’est pas qu’un enjeu d’infrastructure, mais un enjeu de gouvernance : le diffuseur et le producteur de la donnée doivent être capables de connaître les besoins et les usages de la donnée, et construire le canal de diffusion en fonction de ces besoins, pour calibrer la disponibilité de la machine en fonction des besoins les plus importants. La mission considère ainsi que les choix des modes de diffusion doivent être dûment justifiés et proportionnés, pour ne pas limiter la capacité de réutilisation.  


\[1\] https://www.pasteur.fr/fr/file/19235/download, https://www6.inrae.fr/datapartage/Produire-des-donnees-FAIR

\[2\] https://www.go-fair.org/fair-principles/

\[3\] Cadre commun d’architecture des référentiels de données, complément n°2 au cadre commun d’urbanisation du système d’information de l’État version 1.0, Direction interministérielle des systèmes d'information et de communication \(DISIC\), version n°1.0 du 18 décembre 2013.

\[4\] Voir l’exemple cité à l’annexe 1 du rapport au Gouvernement de Valéria Faure-Muntian, Les données géographiques souveraines, daté de juillet 2018.

\[5\] http://mdm.sandre.eaufrance.fr/geo/rapportsv3

\[6\] https://artificialisation.biodiversitetousvivants.fr/sites/artificialisation/files/inlinefiles/observatoir\_artificialisation\_flyer.pdf

\[7\] https://www.sandre.eaufrance.fr/missions-et-organisation-du-sandre

\[8\] Les schémas de données permettent de décrire des modèles de données : quels sont les différents champs, comment sont représentées les données, quelles sont les valeurs possibles etc.

\[9\] https://www.geoportail-urbanisme.gouv.fr/image/UtilisationATOM\_GPU\_1-0.pdf

\[10\] https://doc.data.gouv.fr/jeux-de-donnees/demander-a-datagouvfr-de-moisonner-votre-site/

\[11\] https://www-iuem.univ-brest.fr/pops/attachments/1746 , voir aussi Adeline Maulpoix, Matthieu Noucher, Olivier Pissoat, Grégoire Le Campion, Françoise Gourmelon, et al.. Enquête 2017 auprès des coordinateurs des Infrastructures de Données Géographiques en France.

Rapport intermédiaire du projet de recherche GEOBS. \[Rapport de recherche\] Passages UMR 5319;

LETG - Brest Géomer; PRODIG. 2017. halshs-01635844

