---
ID: 380
post_title: Microsoft Tech Days 2015 – Jour 2
author:
  - Laurent Claisse
post_date:
  - 2015-03-09 16:21:00
post_excerpt:
  - |
    <p>Moins d'annonces d'évolutions .NET, une journée plus orientée architecture.</p> <p><img src="/public/_Claisse/tech-days-2015-2/tech-days-2015.png" alt="tech-days-2015.png" /><br /></p>
layout: post
permalink:
  - ""
published: true
slide_template:
  - default
---
Moins d'annonces d'évolutions .NET, une journée plus orientée architecture.

<!--more-->

<img class=" aligncenter" src="/wp-content/uploads/2015/07/tech-days-2015.png" alt="tech-days-2015.png" />
<h3>Sécurité, cloud, et données privées</h3>
Cette présentation est en deux parties: les questions générales, puis le positionnement Azure
<h4>Axes d'analyse des risques</h4>
Commençons par une classification des différents types de Cloud, basée sur là où s'arrête la responsabilité du fournisseur:
<ul>
	<li>IaaS: Le client achète des VMs (exemple typique: Digital Ocean) et est responsable du déploiement de tous les composants logiciels et applications</li>
	<li>PaaS: Le fournisseur met à disposition la couche middleware (ex: serveurs Apache), l'utilisateur n'a plus qu'à déployer ses applications (exemple typique: Cloudbees). L'utilisateur a moins de responsabilités qu'avec une IaaS, mais dans certains cas cette facilité peut devenir un inconvénient (migrations forcées).</li>
	<li>SaaS: Le fournisseur prend en charge toute la stack, du matériel aux applications. L'utilisateur est un simple consommateur (exemple typique: Salesforce).</li>
</ul>
Les principaux risques du passage au Cloud sont:
<ul>
	<li>sécurité</li>
	<li>protection des données</li>
	<li>conformité légale/réglementaire (compliance)</li>
</ul>
Les risques encourus par les données sont évidemment différents selon qu'elles soient publiques, internes, ou confidentielles.
<h4>Le positionnement Azure</h4>
MS se positionne comme vendeur de tous les types de cloud: public, privé, hybride. Comment entendent-ils se différencier? Leur argumentaire est fondé sur les éléments suivants:
<h5>Conformité aux standards</h5>
Et en particulier ISO 27018. J'avoue ne pas être à même de juger de la pertinence de cet argument. Certains standards ne prouvent pas grand-chose sur la qualité du service fourni par les entreprises (par exemple ISO 9001 est souvent un argument commercial alors qu'il concerne la gestion interne de l'entrprise).

