---
layout: pattern
title: Adapter
folder: adapter
permalink: /patterns/adapter/
categories: Structural
tags:
 - Java
 - Gang Of Four
 - Difficulty-Beginner
---

## Also known as
Wrapper

## Цель / Intent /
Преобразует интерфейс класса в другой ожидаемый интерфейс клиента. Адаптер позволяет классам работать вместе с несовместимыми интерфейсами / Convert the interface of a class into another interface the clients
expect. Adapter lets classes work together that couldn't otherwise because of
incompatible interfaces. / 

![alt text](./etc/adapter.png "Adapter")

Класс Adapter (Captain) приводит интерфейс класса Adaptee (BattleFishingBoat) в соответствие с интерфейсом класса Target (BattleShip) (наследником которого является Adapter). Это позволяет объекту Client использовать объект Adaptee (посредством адаптера Adapter) так, словно он является экземпляром класса Target. Таким образом Client обращается к интерфейсу Target, реализованному в наследнике Adapter, который перенаправляет обращение к Adaptee.

Пример реализации [через наследование](https://ru.wikipedia.org/wiki/%D0%90%D0%B4%D0%B0%D0%BF%D1%82%D0%B5%D1%80_(%D1%88%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD_%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F)#Java) и [через композицию](https://ru.wikipedia.org/wiki/%D0%90%D0%B4%D0%B0%D0%BF%D1%82%D0%B5%D1%80_(%D1%88%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD_%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F)#Java_2)

## Применение / Applicability /
Используйте шаблон адаптера когда: / Use the Adapter pattern when /

* Ты хочешь использовать существующий класс и его интерфейс не соответсвует нужному тебе интерфейсу / you want to use an existing class, and its interface does not match the one you need /
* Ты создаешь класс для повторного использования, который взаимодействует с несвязанными классами, т.е. с классами которые не имеют совместимых интерфейсов / you want to create a reusable class that cooperates with unrelated or unforeseen classes, that is, classes that don't necessarily have compatible interfaces /
* Тебе необходимо использовать несколько существующих подклассво, но не практично создвать свой интерфейс для каждого подкласса. Адаптере может адаптировать интерфейс для родительского класса. / you need to use several existing subclasses, but it's impractical to adapt their interface by subclassing every one. An object adapter can adapt the interface of its parent class. /

## Real world examples

* [java.util.Arrays#asList()](http://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html#asList%28T...%29)

## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
* [J2EE Design Patterns](http://www.amazon.com/J2EE-Design-Patterns-William-Crawford/dp/0596004273/ref=sr_1_2)
