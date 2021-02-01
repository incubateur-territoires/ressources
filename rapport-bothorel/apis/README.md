# 📎 APIs

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

Le choix d’une API détermine notamment la disponibilité des champs de données et les séries temporelles. En mettant à disposition les données les plus "fraîches", elle permet une mise à jour en continue des données pour l’utilisateur, mais elle rend aussi impossible l’accès aux anciennes données, sauf dans le cas où les paramètres de l’API le permettent.

* La structure des données transmises par API est le plus souvent simplifiée et se concentre sur les champs identifiés par les principaux usages. 
* L’API permet également de suivre et de réguler les accès des utilisateurs, et présente à cet égard l’avantage pour le diffuseur de pouvoir gérer des fonctions de sécurité ou de contrat, en exigeant que ces informations juridiques soient envoyées dans la requête \(URL, IP, clé de licence, par exemple\). 
* L’API permet également de gérer les débits d’un client afin d’éviter la saturation des services de diffusion. Elle permet ainsi de garder une trace des appels et de mieux comprendre l’usage des données, ce que ne permet pas une diffusion de fichiers.

> À titre d’exemple, Pôle Emploi a présenté à la mission une "trajectoire d’APIsation", qui répond à la fois "aux orientations stratégiques concernant l’évolution des offres de services de Pôle emploi et à la nécessaire synergie avec \[ses\] partenaires de proximité qui agissent en complémentarité au bénéfice \[des\] usagers ", comme les besoins d’échanges liés à l’emploi des jeunes \(API avec les missions locales\) ou à la mobilité des demandeurs sur les territoires \(API pour favoriser l’accès aux aides aux transports\).

* Toujours envisager en complément de la mise à disposition par API, la mise à disposition de la base de données en format de fichier "plat ", au moins en partie \(comme c’est le cas pour la base SIRENE\).

{% hint style="info" %}
Recourir à une API n’est pas qu’un enjeu d’infrastructure, mais un enjeu de gouvernance : le diffuseur et le producteur de la donnée doivent être capables de **connaître les besoins** et les usages de la donnée, et **construire le canal de diffusion en fonction de ces besoins**, pour calibrer la disponibilité de la machine en fonction des besoins les plus importants. 
{% endhint %}

 



  


### CAS D’USAGE – La base SIRENE

**Une des bases les plus réutilisées de l’open data**

Le répertoire des entreprises et des établissements, dénommé SIRENE enregistre l'état civil de toutes les entreprises et leurs établissements.

Géré par l’INSEE et mis à disposition notamment sur data.gouv.fr, il est considéré par l’État comme une base pivot dans le cadre de la stratégie pour un État-plateforme. La base s’articule autour du numéro SIREN, qui est un numéro à neuf chiffres permettant d’identifier les entreprises, et du numéro SIRET permettant d’identifier les établissements d’une entreprise \(les neuf premiers numéros correspondent au numéro SIREN d’identification unique de l’entreprise, et les cinq suivants permettent d’identifier l’établissement\).

La base SIRENE a été ouverte en janvier 2017 après l’organisation d’un hackathon, et constitue aujourd’hui une des bases de données les plus consultées et réutilisées. Avant la crise de la Covid19 et la mise en ligne des données épidémiologiques, elle était la troisième base la plus consultée sur le site data.gouv.fr, après le répertoire national des associations \(RNA\) notamment. Les utilisateurs de la base SIRENE sont aussi bien des administrations \(le ministère de l’éducation supérieure, de la recherche et de l’innovation par exemple\) que des entreprises privées \(Ellisphere ou inqom par exemple\). Les legaltechs utilisent notamment la base SIRENE afin de mettre en perspective certaines informations juridiques, et proposer, par exemple, de tirer un panorama de contentieux d’une entreprise. Ce résultat peut être obtenu en croisant la base SIRENE avec d’autres bases. .

Le nombre de réutilisateurs mensuels réguliers est passé de 500 en moyenne avant 2017 à 4 400 depuis l’ouverture, progression concomitante au développement de l’offre par API \(231 millions de requêtes sur dix mois en 2020\) et via des sélections sur différentes critères opérables sur le site SIRENE.fr \(118 000 listes éditées sur 10 mois en 2020\).

**Des modes de diffusion discutés par les réutilisateurs**

L’ouverture de la base SIRENE avait parmi ses objectifs, celui d’augmenter sa qualité via les retours des réutilisateurs de la base. Toutefois, les retours observés par l’INSEE demeurent le fait d’anciens rediffuseurs de la base SIRENE. De plus, l’INSEE n’est pas compétent pour décider des modifications des variables qui relèvent du traitement des formalités d’entreprises : les modifications doivent être déclarées par les entreprises par le biais de formalités déposées dans les CFE. Dans l’ensemble, la qualité générale de la base SIRENE semble aujourd’hui reconnue au sein de la communauté, d’après les auditions conduites par la mission.

Cependant, depuis l’ouverture, les réutilisateurs déplorent plusieurs aspects dans le mode de diffusion de la base et la relation avec l’INSEE. En particulier, plusieurs réutilisateurs déplorent un manque de communication avec l’INSEE et regrettent notamment de ne plus avoir accès à un correspondant à l’INSEE qui leur permettait de faire remonter leurs besoins dans l’ancien système.

Par ailleurs, les modifications substantielles du dispositif de diffusion pour basculer de l’ancien dispositif Syracuse vers la nouvelle offre organisée autour de l’API SIRENE, ont pu créer des difficultés pour certains réutilisateurs. Les deux dispositifs ont été maintenus en parallèle de juin 2018 à avril 2019 pour laisser le temps aux réutilisateurs d’adapter leurs systèmes d’information et d’autres évolutions sont intervenues ultérieurement pour offrir des services complémentaires. L’INSEE est à présent dans une phase de consolidation de l’offre, et d’augmentation de la disponibilité de l’API. Par ailleurs, l’INSEE considère que des activités commerciales de services spécifiques assurés pour un nombre limité d’utilisateurs est incompatible avec le principe d’égalité d’accès aux données gratuites.

Certains utilisateurs regrettent enfin, comme pour les données d’Infogreffe, un manque d’exhaustivité de l’information contenue dans la base, concernant des entreprises individuelles ne souhaitant pas que leurs données soient diffusées pour des motifs de prospection. L’INSEE ne diffuse pas ces données au secteur privé et les réserve aux administrations en ayant l’usage, jugeant que leur accessibilité était contraire aux règles du RGPD.

On peut enfin citer plusieurs marges d’amélioration dans l’exploitation de la base, comme l’interopérabilité avec la base RNA \(l’identifiant RNA n’étant pas systématiquement renseigné dans la base\), et le référentiel d’adresse pour l’interopérabilité avec des bases comme la base adresse nationale \(BAN\) ou le code officiel géographique \(COG\). Sur ce dernier point, l’INSEE souhaiterait au-delà du cas de SIRENE, avoir une base adresse unique, et la DINUM essaie de fédérer l’ensemble des acteurs \(IGN, DGFiP et INSEE\). Actuellement, l’INSEE évalue l’intérêt d’utiliser la BAN pour SIRENE.  


