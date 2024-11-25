---
layout: post
title: Wątki i pule wątków
thumbnail-img: /assets/img/2024-11-13.jpg
tags: [współbieżność]
---

Nie korzystać z new Thread(), tylko z Executors.newFixedThreadPool();

var executor = new ThreadPoolExecutor(1, 2, 3L, TimeUnit.SECONDS, null);
executor.prestartAllCoreThreads(); //żeby się nie wygrzewało tylko wystartować pule szybciej

jak coś jest async z pudełka to trzeba zobaczyć co jest w tym pudełku bo mogą być niespodzianki


