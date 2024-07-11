---
guid: 120
title: "Test de la serrure connectée Tedee Go + accessoires"
description: "Test complet et integration dans home-assistant de la serrure Tedee Go avec le bridge wifi Tedee et le clavier code accès Tedee"
ref: "Tedee Go"
layout: post
authors: [Nico]
date: 2024-04-22 11:00
last_modified_at: 2024-04-23 13:55
categories: [Tests, Securite, Wifi]
tags: []
video:
image: 'test-serrure-connectee-tedee-go-plus-bridge-digicode.png'
toc: true
beforetoc: ''
published: true
noindex: false
sitemap:
  changefreq: 'monthly'
  exclude: 'no'
  priority: 0.5 #between 0.0 to 1.0, 1.0 high priority
  lastmod:  # date to end modification
locale: fr_FR
comments: true
rating: 3.8
sourcelink:
  - https://www.youtube.com/@tedee5282/videos
  - https://tedee.com/fr/product-info/tedee-go/
  - https://www.home-assistant.io/integrations/tedee/
  - https://www.domadoo.fr/fr/380_tedee?domid=39
---

Une première pour Haade, je vais te présenter une **serrure connectée** fabriqué dans les pays de l'est, **la Tedee Go** avec le **bridge Tedee** qui va bien et pour finir, le **digicode Tedee**. Pour la petite histoire j'ai demandé à Tedee de me fournir la **version Pro** qui a l'air plus alléchante, **mais la marque privilégie cette gamme pour une installation par des professionnels** et trouvait plus pertinent de m'envoyer la Tedee Go orientée grand public. 

{% include product-embed.html guid="2193" %}

> Je trouve ça dommage car **malgré le prix élevé**, elle dispose d'une batterie rechargeable qui possède une autonomie plus importante !

**Merci à l'entreprise Tedee** pour m'avoir fourni une bonne partie de la gamme afin de pouvoir effectuer les test dans de bonnes conditions !

