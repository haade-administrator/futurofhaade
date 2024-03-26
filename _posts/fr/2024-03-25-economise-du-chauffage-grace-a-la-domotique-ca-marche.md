---
guid: 116
title: "Économise du chauffage grâce à la domotique ça marche !"
description: "Dans le cadre d'un nouveau concept vidéo présenté par August sur youtube, je vais te détailler l'installation d'une chaudière au gaz domotisée avec Home Assistant et Sonoff"
ref: ""
layout: post
author: Nico
date: 2024-03-25 11:09
last_modified_at: 
categories: [Haade-lab, Domotique, Zigbee]
tags: []
image: 'fais-des-economies-d-energies-en-domotisant-ton-installation-de-chauffage.png'
toc: true
beforetoc: ''
published: false
noindex: false
sitemap:
  changefreq: 'monthly'
  exclude: 'no'
  priority: 0.5 #between 0.0 to 1.0, 1.0 high priority
  lastmod:  # date to end modification
locale: fr_FR
comments: true
rating:  
sourcelink:
  - https://community.home-assistant.io/t/trv-calibrator-calibrate-your-valve-with-an-external-sensor-probably-trv-agnostic/451424
---
Voilà un article dédié à la domotisation d'une chaudière traditionnelle au gaz avec des radiateurs branchés sur circuits d'eau. La domotisation t'apporteras confort, économie financières et adaptabilité à toute épreuve. Cet article est rédigé pour compléter la vidéo tournée par August et Lulu sur le sujet. Deux compères qui découvrent la domotique et qui te font partager leurs ressentis.
Pour terminer tu pourras te rendre compte que pour un coût minime tu arriveras à faire un retour sur investissement sur deux ans Maximum.

