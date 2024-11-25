---
layout: post
title: Fallacies of distributed computing
thumbnail-img: /assets/img/2024-10-24.jpg
tags: [spring]
---

- The network is reliable - dlatego ustawiaj timeout bo nie usługi nie działają zawsze np. connection timeout (200 ms), socket/read timeout czyli jak długo czekamy na dane
- Latency is zero - warto utrzymywać pule połączeń żeby minimalizować koszt nawiązywania połączenia za każdym razem i sterować wartościami dotyczącymi szczegółów klientów HTTP takimi jak liczba połączeń równoległych dla host + port i maksymalna liczba utrzymywanych połączeń przez klienta HTTP
- Bandwidth is infinite;
- The network is secure;
- Topology doesn't change;
- There is one administrator;
- Transport cost is zero;
- The network is homogeneous;