{% picture posts/{{ page.guid }}/test-de-la-gamme-tedee-go-bridge-et-clavier-a-code.png --alt test de l'ensemble de la gamme tedee --img width="940" height="529" %}

La Gamme complète Tedee est [disponible chez notre partenaire **domadoo !**](https://www.domadoo.fr/fr/380_tedee?domid=39){: target="_blank"}

## La serrure {{ page.ref }}

### Déballage

On ne va pas s'étaler sur le sujet car tu trouveras facilement toutes les infos sur le net, Le module tedee go est bien emballé et tu trouveras:

- une serrure connectée avec les piles
- un support pour cylindre ne dépassant pas 3mm à la sortie
- une lingette nettoyante
- une clé allen
- la notice
- le guide en carton avec QRcode

{% picture posts/{{ page.guid }}/contenu-boite-tedee-go.png --alt contenu de la boite de la serrure connectée Tedee Go --img width="940" height="529" %}

### Dimensions et Caractéristiques

{% picture posts/{{ page.guid }}/rendu-face-avant-arriere-alu-tedee-go.png --alt rendu et qualité de la serrure connectée Tedee Go --img width="940" height="529" %}

|Modèle|TLV2.0|
|Poids|196 g|
|Dimensions|Ø 58mm x 65mm|
|Température de fonctionnement|10-40°C (uniquement en intérieur)|
|Humidité de fonctionnement|max. 65%|
|Pays de production|Pologne, UE|
|Alimentation électrique|3x CR123/CR123A pile|
|Autonomie de la batterie|Jusqu'à 6-8 mois pour 8 fonctionnements par jour|
|Sécurité|TLS 1.3|
|Peut être couplé avec|Bridge Tedee, Clavier Tedee|
|Peut être installé sur|cylindres à profil européen, équipés d'un double embrayage (d'urgence)|

**Face à la concurrence**

Niveau dimension ( de face ) je tiens à le préciser, **Tedee Go est très petite**, si tu es prêt à mettre la main au portefeuille la Tedee Pro est encore plus petite. Gros point positif pour la marque. Cependant la profondeur est assez importante *ce qui offre tout de même une bonne prise en main.*

{% picture posts/{{ page.guid }}/comparatif-dimension-serrure-connecte-du-marche.png --alt comparatif dimension de la serrure tedee go face à la concurrence --img width="940" height="267" %}

### Installation et Avantage

Bon tu trouveras toutes les infos sur le web et sur la futur vidéo qui verra le jour prochainement [sur notre chaîne Youtube](https://www.youtube.com/channel/UCcXJ1ZsjEvQxuWJy7gH-A6w){: target="_blank"}.

> Elle s'installe très rapidement et sans effort je te le garantie 👍

{% include videoPlayer.html externalId="https://tedee.com/app/uploads/2023/06/Tedee-GO-Installation-guide-with-and-without-adapter-1-3.mp4?_=1" %}

1. **Conserve ton matériel actuel:** Tu intalleras la Tedee GO en quelques minutes, sur le cylindre actuel, **sans avoir à remplacer la quincaillerie, et le tout sans faire un seul trou.**
2. **Conserve les clés:** Tedee GO est un tourne-clés, **tu n'as pas à remplacer la clé ni à la sciller**, la serrure Tedee GO vient s'emboiter sur la clé. Tu pourras bienentendu ouvrir de l'extérieur avec ta clé traditionnelle.
3. **Clés virtuelles:** Partage l’accès à la maison avec Famille, amis ou locataires. Facilite les accès avec des clés virtuelles dans l’application Tedee, en contrôlant qui entre, quand, combien de temps et à quelle heure.
4. **Votre portier personel:** Détend toi avec des fonctionnalités simples – régle le Tedee GO pour qu’elle se verrouille automatiquement lorsque tu pars ou rentre chez toi.

### les options de la serrure {{ page.ref }} avec l'app

1. verrouiller automatiquement la porte lorsque la serrure est déverouillée
2. verrouiller automatiquement la porte lorsque la serrure est semi verouillée
3. déverouillage automatique lorsque tu es à proximité de la porte ( bluetooth )
4. Loquet ( sans poignée exterieur choisis d'ouvrir la porte entièrement)
5. paramètre le bouton physique de la serrure ( déverouiller/verrouiller, fermeture automatique avec délai, temporisation )
6. calibrage
7. Alerte sur serrure déverouillée
8. Option déverouillage d'urgence

{% picture posts/{{ page.guid }}/option-appli-tedee-go-verrouillage-loquet.png --alt option de la tedee go verrouillage, déverrouillage et loquet --img width="940" height="509" %}

Je me répète à travers ce fil, cette serrure **est un régal** en terme de pose et d'installation. **Tedee signe là un sans faute**. Si tu cherches une serrure sans bricoler et sans avoir fait science-po pour la paramétrer alors **la Tedee Go est faite pour toi** 👍.

{% picture posts/{{ page.guid }}/option-appli-tedee-go-bouton-urgence-alerte.png --alt option de la tedee go parametrage bouton, option d'urgence et notification d'alerte --img width="940" height="509" %}

### Qualité de la {{ page.ref }}

La Poignée de protection du système est teintée d'un gris aluminium, **mais je suis un peu déçu** car ça n'en est pas, **c'est bel est bien du plastique** ABS, probablement un choix pris par l'entreprise et certainement à cause du poids de l'ensemble.

{% picture posts/{{ page.guid }}/qualite-coque-plastique-tedee-go.png --alt qualité de la coque tedee Go en ABS pas ce qu'il y a de mieux --img width="940" height="529" %}

### Le bruit dans tout ça 💩

Alors j'ai un peu regardé sur le web il y a des vidéos ou tu peux entendre cette serrure en fonctionnement, mais personne n'en parle vraiment, pourtant cette serrure est bruyante.

> Si comme moi **t'as des ados à la maison**, la serrure va déclencher en toi de l'eczema ! ...

La vidéo a été prise à environ 60cm de la serrure avec le smartphone, les décibels montent à 70, **chauffe marcel ...**

{% include videoPlayer.html youtubeId="8JQ87AqHA74?si=jta7TXpiGcscEfBU" %}

{% include product-embed.html guid="2194" %}

### La conso des piles

**Cet onglet est amené à être modifié au fil du mois pour avoir un lissage des données plus réels**{: .red}

Le module fonctionne avec 3 piles cr123, ce sont des piles lithium qui sont relativement **onéreuses**. Tu les trouves sur internet entre 2 et 4€ selon la qualité/marque. 
Je suis à **9 jours de fonctionnement**, l'autonomie **est de 94%** avec les piles d'origines.
Le fabriquant donne une durée de vie de **6 à 8 mois** pour une moyenne de 8 fonctionnements par jour sois 4 ouvertures/fermetures.

Mis à part le premier jour je suis en dessous de 8 fonctionnements, d'après les données recueillies **nous serions à 150 jours d'autonomies** ce qui représente 5 mois de fonctionnements sur pile

> Si tu fais de la location saisonnière n'oubli pas de changer régulièrement les piles  pour espérer qu'elles tiennent toute la saison ou forme la conciergerie afin de savoir les changer. !

**Les + du produit:**{: .blue}
- L'application ( difficile de faire mieux )
- l'installation ( super pratique )
- la connectivité Bluetooth
- la qualité de fabrication

**Les - du produit:**{: .red}
- Module sur pile 3 x CR123
- energivore
- poignée en plastique
- très bruyant
- Bridge obligatoire pour la connecter à une domotique externe
- le prix 165€

## Tedee Bridge pour {{ page.ref }}

{% include product-embed.html guid="2195" %}

Le routeur sans fil Tedee Bridge te permet de contrôler la serrure connectée Tedee GO via Internet, et te permet de bénficier de l'API afin de la contrôler facilement via une box domotique, dans mon cas Home-Assistant. **Est-ce nécessaire ! perso si la domotique t'intéresse alors achète le bridge Tedee.**

**Le Bridge est bien fait**,sur l'emballage et la conception rien à dire. T'as pu t'en rendre compte, **il n'y a pas de fil**, mais tu pourrais en rajouter un. D'origine tu emboites le bridge sur la prise et tu la branche. Ensuite tu démarres l'appli et tu suis le guide, 2 minutes après le bridge prendra **en charge la serrure tedee Go** et c'est t.e.r.m.i.n.é.

{% picture posts/{{ page.guid }}/deballage-module-bridge-pour-serrure-connectee-tedee.png --alt Présentation et déballage du bridge pour ouvrir l'accès vers l'extérieur au tedee go --img width="940" height="529" %}

Bon tu le sais **posséder une serrure connectée c'est bien**, l'utiliser avec une application qui soit 100% fonctionnel c'est mieux, mais si t'es comme moi et qu tu utilises plusieurs marques ou protocoles, centraliser l'ensemble dans une seule application, c'est quand même un grand confort. 

**Pour la petite histoire**, un jour un garagiste est venu chez moi pour changer les pneus de la voiture, enfin bref, il s'est mis à parler de son système solaire, et du contrôle, alors j'ai dévié sur la domotique, logique. Et là il commence à sortir le portable et à me montrer diverses applications pour contrôler tout ce qu'il a domotisé. 

> Et je me suis dit punaise comment il fait pour s'en sortir, c'est le smartphone qui doit chauffer !

### Caractéristiques techniques

|Modèle|TBV1.0|
|Poids|51,6g|
|Dimensions|64,5 mm x 63,5 mm x 28 mm|
|Température de fonctionnement|10-40°C (intérieur uniquement)|
|Humidité de fonctionnement|max. 65%|
|Fabriqué en|Pologne, UE|
|Alimentation|5V = 300mA|
|Connexion électrique|Prise de courant (incluse) ou micro USB (câble non inclus)|
|Communication Wi-Fi|**2,4 GHz**|
|Communication Bluetooth|BLE 5.0, 2,4GHz|
|Protocole de sécurité|TLS 1.3|
|Configuration recommandée|max. à 2 m de l'écluse Tedee ; 1-10 m du routeur Wi-Fi|
|Fonctionne avec les systèmes de maison intelligente|Google Assistant, Amazon Alexa, Homey, Fibaro,<br> Grenton, eeDomus, Consolomio<br>Jeedom, Home-Assistant, etc...|

**Les + du produit:**{: .blue}
- installation et intégration extra

**Les - du produit:**{: .red}
- le prix ( 79€ )

> Après la Tedee Go, **le bridge est un régal** en terme d'installation et de configuration dans l'application Tedee. Tu apprécieras cette simplicité !

## Tedee Clavier code d'accès

{% include product-embed.html guid="2196" %}

> Certe ce clavier n'est pas donné, 99€ rien que le prix laisse songeur, mais on continue sur une belle lancée

{% picture posts/{{ page.guid }}/deballage-digicode-pour-serrure-connectee-tedee-go.png --alt contenu de la boite du digicode Tedee Go --img width="940" height="529" %}

Mais franchement **ça reste une découverte intéressante**, d'une qualité remarquable, il fait ce qu'on lui demande, *avec une intégration dans l'application aussi simple que la Tedee Go et Bridge*. Il fonctionne en bluetooth donc il devra être à une certaine distance max de la {{ page.ref }} pour des raisons de couvertures et de sécurité. Le produit est de très bonne fabrication avec des plastiques épais et moulé sur la face arrière.

### Détails du fonctionnement

{% picture posts/{{ page.guid }}/détail-des-fonctions-du-digicode-tedee.png --alt détail de fonctionnement des touches du digicode Tedee Go --img width="940" height="346" %}

- Déverrouillez la porte sans smartphone à l'aide d'un code PIN
- Installation en quelques minutes, alimentation via 3 piles AAA VARTA. Installation avec de la colle ou des vis, même en extérieur.
- Choisis un code de 5 à 8 chiffres et définis, modifie et assigne des codes PIN **via l’appli mobile ou que tu te trouves**
- Gére jusqu’à 100 codes PIN actifs et assignes des codes uniques aux utilisateurs pour un contrôle intégral des accès et de l’historique des activités.
- Enfin Partage les accès simplement en donnant le code PIN logique ! NON !.

**Aucune prise de risque**

Aucune donnée n’est stockée dans le clavier. Il se connecte uniquement à la serrure connectée tedee qui fonctionne au moyen d’un cloud sécurisé.

### Option du digicode Tedee

{% picture posts/{{ page.guid }}/gestion-code-acces-tedee-avec-appli.png --alt Accès aux options du digicode tedee sur l'application officielle --img width="940" height="509" %}

Le digicode Tedee n'est pas en reste côté options tu pourras paramétrer:

- le son
- le rétroéclairage
- activer une notification du bouton sonnette
- le verouillage sans code pin

{% picture posts/{{ page.guid }}/gestion-code-acces-tedee-avec-appli-option-digicode.png --alt Pleins d'options pour le digicode Tedee sons, retroeclairages, notification --img width="940" height="509" %}

Comme je le disais les produits de la gamme Tedee sont très bien faits, l'application regorge d'options paramétrables et c'est un réel plus.

### Caractéristiques

|Modèle|TKV 1.0|
|Poids|120 g (sans piles), 155 g (avec 3 piles AAA)|
|Dimensions|48mm x 135mm x 28mm|
|Alimentation électrique|3 piles AAA incluses|
|Autonomie des piles|selon les indications du fabricant des piles|
|Communication Bluetooth|Bluetooth BLE 5.0 2,4 Ghz|
|Indice de protection IP|IP65|

**Les + du produit:**{: .blue}
- la qualité de fabrication
- les piles fournis
- fonctionnement très pro
- superbe intégration dans l'appli
- installation au mur facile et visses fournis
- change le code à distance

**Les - du produit:**{: .red}
- le prix 99€ ( très cher pour un digicode )

**Alors savoir si ce Digicode t'es utiles ?** 

Oui, si des personnes ( enfants, locataires saisonniers ) doivent avoir la clé et ne possèdent pas de téléphones ou ne veulent pas installer l'application Tedee.

## Notices des produits Tedee

{% include doclink.html pdf="manuel-installation-utilisation-tedee-go-FR.pdf" title="Notice d'installation et manuel d'utilisation du Tedee Go" %}

{% include doclink.html pdf="installation-utilisation-manuel-bridge-tedee-FR.pdf" title="Notice d'installation et manuel d'utilisation du Tedee Bridge" %}

{% include doclink.html pdf="installation-utilisation-code-acces-tedee-FR.pdf" title="Notice d'installation et manuel d'utilisation du Tedee clavier à code d'accès" %}

## L'application Tedee

Google playstore: [Tedee](https://play.google.com/store/apps/details?id=tedee.mobile&hl=fr&gl=US)

Apple AppStore: [Tedee](https://apps.apple.com/fr/app/tedee/id1481874162)

Je suis pas fan de domotiser son habitation à travers de multiples applications, **mais plutôt pour le tout en un** c'est d'ailleurs pour ça que des systèmes comme **Jeedom** ou **Home-assistant** existent, heureusement il y a ces solutions, mais pour l'instant elles ne sont pas aussi complètes que l'application Tedee, Tu pourras quand même contrôler la serrure !

**L'application Tedee est très bien faite**, l'intégration des produits de la marque ne prend que quelques secondes et le paramétrage est simplifié. tout se passe par QRCode et une connection Bluetooth à part la bridge ou un paramétrage wifi est nécessaire ( compatible 2,4 et 5Ghz ), là aussi je n'ai rencontré aucun soucis. À peine ton module reconnu que l'application de propose déjà une mise à jour qui ne prend que quelques secondes et le tout transféré par bluetooth.

> franchement j'ai rarement vu une **application aussi optimisée** et simple d'utilisation.

### Appairage Tedee

Les modules Tedee ( Go, Bridge et digicode ) sont équipés du **Bluetooth** ainsi que des qrcodes sur le produit et sur la notice **pour l'appairage**, seul le digicode ne possède pas de qrcode sur le produit raison de sécurité oblique. À la demande de l'appli scan le qrcode du nouveau produit et il s'intègrera immediatement, **si une mise à jour est disponible elle se fera directement à la vitesse de l'éclair.** ⚡

### Partage d'accès invité

**L'Application sur Smartphone** est bien faite pour générer un accès avec divers paramétrages ainsi que **l'envoi de mails automatiques**, mais *je suis déçu* car la personne **doit télécharger l'appli** pour pouvoir utiliser cet accès, un lien sous formes de boutons à cliquer aurait été plus simple *car si tu fais de la location saisonnière le client sera peut être réticent à installer ce type d'applis.* *Bon il reste toujours le Digicode Tedee qui allègera un peu plus ton portefeuille*.

{% picture posts/{{ page.guid }}/exemple-mail-invitation-serrure-connectee-tedee-go.png --alt mail de partage d'accès à la serrure Tedee Go --img width="940" height="529" %}

**Mais ce n'est pas inéluctable, le portail web** de [Tedee](https://portal.tedee.com/){: target="_blank"} te permettra de peaufiner la gestion des liens ou des code d'accès en fonction d'une ou plusieurs serrures mais aussi en fonctions de diverses organisations et applications de réservations, ça à l'air complet du coup je rédigerai un article spécialement sur la gestion des serrures connectées de la marque Tedee.

{% include product-embed.html guid="2194" %}

## Compatibilité Tedee

### API Tedee

Une API en [perpetuelle évolution disponible ici](https://api.tedee.com/swagger/index.html#/)

{% picture posts/{{ page.guid }}/parametres-bridge-app-tedee-go-et-acces-api.png --alt Accès à l'api sur l'appli pour paramétrer Tedee Go et les logiciels sources externes comme home assistant --img width="940" height="509" %}

La [marque affiche une compatibilité](https://tedee.com/fr/integrations-domotique/?utm_term=&utm_source=adwords&utm_campaign=Reklamy+produktowe+(Francja)&utm_medium=ppc&hsa_acc=3229275490&hsa_cam=17745495747&hsa_grp=&hsa_ad=&hsa_src=x&hsa_tgt=&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=CjwKCAjww_iwBhApEiwAuG6ccPTO6PYLs8TsvjS_pwlJDUcOecnh8vRsJgiHe4mjfkhCQ_X4k1uJaBoCnccQAvD_BwE#technology-section-1){: target="_blank"} avec Google Home, Amazon Alexa, Apple HomeKit ou Homey mais aussi Fibaro, eedomus, Loxone, neuronhouse, Jeedom, Ampio et **Home-Assistant**

> Il vous faudra dans tous ces cas le Tedee Bridge

### avec bridge
- Home-assistant
- Jeedom (plugin 4€)
- Fibaro
- Eedomus
- Loxone
- etc...

## Intégration Home Assistant

Et oui la serrure {{ page.ref }} est partiellement compatible avec home assistant mais pour se faire il te faudra idéalement le bridge mais pas obligatoire, tu pourrais utiliser directement la {{ page.ref }} avec HA par **le biais de homekit si tu possèdes déjà un bridge homekit** mais tu n'auras pas accès à toute les fonctions.

### Avec le bridge Tedee

Une fois le bridge paramétré via l'application officielle Tedee, va dans les paramètres et active l'API. Une fois activée rends toi dans les infos de l'API et récupère la clé Token ainsi que l'adresse IP, [voir la capture ci-dessus](#api-tedee)

Ensuite le reste se passe dans Home-Assistant d'une manière plus que simple clic directement sur le bouton ci-dessous

{% include homeassistantlink.html integration_brand="tedee" %}

Renseigne l'adresse IP ainsi que le token et tu auras directement toutes les infos qui remonteront dans Home assistant ( pour l'instant seul la serrure et le bridge remonteront ), je n'ai pas trop d'inquiétude pour l'intégration des autres composants car l'API est très complète. Tu peux par ailleurs participer au projet d'intégration car il existe une [librairie python](https://pypi.org/project/pytedee-async/){: target="_blank"} d'intégration et le [github correspondant](https://github.com/zweckj/pytedee_async){: target="_blank"}

### Rendu home-assistant et {{ page.ref }}

{% picture posts/{{ page.guid }}/integration-bridget-et-tedee-go-home-assistant.png --alt integration tedee go et bridge dans home assistant --img width="940" height="113" %}

Sur l'application Tedee j'ai un bridge, une Tedee Go et un Digicode d'installé, et actuellement seul le Bridge et la Tedee Go sont reconnus. Le Bridge n'intègre pas de fonctions à contrôler. 
Pour la serrure {{ page.ref }}, tu trouveras la fonction principale de verrouillage ainsi que des infos auxquelles je n'ai pu faire de rapprochement avec l'application Tedee.

- Comme la durée du mécanisme à 2 ( qui devrait être un délai d'ouverture )
- Mécanisme activé ...
- semi verouillé ( bon là il s'agit de l'option sur l'appli).

{% picture posts/{{ page.guid }}/fonctions-disponibles-tedee-go-home-assistant.png --alt fonctions disponibles dans home assistant de la serrure connectée tedee go --img width="940" height="623" %}

Ci-dessous j'ai réalisé un **Gif animé** du fonctionnement du déverouillage et le tout sans passer par le cloud Tedee ( car on utilises l'appel par API ). **Le fonctionnement sous Home Assistant de la {{ page.ref }} est super intéressant.**

Car tu pourras choisir entre déverouiller la poignée **ou** déverouiller avec action sur le loquet, **contrairement à l'appli Tedee** ou il faut sélectionner une option loquet au préalable avant de pouvoir l'utiliser.

![Fonctionnement de la serrure connectée tedee go dans home assistant]({{ site.baseurl}}/assets/images/posts/{{ page.guid }}/fonctionnement-home-assistant.webp{{ cachebuster }}){: width="597" height="679" class="lazyload pictaninpost"}

{% include product-embed.html guid="2193" %}

## Conclusion

**La serrure Tedee Go, le Tedee Bridge et le Digicode, sont des réussites d'installations et d'intégrations dans l'univers de la marque Tedee.** L'ensemble est fabriqué en Europe (Pologne) et c'est une bonne chose. 

La serrure connectée Tedee Go est une **bonne serrure** mais possède **2** points **négatifs**, d'une **elle est bruyante** et de deux elle est **énergivore**.

> Si le bruit est le cadet de tes soucis alors je te conseil serrure intelligente Tedee Go, sinon passe ton tour.

