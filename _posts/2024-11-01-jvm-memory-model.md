---
layout: post
title: Model pamięci JVM
thumbnail-img: /assets/img/2024-11-01.jpg
tags: [jvm]
---

- stack - created at the same time as the thread. A Java Virtual Machine stack is analogous to the stack of a conventional language such as C: it holds local variables and partial results, and plays a part in method invocation and return.
- heap - shared among all Java Virtual Machine threads. The heap is the run-time data area from which memory for all class instances and arrays is allocated
- method area - shared among all Java Virtual Machine threads. The method area is analogous to the storage area for compiled code of a conventional language or analogous to the "text" segment in an operating system process
- run-time constant pool - per-class or per-interface run-time representation of the constant_pool table in a class file. It contains several kinds of constants, ranging from numeric literals known at compile-time to method and field references that must be resolved at run-time. The run-time constant pool serves a function similar to that of a symbol table for a conventional programming language, although it contains a wider range of data than a typical symbol table.
- native methods stacks - (methods written in a language other than the Java programming language). Native method stacks may also be used by the implementation of an interpreter for the Java Virtual Machine's instruction set in a language such as C

Przy okazji warto wspomnieć o tym czym jest proces i wątek. Proces jest zbiorem wątków dla których istnieje współdzielona pamięć. Jeżeli mamy parę procesów to one między sobą nie dzielą się pamięcią. Proces to 'worek' na wątki. Wątki i procesy w linuxie leżą bardzo blisko siebie. Gdy startuje JVM, to JVM prosi system o wątki systemowe. Java tylko zleca stworzenia wątku. Więc wątki JVM to są wątki systemowe. Wątki JVM są w taki sam sposób zarządzane jak wątki systemowe.