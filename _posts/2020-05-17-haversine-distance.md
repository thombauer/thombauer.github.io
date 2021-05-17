---
layout: post
title: Implementierung der Haversine-Distanz für Schweizer Postleitzahlen. Von opendata zu Beispielfragestellungen.
cover-img: /assets/img/world.jpg
tags: [data science, geography, python, open data]
---

Jede Schweizer Postleitzahl erfügt neben weiteren beschreibenden Features über eine Zuweisung zu Längen- und Breitengraden. Für einen schnellen Überblick über die Distanz zwischen den offiziellen Koordinaten von zwei Postleitzahlen lässt sich mit der Haversine-Formel schnell ein passendes Resultat errechnen. Die berechnete Distanz kann helfen, räumliche Daten in Maschine-Learning-Modellen als Feature nutzbar zu machen. Aber auch für prinzipiell alle Anwendungen, bei denen ein Set von Längen- und Breitengraden mit einem anderen Set abgeglichen werden soll, sind diese Distanzen nutzbar. Beispielweise könnte man sich alle Wochenmärkte im Umkreis von 50 Kilometern um den eigenen Wohnort ausgeben lassen.

Titel-Image: <span><a href="https://unsplash.com/@louishansel?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Louis Hansel</a> on <a href="https://unsplash.com/s/photos/circle-map?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a></span>
 
## open data

## Haversine Formula

Die Haversine-Formel beschreibt eine Anwendung der sphärischen Trigonometrie, welche die Seiten und Winkel von sphärischen Dreiecken in Beziehung setzt. Die ersten Tabellen mit diesen Werten findet man im frühen 18. Jahrhundert, verwendet wurden sie für die Navigation. Mit der Formel lässt sich die kürzeste Distanz zwischen zwei Punkten auf einer Kugel unter Verwendung ihrer entlang der Oberfläche gemessenen Breiten- und Längengrade berechnen. Die Ergbnisse sind dahingehend nicht perfekt, da die Berechnung die Annahme trifft, dass es sich bei der Erde um eine perfekte Kugel handelt, während sie in Wirklichkeit ein abgeflachter Sphäroid ist. Die Formel lässt sich in vielen Programmiersprachen implementieren, unten sehen wir die Pipeline in Pandas.

<span>Photo by <a href="https://unsplash.com/@seagrave?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Nick Seagrave</a> on <a href="https://unsplash.com/s/photos/swiss-map?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a></span> ![Navigate](/assets/img/navigate.jpg)
