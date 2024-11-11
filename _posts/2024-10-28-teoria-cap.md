---
layout: post
title: Teoria CAP
thumbnail-img: /assets/img/2024-10-28.jpg
tags: [systemy rozproszone]
---

Teoria CAP opisuje ograniczenia jakie występują podczas projektowania systemów rozproszonych. Ograniczenia te wynikają, że nie można mieć jednocześnie zapewnionej spójności (C), dostępności (A) i odporności na podział sieci (P). Przekłada się to ostatecznie, że możemy mieć maksymalnie spełnione jedną cechę dodatkowo gdy chcemy mieć zapewnioną odporność na podział sieci, która dla systemów rozproszonych jest kluczowa. Jest to oczywiście kombinacja AP i CP. Gdy chcemy zapewnić spójność i odporność na podział sieci najczęściej staramy się odseparować węzły, które nie mają komunikacji z resztą wezłów od możliwości zapisu do nich tak aby tylko zapis dokonywany był w tych węzłach, które się z sobą komunikują. CP najlepiejsz będzie się sprawdzać w systemach bankowych czy finansowych. Dla opcji AP godzimy się na tymczasową niespójność bo dostępność jest dla nas najważniejsza i zgadzamy się na ostateczną spójność dla systemu czyli wszystkie niespójności rozwiązujemy gdy siec zostanie przywrócona do działania. Dobrymi przykładami takich systemów to aplikacje społecznościowe czy sklepy internetowe.