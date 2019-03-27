---
layout: post
title:  "Kausale Dekonvolution durch algorithmische generative Modelle"
date:   2019-03-18
author: Allan Zea
categories: Maschinelles Lernen
tags:	maschinelleslernen
---

Heutzutage produziert die globale Wissenschaft ganz riesige Mengen von Daten, die immer schweriger zu verarbeiten sind und deren Größe sich immer in kürzeren Zeiträumen verdoppelt. Eine der größten Herausforderungen ist es nun, solche Datenmengen auf eine effiziente und optimale Weise analysieren zu können. Traditionelle Klassifizierung- und Korrelationsvefahren des maschinellen Lernens spielen in dieser Hinsicht eine wessentliche rolle, besonders bei Aufgaben bezüglich der Mustererkennung bzw. des Mustervergleichs. Doch bei anderen Aufgaben sind sie in gewisser Maße nicht zuverlässig, z.B. bei Aufgaben, wo es notwendig ist zu entdecken, welche Mechanismen überhaupt erst die in den Daten vorkommenden Muster generiert haben. Das bedeutet natürlich nicht, dass traditionelle Methode im maschinellen Lernen schlecht sind! Es geht nur darum, dass sie mit einigen speziellen Fähigkeiten nicht versehen sind.

Kurz gesagt dient unsere Methode dem Zweck, komplexe und vernetzte Datenmengen zu zerlegen, 
um ihre zugrunde liegenden Bestandteile herauszufinden. Solche Bestandteile betrachten wir als 
Kandidatenalgorithmen/Computerprogramme, die die Daten generieren könnten.

Den Informationsbeitrag einer gegebenen Kante $$e$$ zum Graphen $$G$$ kann man also ermitteln, indem man die Differenz $$I(G,e):=C(G)-C(G-e)$$ zwischen den Informationsgehalten von $$G$$ und $$G-e$$ berechnet.
