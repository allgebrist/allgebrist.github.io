---
layout: post
title:  "Kausale Dekonvolution durch algorithmische generative Modelle"
date:   2019-03-27
author: Allan Zea
categories: machinelleslernen
tags:	maschinelleslernen
---

Heutzutage produziert die globale Wissenschaft riesige Mengen von Daten, die immer schwieriger zu verarbeiten sind und deren Größe sich immer in kürzeren Zeiträumen verdoppelt. Eine der größten Herausforderungen ist es nun, solche Datenmengen auf eine effiziente und optimale Weise analysieren zu können. Traditionelle Klassifizierungs- und Korrelationsvefahren des maschinellen Lernens spielen in dieser Hinsicht eine wessentliche Rolle, besonders bei Aufgaben bezüglich der Mustererkennung bzw. des Mustervergleichs. Doch bei anderen Aufgaben sind sie in gewisser Maße nicht zuverlässig, z.B. bei Aufgaben, wo es notwendig ist zu entdecken, welche Mechanismen überhaupt erst die in den Daten vorkommenden Muster generiert haben. Dies bedeutet aber nicht, dass traditionelle Methoden im maschinellen Lernen schlecht sind! Es geht nur darum, dass sie nicht mit einigen speziellen Fähigkeiten versehen sind.

In einer Arbeit vom [Algorithmic Dynamics Lab](https://www.algorithmicdynamics.net/), die kürzlich von Nature veröffentlicht wurde [1], versuchten wir mithilfe eines Entfaltungsalgorithmus die oben genannte Beschränkung zu vermeiden. Unser Algorithmus dient dem Zweck, komplexe und vernetzte Datenmengen zu zerlegen, um ihre zugrunde liegenden Bestandteile herauszufinden. Solche Bestandteile betrachten wir als Kandidatenalgorithmen/Computerprogramme, die die Daten generieren könnten. Das folgende Video von Nature ist eine gute Einleitung ins Thema.

<iframe width="668" height="376" src="https://www.youtube.com/embed/rkmz7DAA-t8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>&nbsp;</iframe>

***

### Algorithmische Informationstheorie

Wir beginnen mit einigen grundlegenden Konzepten aus der algorithmischen Informationstheorie. Unsere Darstellung gründet auf den von Andrei N. Kolmogorow eingeführten Komplexitätsbegriff [2]. Die Kolmogorow-Komplexität $$K_{T_U}(w)$$ des Wortes $$w$$ bezüglich einer universellen Turingmaschine $$T_U$$ ist definiert als die Länge des kürzesten Programms $$p$$, das $$w$$ generiert. 

$$ K_{T_U}(w):=\min_{p:T_U(p)=w}|p|. $$

Man kann dieser Definition nach die Kolmogorow-Komplexität eines Objekts einfach als seine kleinste Beschreibung (Computerprogramm, das das Objekt generiert) betrachten. Ist $$T$$ eine beliebige Turingmaschine, so ist $$K_T(w)=K_{T_U}(w)+c_T$$ [3, Satz 2.1], wobei $$c_T$$ eine von $$w$$ unabhängige Konstante ist. Daraus folgt, dass die kürzeste Beschreibung eines beliebigen Objekts bis auf eine Konstante unabhängig von der gewählten Universalprogrammiersprache ist. Diese interessante Eigenschaft und viele anderen findet man in [4].

$$AP(w):=\sum_{p:T_U(p)=w}1/2^{|p|}$$

Den Informationsbeitrag einer gegebenen Kante $$e$$ zum Graphen $$G$$ kann man also ermitteln, indem man die Differenz $$I(G,e):=C(G)-C(G-e)$$ zwischen den Informationsgehalten von $$G$$ und $$G-e$$ berechnet.

## Literatur

[1] H. Zenil, N.A. Kiani, A. A. Zea, J. Tegnér, Causal Deconvolution by Algorithmic Generative Models, Nature Machine Intelligence, vol 1(1), pp. 58-66, 2019.

[2] A. N. Kolmogorow, Three approaches to the quantitative definition of information, Problems of Information Transmission (Russisch: Проблемы передачи информации), vol 1(1), pp. 3-11, 1965.

[3] J. Hromkovic, Theoretische Informatik: Formale Sprachen, Berechenbarkeit, Komplexitätstheorie, Algorithmik, Kommunikation und Kryptographie (5. überarbeitete Auflage). Springer-Vieweg, 2014.

[4] M. Li, P. Vitányi, An Introduction to Kolmogorov Complexity and its Applications (3. Auflage). Springer Texts in Computer Science, 2008.
