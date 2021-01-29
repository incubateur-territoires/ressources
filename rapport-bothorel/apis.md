# APIs

## **Les API : un outil utile, mais qui ne doit pas conduire à limiter les réutilisations**

* L'API \(Application Programming Interface\) est une interface qui rend disponible les données et des fonctionnalités d’une application existante, à destination d’une application cliente. 
* Physiquement, les bases de données sont stockées à distance \(chez leur propriétaire par exemple\).
* L’accès aux données souhaitées se fait par le biais de l’API, au moment où l’application cliente en a besoin, par requête, selon des protocoles. 
* Le choix de recourir à une API est le plus souvent justifié par des contraintes techniques, par ex : 
  * la volumétrie de la donnée mise à disposition et des réutilisations, 
  * le degré de sécurité, 
  * la fréquence de mise à jour ou la granularité des données \(cf cas usage SIRENE\). 

L’API présente ainsi à la fois des avantages et des inconvénients pour l’utilisateur, et son utilisation doit donc être justifiée par ce bilan d’opportunité, entre la facilitation du service, et la restriction des usages. Si la donnée est un bien non rival, c’est-à-dire que son utilisation par un nouvel utilisateur ne limite pas l’utilisation qui est faite par les autres utilisateurs, ce n’est pas vrai de l’API, sorte de "pont du XXIème siècle ", infrastructure d’accès à la donnée dont l’utilisation engendre des coûts.

Par ailleurs, il convient de souligner que l’API suppose d’avoir les moyens de recourir à une application qui interroge l’API et récupère les données, ce qui n’est pas à la portée de l’usager non expert, mais ce qui facilite l’appropriation de la donnée pour les réutilisateurs qui souhaitent exploiter la donnée par le biais d’une application.

Le choix d’une API détermine notamment la disponibilité des champs de données et les séries temporelles. En mettant à disposition les données les plus "fraîches", elle permet une mise à jour en continue des données pour l’utilisateur, mais elle rend aussi impossible l’accès aux anciennes données, sauf dans le cas où les paramètres de l’API le permettent. Par exemple, dans le champ de l’environnement, Hub’eau est un portail d’API qui expose de façon simplifiée les données du SI eau.

L’API "Hydrométrie" expose les observations de hauteur d’eau du réseau de mesure français, à partir de la plateforme du service central d’hydrométéorologie et d’appui à la prévision des inondation \(SCHAPI\), mises à jour toutes les deux minutes, avec 24 heures de profondeur, et maintient un historique d’un mois. Cela permet le développement d’applications visant à informer en temps réel des risques d’inondation.

En théorie, une API pourrait permettre au client d’accéder à l’intégralité des champs, sur l’intégralité de la période temporelle et l’intégralité du champ géographique disponible, mais ce service représenterait un coût en infrastructure disproportionné par rapport au besoin. Ainsi, la structure des données transmises par API est le plus souvent simplifiée et se concentre sur les champs identifiés par les principaux usages. Cela permet aussi d’en simplifier l’usage par les développeurs, qui ne sont pas obligés de maîtriser le schéma originel des données pour les exploiter.

L’API permet également de suivre et de réguler les accès des utilisateurs, et présente à cet égard l’avantage pour le diffuseur de pouvoir gérer des fonctions de sécurité ou de contrat, en exigeant que ces informations juridiques soient envoyées dans la requête \(URL, IP, clé de licence, par exemple\). L’API permet également de gérer les débits d’un client afin d’éviter la saturation des services de diffusion. Elle permet ainsi de garder une trace des appels et de mieux comprendre l’usage des données, ce que ne permet pas une diffusion de fichiers, qui plus quand quand ils peuvent être à leur tour rediffusés.

À titre d’exemple, Pôle Emploi a présenté à la mission une "trajectoire d’APIsation", qui répond à la fois "aux orientations stratégiques concernant l’évolution des offres de services de Pôle emploi et à la nécessaire synergie avec \[ses\] partenaires de proximité qui agissent en complémentarité au bénéfice \[des\] usagers ", comme les besoins d’échanges liés à l’emploi des jeunes \(API avec les missions locales\) ou à la mobilité des demandeurs sur les territoires \(API pour favoriser l’accès aux aides aux transports\).

Pour pallier ces inconvénients, en particulier l’impossibilité de reconstituer la base de données complète \(avec tous ses objets et ses champs\), il semble raisonnable d’envisager toujours, en complément de la mise à disposition par API, la mise à disposition de la base de données en format de fichier "plat ", au moins en partie \(comme c’est le cas pour la base SIRENE\).

Finalement, recourir à une API n’est pas qu’un enjeu d’infrastructure, mais un enjeu de gouvernance : le diffuseur et le producteur de la donnée doivent être capables de connaître les besoins et les usages de la donnée, et construire le canal de diffusion en fonction de ces besoins, pour calibrer la disponibilité de la machine en fonction des besoins les plus importants. La mission considère ainsi que les choix des modes de diffusion doivent être dûment justifiés et proportionnés, pour ne pas limiter la capacité de réutilisation.

