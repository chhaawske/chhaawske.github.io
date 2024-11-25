---
layout: post
title: Różnica miedzy Kafka i RabbitMQ
thumbnail-img: /assets/img/2024-11-11.jpg
tags: [systemy rozproszone]
---

Kafka charakteryzuje się większą wydajnością na dużą skalę przez co bardzo dobrze sprawdza się w przetwarzaniu dużych zbiorów danych w czasie rzeczywistym. RabbitMQ nastawiony jest natomiast na integracje usług miedzy sobą przez co zapewnia niską latencję. Główną różnicą jest ilość wiadomości obsługiwana w ciągu 1 sekundy. Dla RabbitMQ jest to max 10,000 wiadomości a dla Kafka to 1,000,000 wiadomosci na sekundę. RabbitMQ ma ograniczania w skalowalności, podczs gdy Kafka bardzo dobrze się skaluje. Kafka domyślnie przechowuje wiadomości na dysku twardym, RabbitMQ nie ma takiego założenia. RabbitMQ jest jednak uznawany za bardziej niezawodne narzędzie w porównaniu do Kafki.