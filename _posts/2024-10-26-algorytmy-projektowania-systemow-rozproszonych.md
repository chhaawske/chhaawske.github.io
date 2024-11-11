---
layout: post
title: Algorytmy projektowania systemów rozproszonych
thumbnail-img: /assets/img/2024-10-26.jpg
tags: [systemy rozproszone]
---

1. Consistent Hashing
Jest to technika stosowana w rozproszonych systemach do równomiernego rozkładania danych na serwerach. W tradycyjnym haszowaniu zmiana liczby serwerów wymagałaby przepisania wszystkich danych, ale w consistent hashing zmiana liczby serwerów wpływa jedynie na część danych. W systemie reprezentowanym przez pierścień, serwery (nazywane węzłami) i dane są przypisywane do punktów na pierścieniu. Kiedy dodajemy lub usuwamy serwer, tylko niewielka liczba danych musi być przemieszczona. Przykład: CDN

2. MapReduce
Model używany do przetwarzania dużych zbiorów danych na klastrach komputerów. Działa w dwóch fazach:
Map gdy dane wejściowe są dzielone na części, a każda część jest przetwarzana równolegle, tworząc pary klucz-wartość.
Reduce gdzie wyniki z fazy Map są agregowane na podstawie kluczy.
Przykład: wyszukiwanie informacji w dużych zbiorach danych

3. Distributed Hash Tables (DHT)
To rozproszona struktura danych umożliwiająca przechowywanie i wyszukiwanie informacji w rozproszonym środowisku. W DHT każdy węzeł przechowuje część danych i odpowiada za znajdowanie danych w systemie. Jednym z najpopularniejszych protokołów DHT jest Chord, który używa consistent hashing do przydzielania kluczy do węzłów. Przykład: sieci P2P

4. Bloom Filters
To struktura danych stosowana do sprawdzania, czy dany element należy do zbioru. Bloom filter pozwala na sprawdzenie obecności elementu z pewnym ryzykiem błędu (może dawać fałszywe pozytywy), ale nigdy nie zwraca fałszywych negatywów. Jest bardzo efektywny pamięciowo, dlatego często używany jest w systemach bazodanowych i sieciach komputerowych.

5. Two-phase commit (2PC)
Jest to protokół stosowany w bazach danych do zapewnienia spójności transakcji w rozproszonym systemie. Składa się z dwóch faz:
Prepare gdy koordynator sprawdza, czy wszystkie węzły są gotowe na wykonanie transakcji.
Commit/Rollback gdy wszystkie węzły są gotowe, koordynator wysyła polecenie commit (zatwierdzenie); w przeciwnym razie wysyła polecenie rollback (wycofanie). 2PC zapewnia spójność, ale jest podatny na blokady w przypadku awarii.

6. Paxos
Paxos to algorytm konsensusu, który pozwala rozproszonym systemom osiągać zgodność w sytuacji, gdy niektóre węzły mogą zawieść. Paxos zapewnia, że wszystkie węzły w systemie osiągną zgodę co do jednej wartości. Jest często stosowany w systemach, gdzie wymagana jest odporność na awarie.

7. Raft
Raft to alternatywny do Paxos algorytm konsensusu, który jest łatwiejszy do zrozumienia i implementacji. Raft wykorzystuje mechanizm wyboru lidera do koordynowania decyzji między węzłami. Jest popularny w systemach rozproszonych, takich jak Kubernetes, gdzie potrzebna jest spójność.

8. Gossip Protocol
Protokół gossip jest wykorzystywany do wymiany informacji między węzłami w sieciach rozproszonych. Węzły losowo wybierają inne węzły, z którymi dzielą się informacjami, co pozwala na szybkie rozprzestrzenianie się informacji po całej sieci. Gossip jest często stosowany do monitorowania statusu węzłów i propagacji danych w dużych klastrach.

9. Chord
Chord jest protokołem DHT, który używa consistent hashing do mapowania kluczy na węzły w pierścieniu. Każdy węzeł w Chord jest odpowiedzialny za klucze znajdujące się na nim i w jego sąsiedztwie. Pozwala to na szybkie i skalowalne wyszukiwanie kluczy w rozproszonym środowisku, co jest przydatne w sieciach peer-to-peer.

10. CAP theorem
Twierdzenie CAP mówi, że w rozproszonym systemie można jednocześnie zagwarantować tylko dwie z trzech właściwości:
Consistency (spójność): Wszystkie węzły mają tę samą wersję danych.
Availability (dostępność): Każde żądanie otrzymuje odpowiedź, nawet jeśli niektóre węzły są wyłączone.
Partition tolerance (odporność na podział sieci): System działa poprawnie, nawet jeśli wystąpią błędy komunikacji między węzłami.
Zgodnie z twierdzeniem CAP, żaden system nie może zapewnić wszystkich trzech właściwości jednocześnie w przypadku podziału sieci.