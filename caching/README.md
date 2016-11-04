---
layout: pattern
title: Caching
folder: caching
permalink: /patterns/caching/
categories: Other
tags:
 - Java
 - Difficulty-Intermediate
 - Performance
---

## Назначение / Intent /
Для того, чтобы не тратить время на повторное создание ресурсов после их использования. Ресурсы сохраняются в некотором быстром хранилище, и по необходимости возвращаются из хранилища / To avoid expensive re-acquisition of resources by not releasing
the resources immediately after their use. The resources retain their identity, are kept in some
fast-access storage, and are re-used to avoid having to acquire them again. /

![alt text](./etc/caching.png "Caching")

## Применение / Applicability / 
Шаблон Caching используется когда / Use the Caching pattern(s) when /

* Повторное создание, инициализация одного и того же ресурса приводит к снижению производительности / Repetitious acquisition, initialization, and release of the same resource causes unnecessary performance overhead. /

## Credits

* [Write-through, write-around, write-back: Cache explained](http://www.computerweekly.com/feature/Write-through-write-around-write-back-Cache-explained)
* [Read-Through, Write-Through, Write-Behind, and Refresh-Ahead Caching](https://docs.oracle.com/cd/E15357_01/coh.360/e15723/cache_rtwtwbra.htm#COHDG5177)
