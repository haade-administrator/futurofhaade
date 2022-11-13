---
guid: 27
title: "Domotiser simplement l'allumage de la lumière de la piscine"
description: "Ewelink propose un module à 11€ avec puce zigbee qui nous permet de domotiser la lumière traditionnelle d'une piscine"
layout: post
author: Nico
date: 2022-11-07 22:00
last_modified_at: 
categories: [Domotique, Haade-lab, Home-Assistant]
tags: []
image: 'domotiser-lumière-piscine-traditionnelle-zigbee-ewelink.jpg'
toc: true
beforetoc: ''
published: false
sitemap:
  changefreq: 'monthly'
  exclude: 'no'
  priority: 0.5 #between 0.0 to 1.0, 1.0 high priority
  lastmod:  # date to end modification
locale: fr_FR
comments: true
rating:  
---

## Intro

{% include product-embed.html image="1-600x600.jpg" title="Module relais 1 zigbee 7-32v" brand="Ewelink" description="Module 1 relais zigbee eweling pour domotiser moteur ou lumière 7-32v" affiliate="_DCX0fWX" %}

Voilà une présentation d'un petit module à 7€ qui sans le rappeler fait penser à un petit [tuto de domotisation d'une porte de garage pour 5€]({% post_url /fr/2021-05-19-domotiser-sa-porte-de-garage-pour-5€ %}).
La grande nouveauté de cet article c'est le fait que Ewelink produise un module équivalent intégrant le protocole Zigbee 3.0 et en plus ils embarquent le RF 433 Mhz dispo à la vente avec une télécommande pour ceux qui le désirent.

## Prérequis
- Une piscine avec une ampoule traditionnelle ( donc une vieille piscine 🤪 )
- Une box domotique sous home-assistant
- le module Zigbee2mqtt intégré à HA
- Un module Ewelink simple relais dispo ici.
- toucher un minimum en éléctricité.

## l'avantage du module

Grâce à son large spectre d'alimentation usb 5v et 7-32v
on peut domotiser facilement tout ce qui est commandé par moteur électrique dans la maison
- moteur de portail
- porte de garage
- lumière de piscine
- etc...

On peut le commander sans hub domotique grâce à la fréquence radio et à la télécommande ( en option )

## Schéma des connectiques

- Relais AC-DC 30v-230-
- alimentation micro usb 5v
- alimentation filaire 7-32v
- bouton-switch manuel
- bouton d'appairage
- led de fonctionnement et du relais
- antenne RF-433Mhz

{% picture posts/{{ page.guid }}/detail-relais-ewelink-zigbee.jpg --alt détail relais ewelink zigbee --img width="820" height="820" %}

{% include product-embed.html image="1-600x600.jpg" title="Module relais 1 zigbee 7-32v" brand="Ewelink" description="Module 1 relais zigbee eweling pour domotiser moteur ou lumière 7-32v" affiliate="_DCX0fWX" %}



