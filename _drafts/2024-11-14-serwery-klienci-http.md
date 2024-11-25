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


ograniczenia w problem c10k równoległych połączeń
- max liczba połączeń możliwych do zestawienia bo w linuxie połączenie jest plikiem (file descriptorem) i mamy na nie limity dla ubuntu default to 1024 tylko połączenia są nie tylko na wejściu ale również między warstwami aż do bazy danych więc ta pula staje się automatycznie mniejsza i 1024 połączenia nie przełożą się na 1024 różnych klientów naszej aplikacji 
w linuxie /proc/1234/limits pokazuje np. limit file descriptorów