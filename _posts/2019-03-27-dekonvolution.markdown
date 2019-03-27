---
layout: post
title:  "Kausale Dekonvolution durch algorithmische generative Modelle"
date:   2019-03-18
author: Allan Zea
categories: Maschinelles Lernen
tags:	maschinelleslernen
---

Kurz gesagt dient unsere Methode dem Zweck, komplexe und vernetzte Datenmengen zu zerlegen, 
um ihre zugrunde liegenden Bestandteile herauszufinden. Solche Bestandteile betrachten wir als 
Kandidatenalgorithmen/Computerprogramme, die die Daten generieren könnten.

Den Informationsbeitrag einer gegebenen Kante $$e$$ zum Graphen $$G$$ kann man also ermitteln, indem man die Differenz $$I(G,e)=C(G)-C(G-e)$$ zwischen den Informationsgehalten von $$G$$ und $$G-e$$ berechnet.