D'un autre côté Azure est de toute façon de bonne facture technique. Mais on peut quand même avoir des surprises, par example le SqlServer Azure a des limitations qui font échouer des scripts d'import fonctionnant sur SqlServer natif. Dans l'ensemble Azure est une offre très compétente techniquement, pas d'inquiètude à ce sujet. Attention quand même à bien comprendre les implications du SLA (calculer l'indisponibiité consécutive maximale admise, et imaginer qu'elle se produise pendant la période d'activité maximale - Noël par exemple pour du e-commerce), car à moins d'être un VIP, le SLA peut être à double tranchant.
<h5>Transparence</h5>
On peut par exemple savoir précisément où sont hébergées nos données. D'autre part MS s'affiche comme simple sous-traitant des traitements, et promet par exemple à ce titre de ne pas utiliser les données à ses fins propres.

Enfin, l'intervenant aborde spontanément LA question à laquelle tout le monde pense: quid du fait que le gouvernement américain prétend désormais accéder aux données hébergées par des entreprises US, même si elles sont stockées en Europe, sans avoir à passer par les voies normales de la coopération internationale?

MS a récemment refusé de transmettre les données demandées par un juge de New York, et plus généralement les entreprises américaines s'inquiètent de la perte de confiance provoquée par ces exigences. La procédure judiciaire est encore en cours (mon pifomètre: MS va gagner).

Par contre, la louable résistance de MS concerne une demande provenant du circuit judiciaire normal (et donc publique..). Qu'en est-il des demandes provenant des procédures d'exception, qui elles restent secrètes? (FISA court, national security letters, révélations Snowden).

Sur ce sujet, autant l'entreprise française lambda peut à mon avis utiliser Azure sans paranoïa, autant il n'est (par exemple) pas envisageable qu'une entreprise du secteur de la défense en fasse de même. Une entreprise en compétition avec une entreprise US ne devrait-elle pas se méfier? Ou se situe la frontière?
<h3>Makers + IOT : une nouvelle révolution industrielle?</h3>
Le logiciel s'insinue partout aussi irrésistiblement que l'eau. D'un autre côté, les programmeurs fabriquent de plus en plus d'objets physiques. Ce double mouvement va-t-il conduire à des changements profonds, et dans quel sens?
<h4>Le mouvement des Makers</h4>
Le premier orateur est l'organisateur de Makers Faire France. Maker Faire Paris 2015 <a href="http://www.makerfaireparis.com/presentation/foire-des-paris/">se tiendra les 2 &amp; 3 mai lors de la 111e édition de Foire de Paris</a>

Le terme "makers" désigne la fabrication à petite échelle, par des individus ou des petits groupes. Si ce mouvement est en train d'exploser, c'est grâce à la démocratisation de quelques technologies clef depuis quelques années:
<h4>Les technologies clefs</h4>
<h5>L'impression 3D</h5>
Elle permet de produire des objets en plastique sans avoir besoin d'un moule, qui est très coûteux. Cela rend possible la fabrication de faibles volumes, impossible à amortir sinon.
<h5>Les cartes de prototypage</h5>
Les Arduino et RaspberryPi sont bien connues des programmeurs. Leur petit prix et leur faible encombrement permet de les embarquer dans des objets physiques de petite taille.
<h5>La combinaison des deux</h5>
Parmis ces utilisations on peut citer la domotique et la robotique. Un des meilleurs examples est le Français Gaël Langevin et son <a href="http://www.inmoov.fr/project/">robot InMoov</a>, fabriqué par impression 3D et contrôlé par un simple Arduino.

<img style="margin: 0 auto;" src="/wp-content/uploads/2015/07/.inmoov_s.jpg" alt="inmoov.jpg" />

Nicolas Huchet, amputé d'un bras, a désormais <a href="http://bionico.org/inde-techfest-bombay-2-3-4-janvier-2015/">un bras bionique</a> low-cost fabriqué avec cette technologie:

<img style="margin: 0 auto;" src="/wp-content/uploads/2015/07/.bionic-hand_s.jpg" alt="bionic-hand.jpg" />
<h4>Les lieux</h4>
Traditionnellement, les Fab labs sont des lieux communautaires mis à disposition gratuitement (mais forcément avec les contraintes de partage associées). Ils peuvent être d'associations, d'universités, d'entreprises, ..

Un autre type de lieux, payant celui-là, existe désormais: les Tech shops, dont parle le deuxième intervenant (<a href="http://usine.io/">Usine IO</a>). Il peut s'avérer par exemple plus adéquat pour une entreprise ne souhaitant pas partager son travail.
<h4>Les places de marché</h4>
A part les salons, les places de marché sont surtout sur internet. Evidemment les makers qui n'ont pas les moyens d'investir dans un moule de production plastique peuvent encore moins avoir une boutique physique. Quelques exemple montrent que ce marché existe également:
<ul>
	<li><a href="de.dawanda.com">de.dawanda.com</a></li>
	<li><a href="www.etsy.com">www.etsy.com</a></li>
	<li><a href="www.alittlemarket.com">www.alittlemarket.com</a></li>
	<li><a title="https://www.tindie.com/" href="https://www.tindie.com/">https://www.tindie.com/</a></li>
	<li>ebay..</li>
	<li>amazon</li>
</ul>
En Europe, le mouvement était plutôt originaire d'Italie, mais il va probablemnt exploser cette année, j'irai probablement à la pêche aux idées porte de Versailles.
<h3>Analyser sa maison à l'aide de Apache Storm: Big data en temps réel</h3>
Certains domaines métier nécessitent une analyse big data en temps réel:
<ul>
	<li>gestion des stocks</li>
	<li>détection de fraudes</li>
	<li>gestion des bouchons</li>
	<li>..</li>
</ul>
Les technologies mises en oeuvres sont proches quelque soit le domaine, cette présentation prend un exemple volontairement simpliste de suivi d'indicateurs domotiques pour les illustrer.

Cette présentation a battu le record du nombre de technologies au mètre carré, je ne peux donc pas tout détailler, mais je vais essayer de reprendre les idées les plus intéressantes.
<h4>Matériel</h4>
<img title="raspberry" src="/wp-content/uploads/2015/07/rasp-logo.png" alt="raspberry" />

Le capteur de température/hygrométrie est un Enocean, car cette marque a l'avantage d'être sans fil, sans pile, et d'être bien documentée. Il envoie à intervalle régulier ces informations à un Raspberry Pi local. Chaque maison est donc équipée d'un capteur Enocean et d'un Raspberry. Le raspberry héberge une application Node.js qui transmer les données des capteurs vers les traitements.

&nbsp;
<h4>Architecture initiale</h4>
Dans le prototype initial, l'application Node.js envoyait les données vers un serveur central, qui réalisait les traitements et exposait une application web pour consulter les résultats. Mais cette architecture:
<ul>
	<li>N'est pas scalable</li>
	<li>Ne protège pas contre la perte d'informations (ne serait-ce qu'en cas de reboot du serveur).</li>
