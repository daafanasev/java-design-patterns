---
layout: pattern
title: Chain of responsibility
folder: chain
permalink: /patterns/chain/
categories: Behavioral
tags:
 - Java
 - Gang Of Four
 - Difficulty-Intermediate
---

## Назначение / Intent /
Избегает связи отправителя запроса с приемником, предоставляя Chain, больше чем одному объекту, обработать запрос. Chain получает объекты и передает запрос далее до объекта обработки.   / Avoid coupling the sender of a request to its receiver by giving
more than one object a chance to handle the request. Chain the receiving
objects and pass the request along the chain until an object handles it. /

![alt text](./etc/chain_1.png "Chain of Responsibility")

## Применение  / Applicability /
Шаблон Chain используется когда:  / Use Chain of Responsibility when /

* больше чем один объект может обработать запрос и неизвестен приоритет. Обработчик назначается автоматически.  / more than one object may handle a request, and the handler isn't known a priori. The handler should be ascertained automatically /
* вы хотите передать запрос одному из нескольких объектов без указания получателя явно.   / you want to issue a request to one of several objects without specifying the receiver explicitly /
* множество объектов, которые могут обработать запрос, должны быть определены динамически the set of objects that can handle a request should be specified dynamically

## Real world examples

* [java.util.logging.Logger#log()](http://docs.oracle.com/javase/8/docs/api/java/util/logging/Logger.html#log%28java.util.logging.Level,%20java.lang.String%29)
* [Apache Commons Chain](https://commons.apache.org/proper/commons-chain/index.html)

## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
