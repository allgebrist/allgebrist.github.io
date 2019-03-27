---
layout: post
title:  "Kausale Dekonvolution durch algorithmische generative Modelle"
date:   2019-03-18
author: Allan Zea
categories: Maschinelles Lernen
tags:	maschinelleslernen
---

Heutzutage produziert die globale Wissenschaft ganz riesige Mengen von Daten, die immer schweriger zu verarbeiten sind und deren Größe sich immer in kürzeren Zeiträumen verdoppelt. Eine der größten Herausforderungen ist es nun, solche Datenmengen auf eine effiziente Weise analysieren zu können.

Kurz gesagt dient unsere Methode dem Zweck, komplexe und vernetzte Datenmengen zu zerlegen, 
um ihre zugrunde liegenden Bestandteile herauszufinden. Solche Bestandteile betrachten wir als 
Kandidatenalgorithmen/Computerprogramme, die die Daten generieren könnten.

Den Informationsbeitrag einer gegebenen Kante $$e$$ zum Graphen $$G$$ kann man also ermitteln, indem man die Differenz $$I(G,e):=C(G)-C(G-e)$$ zwischen den Informationsgehalten von $$G$$ und $$G-e$$ berechnet.