</ul>
<h4>Queue de messages</h4>
Dans l'architecture présentée, l'application Node.js n'envoie plus directement vers le serveur de traitement mais vers une queue Azure Event Hub, qui:
<ul>
	<li>Stocke les messages, ce qui permet d'éviter la perte de données</li>
	<li>Peut recevoir jusqu'à 10^6 événements par seconde, et ne constitue donc pas un goulot d'étranglement</li>
</ul>
Cette queue est pollée par l'étage suivant de l'architecture, Apache Storm.
<h4>Apache Storm</h4>
Storm est un système de traitement en temps réel distribué (master node/worker nodes comme hadoop). <img src="/wp-content/uploads/2015/07/apache-storm.png" alt="apache-storm.png" />

Une chaîne de traitement est un graphe qui connecte des primitives Storm:
<ul>
	<li>Un tuple est un quanta de données; ici les tuples contiennent les mesures relevées par les capteurs</li>
	<li>Un Stream est un stream infini de tuples</li>
	<li>Un Spout est une source de streams; ici il y a 1 spout, qui polle la queue Azure Event Hub</li>
	<li>Un Bolt est un processeur de stream; ici le premier Bolt de la chaîne est un parseur, qui transforme un Stream de JSON en Stream d'objets</li>
	<li>Une topologie connecte les Spouts et les Bolts:</li>
