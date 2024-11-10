---
layout: post
title: Algorytmy load balancingu
tags: [wydajność]
---

Load balancing zarządzaniem ruchem sieciowym w sposób statyczny i dynamiczny.

Statycznie:
- round robin - żądania są wysyłane do różnych serwisów sekwencyjnie
- sticky round robin - żądania od 1 usera zawsze trafiają do tego samego seriwsu
- weighted round robin - ręczne przydzielenie wag dla poszczególnych serwisów i kierowanie proporcjonalnie więcej żądań do serwisu o największej wadze 
- hash - IP/URL są hashowane i przydzielane do serwisów na podstawie tych hashy

Dynamicznie:
- least connections - żądania wysyłane są do miejsca o najmniejsz liczbie połączeń
- least response time - żądania wysłane są do serwisu o najkrótyszym czasie odpowiedzi
