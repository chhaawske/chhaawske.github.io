---
layout: post
title: Serwery i klienci HTTP
thumbnail-img: /assets/img/2024-11-14.jpg
tags: [aplikacje webowe]
---

Klient blokujący - IO np. HttpURLConnection, Apache HTTP Client, OkHttp. Wysyłam żądanie czekam na odpowiedź czyli blokuje

Klinet nieblokujący - NIO nonblocking np. Apache Asynch HTTP Client, Netty based, Undertow based



Pytania do zadania przed wyborem klienta HTTP:
- czy mam jakąś pule połączeń i jaki jest jest rozmiar?
- jakie mamy timeouty?
- jaki jest model wątków?
- na jakim wątku działa mój kod?
- jak duża jest pula wątków?
- jak mogę kontrolować pule wątków?