</ul>
<pre class="java code java" style="font-family: inherit;"><span style="color: #000000; font-weight: bold;">protected</span> StormTopology buildTopology<span style="color: #009900;">(</span>EventHubSpout eventHubSpout, SimpleHBaseMapper mapper<span style="color: #009900;">)</span> <span style="color: #009900;">{</span>   TopologyBuilder topologyBuilder <span style="color: #339933;">=</span> <span style="color: #000000; font-weight: bold;">new</span> TopologyBuilder<span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #339933;">;</span>   <span style="color: #666666; font-style: italic;">// Name the spout 'EventHubsSpout', and set it to create</span> <span style="color: #666666; font-style: italic;">// as many as we have partition counts in the config file</span> topologyBuilder     .<span style="color: #006633;">setSpout</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"EventHub"</span>, eventHubSpout, spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">setNumTasks</span><span style="color: #009900;">(</span>spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span><span style="color: #339933;">;</span>   <span style="color: #666666; font-style: italic;">// Create the parser bolt, which subscribes to the stream from EventHub</span> topologyBuilder     .<span style="color: #006633;">setBolt</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"Parser"</span>, <span style="color: #000000; font-weight: bold;">new</span> ParserBolt<span style="color: #009900;">(</span><span style="color: #009900;">)</span>, spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">localOrShuffleGrouping</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"EventHub"</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">setNumTasks</span><span style="color: #009900;">(</span>spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span><span style="color: #339933;">;</span>   topologyBuilder     .<span style="color: #006633;">setBolt</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"DeviceData"</span>, <span style="color: #000000; font-weight: bold;">new</span> DeviceDataBolt<span style="color: #009900;">(</span><span style="color: #009900;">)</span>, spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">fieldsGrouping</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"Parser"</span>, <span style="color: #0000ff;">"dataDeviceStream"</span>, <span style="color: #000000; font-weight: bold;">new</span> Fields<span style="color: #009900;">(</span><span style="color: #0000ff;">"timestamp"</span>, <span style="color: #0000ff;">"deviceid"</span>, <span style="color: #0000ff;">"datas"</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">setNumTasks</span><span style="color: #009900;">(</span>spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span><span style="color: #339933;">;</span>   topologyBuilder     .<span style="color: #006633;">setBolt</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"Average"</span>, <span style="color: #000000; font-weight: bold;">new</span> AverageBolt<span style="color: #009900;">(</span><span style="color: #009900;">)</span>, spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">fieldsGrouping</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"Parser"</span>, <span style="color: #0000ff;">"averageStream"</span>, <span style="color: #000000; font-weight: bold;">new</span> Fields<span style="color: #009900;">(</span><span style="color: #0000ff;">"timestamp"</span>, <span style="color: #0000ff;">"deviceid"</span>, <span style="color: #0000ff;">"datas"</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">setNumTasks</span><span style="color: #009900;">(</span><span style="color: #cc66cc;">1</span><span style="color: #009900;">)</span><span style="color: #339933;">;</span>   topologyBuilder     .<span style="color: #006633;">setBolt</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"Alert"</span>, <span style="color: #000000; font-weight: bold;">new</span> AlertBolt<span style="color: #009900;">(</span><span style="color: #009900;">)</span>, spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">fieldsGrouping</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"Parser"</span>, <span style="color: #0000ff;">"alertStream"</span>, <span style="color: #000000; font-weight: bold;">new</span> Fields<span style="color: #009900;">(</span><span style="color: #0000ff;">"timestamp"</span>, <span style="color: #0000ff;">"deviceid"</span>, <span style="color: #0000ff;">"datas"</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">setNumTasks</span><span style="color: #009900;">(</span>spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span><span style="color: #339933;">;</span>   <span style="color: #666666; font-style: italic;">// Create the HBase bolt, which subscribes to the stream from Parser</span> topologyBuilder     .<span style="color: #006633;">setBolt</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"HBase"</span>, <span style="color: #000000; font-weight: bold;">new</span> HBaseBolt<span style="color: #009900;">(</span><span style="color: #0000ff;">"SensorData"</span>, mapper<span style="color: #009900;">)</span>.<span style="color: #006633;">withConfigKey</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"hbase.conf"</span><span style="color: #009900;">)</span>, spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">fieldsGrouping</span><span style="color: #009900;">(</span><span style="color: #0000ff;">"Parser"</span>, <span style="color: #0000ff;">"hbasestream"</span>, <span style="color: #000000; font-weight: bold;">new</span> Fields<span style="color: #009900;">(</span><span style="color: #0000ff;">"timestamp"</span>, <span style="color: #0000ff;">"deviceid"</span>, <span style="color: #0000ff;">"datas"</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span>     .<span style="color: #006633;">setNumTasks</span><span style="color: #009900;">(</span>spoutConfig.<span style="color: #006633;">getPartitionCount</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #009900;">)</span><span style="color: #339933;">;</span>   <span style="color: #000000; font-weight: bold;">return</span> topologyBuilder.<span style="color: #006633;">createTopology</span><span style="color: #009900;">(</span><span style="color: #009900;">)</span><span style="color: #339933;">;</span> <span style="color: #009900;">}</span></pre>
Le code est <a title="disponible sur GitHub" href="https://github.com/DCubeLabs/Techdays2015">disponible sur GitHub</a>.
<h4>Lambda architecture</h4>
<img src="/wp-content/uploads/2015/07/lambda-archi.png" alt="lambda-archi.png" /> Cette architecture consiste en gros à réaliser à la fois un traitement en temps réel et un archivage des données moyennées. Ici le terme lambda n'a rien à voir avec les lambdas de la programmation fonctionnelle.

Les deux pattes du lambda évoquent plutôt le double aiguillage des données d'entrée:
<h5>Traitement temps réel</h5>
Le Bolt d'alerte envoie par websocket des notifications lorsque événement anormal est détecté
<h5>Traitement différé</h5>
Un Bolt moyenne les mesures par groupe de 10 tuples. Le Bolt de stockage archive ensuite dans HBase.
<h4>Production de dashboards</h4>
Hive et HBase sont intégrés, ce qui permet d'utiliser des requêtes HiveQL pour requêter les données stockées dans HBase. Le front présente les résultats de ces requêtes avec utilise Google Charts et D3.js
<h3>Applications multiplateformes avec Cordova, HTML 5, et JS</h3>
<img style="float: left; margin: 0 1em 1em 0;" title="cordova" src="/wp-content/uploads/2015/07/cordova-logo.png" alt="cordova" />

Cordova est l'ex PhoneGap, donné à la fondation Apache. Il va plus loin que ce dernier avec une interface CLI assez simple, illustrée par la demo:
<ul>
	<li>cordova create &lt;projet&gt;</li>
	<li>cordova platform add android</li>
	<li>cordova platform add browser</li>
	<li>cordova run browser</li>
	<li>..</li>
</ul>
Cordova utilise WebView sur android et ios, mais est supporté nativement sur windows phone.

Les fonctionnalités spécifiques au mobile nécessite l'installation d'un plugin. Sans IDE, l'installation d'un plugin se fait en recherchant le plugin sur internet puis en utilisant la CLI: cordova plugin add org.apache.cordova.camera

Visual Studio a un bon support de Cordova:
<ul>
	<li>installe tout (le SDK android, java, ..)</li>
	<li>pas besoin de chercher le nom des plugins sur internet</li>
	<li>fournit un émulateur android</li>
	<li>debug à partir d'un seul outil (mais sur ios, nécessite l'installation de vs-mda-remote)</li>
	<li>tout cela intégré avec l'utilisation de Typescript</li>
</ul>