## Prérequis
- une **box domotique** [Home Assistant Green](https://www.domadoo.fr/fr/box-domotique/7046-nabu-casa-box-domotique-home-assistant-green-0794677011758.html?domid=39){: target="_blank"} ou [Sonoff Ihost](https://www.domadoo.fr/fr/box-domotique/6715-box-domotique-ihost-local-zigbee-30-wifi-4gb-sonoff.html?domid=39){: target="_blank"}
- Si tu utilises la Home Assistant Green il te faudra une [clé zigbee Skyconnect](https://www.domadoo.fr/fr/box-domotique/6938-dongle-usb-zigbee-30-skyconnect-pour-home-assistant-nabu-casa-0794677011635.html?domid=39){: target="_blank"}
- des modules thermostatiques [TRV Sonoff](https://www.domadoo.fr/fr/chauffage-clim/6776-sonoff-tete-thermostatique-connectee-zigbee-30.html?domid=39){: target="_blank"} de pref
- des modules [thermostats températures et humidités](https://www.domadoo.fr/fr/chauffage-clim/6732-sonoff-capteur-de-temperature-et-d-humidite-zigbee-30-avec-support-snzb-02p.html?domid=39){: target="_blank"} ( marque **Sonoff** de préférence )
- un module multifonction [Nodon SIN-4-1-20](https://www.domadoo.fr/fr/peripheriques/5688-nodon-module-multifonction-zigbee-nodon-sin-4-1-20-onoff-contact-sec-3700313925188.html?domid=39){: target="_blank"} contact sec (afin de contrôler l'allumage et l'extinction de la chaudière)
- des compétences si t'en as c'est mieux

Il faut savoir qu'en domotique il y a plusieurs façons de faire comme on dit:

> Tous les chemins mènent à Rome

Je vais te détailler les produits utilisés, ainsi que la mise en place sur Home Assistant. À travers une installation des plus limpides, j'ai agrémenté ce mécanisme à l'aide d'automatisations, templates et Blueprint. Ne t'inquiètes pas ce n'est pas si compliqué surtout qu'au fil du temps Home Assistant à su s'adapter et rendre son interface utilisable même aux plus novices d'entres vous.

## Le matériel

Chez August comme il le dit si bien dans sa vidéo, nous avons décidé de partir sur une [box Home Assistant Green](https://www.domadoo.fr/fr/box-domotique/7046-nabu-casa-box-domotique-home-assistant-green-0794677011758.html?domid=39){: target="_blank"} avec un [dongle zigbee Skyconnect](https://www.domadoo.fr/fr/box-domotique/6938-dongle-usb-zigbee-30-skyconnect-pour-home-assistant-nabu-casa-0794677011635.html?domid=39){: target="_blank"} pour contrôler les modules zigbee. Mais tu pourrais aussi partir sur une [box sonoff ihost avec clé zigbee intégré](https://www.domadoo.fr/fr/box-domotique/6715-box-domotique-ihost-local-zigbee-30-wifi-4gb-sonoff.html?domid=39){: target="_blank"} si tu désires domotiser certains aspects de ton logement, attention tout de même aux automatisations qui seront plus délicates à paramétrer. **En effet la box Home assistant green** est compatible avec le gigantesque **univers Home assistant** et de plus tu participes au projet opensource en investissant dans leurs Box et clés, et je trouve ça sympa.

{%- include alert.html type="info" text="Pour info il existe aussi la box <b>Home Assistant Yellow</b> qui inclus la clé Zigbee mais le tarif est plus cher, pour le taf ça reste le même." link="https://www.home-assistant.io/yellow/" textlink="Home Assistant Yellow" %}

Pour les **têtes thermostatiques** nous sommes partis sur le modules **TRV de chez Sonoff**, dans un précéddent [article comparatif Sonoff/Xiaomi/Moes]({% post_url /fr/2024-01-29-comparatif-tete-thermostatique-robinet-zigbee-xiaomi-sonoff-moes %}){: target="_blank"} il se trouve que c'est le Sonoff qui s'en est **le mieux sorti** sur les aspects **esthétiques/fonctionnements/qualité/prix**.

{% include product-embed.html image="sonoff-tete-thermostatique-connectee-zigbee-30.jpg" title="Sonoff TRVZB" brand="Sonoff" description="La tête thermostatique connectée SONOFF Zigbee vous permet de contrôler la température plus précisément avec moins d'énergie, vous offrant ainsi une maison plus confortable." domlink="chauffage-clim/6776-sonoff-tete-thermostatique-connectee-zigbee-30.html" iteadlink="sonoff-zigbee-thermostatic-radiator-valve" affiliate="_DFB4iQZ" %}

{%- include alert.html type="info" text="Pour Info Chez Itead fournisseur officiel Sonoff le module est à <b>26,9$ HT</b> + <b>10%</b> de remises à <b>partir de 3</b> ou <b>10%</b> de remises supplémentaires avec le code <b>HAADESONOFF</b> dès l'achat d'un module, ce qui est <b>exceptionnel</b>" link="https://itead.cc/product/sonoff-zigbee-thermostatic-radiator-valve/ref/122/" textlink="Module Sonoff TRV" %}

Ensuite **il te faudra un module contact-sec** qui commandera la fonction ouvert/fermé de ta chaudière ( Gaz, Fioul et même pompe à chaleur ), il en existe plusieurs sur le marché, j'ai sélectionné le module [Nodon multifonction SIN-4-1-20](https://www.domadoo.fr/fr/peripheriques/5688-nodon-module-multifonction-zigbee-nodon-sin-4-1-20-onoff-contact-sec-3700313925188.html?domid=39){: target="_blank"} car il est de très bonne fabrication, d'ailleurs [tu pourras lire un test à ce sujet]({% post_url /fr/2023-07-31-test-nodon-module-zigbee-1-relais-multifonction-veritable-couteau-suisse %}){: target="_blank"}.

Pour terminer je te conseil **fortement d'équiper chaque pièces d'un micro-module de température,** <ins>Pourquoi:</ins> Le robinet thermostatique est équipé d'un thermostat intégré cependant *la température est faussée en période de fonctionnement du fait de la proximité avec le corps de chauffe*, de plus c'est encore plus pertinant quand tu possèdes deux radiateurs dans la même pièce. 

Tu verras plus bas qu'à l'aide d'un **simple Blueprint** tu pourras demander à Home Assistant de calibrer le thermostat des robinets sur le thermostat de la pièce *c'est un réel plus* 👌.

**Dans la gamme des micro-modules thermostatiques** le choix est vaste, je te conseil encore un module **Sonoff le SNZB-02P**, il est fiable, esthétique et peu cher. [là aussi j'ai testé le Sonof SNZB-02P, n'hésite pas à consulter]({% post_url /fr/2023-08-20-test-capteur-zigbee-temperature-humidite-sonoff-SNZB-02P %}){: target="_blank"}.

{% include product-embed.html image="sonoff-capteur-de-temperature-et-d-humidite-zigbee-30-avec-support-snzb-02p.jpg" title="ZSonoff SNZB-02P" brand="Sonoff" description="Micro-module zigbee température et humidité Sonoff SNZB-02P" iteadlink="sonoff-zigbee-temperature-and-humidity-sensor-snzb-02p" domlink="chauffage-clim/6732-sonoff-capteur-de-temperature-et-d-humidite-zigbee-30-avec-support-snzb-02p.html" affiliate="_DkJNVHx" %}

{%- include alert.html type="info" text="Pour Info Chez Itead fournisseur officiel Sonoff bénéficie de <b>10%</b> de remises supplémentaires avec le code <b>HAADESONOFF</b>" link="https://itead.cc/product/sonoff-zigbee-temperature-and-humidity-sensor-snzb-02p/ref/122/" textlink="Module Température Sonoff SNZB-02P" %}

## Le coût de reviens chez August

1. la box Home-Assistant Green à 99,99€
2. la clé skyconnect à 39,99€
3. les 5 robinets thermostatiques à 27,20€ ttc livré l'unité soit 136€ (ITEAD)
4. Un micromodule Nodon à 39,99€
5. 2 thermostats SNZB-02P à 12,95€ l'unité soit 25,9€ les deux (ITEAD)

**Total:** 341,87€

## La mise en place

Commence par insérer la clé Skyconnect sur la box Home Assistant Green branche le cable rj45 et alimente la box, laisse tourner quelques instants et ensuite connecte toi à l'adresse [http://homeassistant.local:8123](http://homeassistant.local:8123) et oui c'est plug'n play

**Pour plus d'infos** sur ces manipulations j'ai [rédigé un article sur la Home Assistant Green et la clé Skyconnect]({% post_url /fr/2024-02-12-test-box-homeassistant-green-et-cle-zigbee-skyconnect-performance-et-stabilite %}){: target="_blank"}

Ensuite tu as le choix pour la configuration de la clé zigbee soit tu passes par le module ZHA intégré à Home Assistant soit par le module complémentaire Zigbee2mqtt, ça dépend de ta vision des choses en tous cas pour la rédaction de cet article avec les modules mentionnés ZHA et Zigbee2mqtt fonctionnent. Perso j'ai une préférence pour Zigbee2mqtt qui intègre énormément de modules.

Pour l'installer rien de plus simple clic sur le bouton ci-dessous

Et pour paramétrer ta clé va sur les [infos d'installations officielles](https://github.com/zigbee2mqtt/hassio-zigbee2mqtt#installation).


## centraliser les thermostats

{% include homeassistantlink.html blueprint_import="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Frotilho%2Fhome-assistant-blueprints%2Fblob%2Fmain%2Ftrv_calibrator.yaml" %}

## Mode Chauffage

## Créer des moyennes

{% highlight yaml %}
{% raw %}
{% set salon = state_attr('climate.th_salon', 'current_temperature') | float %}
{% set bureau = state_attr('climate.th_bureau', 'current_temperature') | float %}
{{ ((salon + bureau) / 2) | round(2, default=0) }}
{% endraw %}
{% endhighlight %}

## Uniformiser le fonctionnement

{% highlight yaml %}
{% raw %}
{%- set result = state_attr('climate.th_salon', 'running_state') %}
{%- if result == 'heat' %}
{%- set result = 'on' %}
{{ result }}
{%- else %}
{%- set result = 'off' %}
{{ result }}
{%- endif %}
{% endraw %}
{% endhighlight %}

## Automatisation

## Conclusion
