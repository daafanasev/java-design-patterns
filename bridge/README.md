---
layout: pattern
title: Bridge
folder: bridge
permalink: /patterns/bridge/
categories: Structural
tags:
 - Java
 - Gang Of Four
 - Difficulty-Intermediate
---

## Also known as
Handle/Body

## Цель / Intent /
Отделить абстракцию от реализации, т.к. оба могут изменяться независимо / Decouple an abstraction from its implementation so that the two can vary independently./

![alt text](./etc/bridge.png "Bridge")

## Применение / Applicability /
Используйте шаблон Bridge когда: /Use the Bridge pattern when /

* Ты избегаешь постоянного связывания между абстракцией и реализацией. Это может быть случай, когда например, реализация должна выбираться или переключаться в реальном времени. / you want to avoid a permanent binding between an abstraction and its implementation. This might be the case, for example, when the implementation must be selected or switched at run-time. /
* оба, абстракция и реализация должны расширяться на подклассы. В этом случае, шаблон Bridge дает тебе комбиниовтаь различные абстракции и реализации и расширять их независимо друг от друга. / both the abstractions and their implementations should be extensible by subclassing. In this case, the Bridge pattern lets you combine the different abstractions and implementations and extend them independently /
* изменения в реализации не должны влиять на клиентов / changes in the implementation of an abstraction should have no impact on clients; that is, their code should not have to be recompiled. /
* ты имеешь профилированные классы. Такая иерархия классов указывает на необходимость разбиения объекта на две части. Рамбо использует термин «вложенные обобщения» в иерархии таких классов /  you have a proliferation of classes. Such a class hierarchy indicates the need for splitting an object into two parts. Rumbaugh uses the term "nested generalizations" to refer to such class hierarchies /
* Вы хотите разделить реализацию между несколькими объектами (возможно, с помощью подсчета ссылок), и этот факт должен быть скрыт от клиента. Простой пример класса String, Coplien, в которых на несколько объектов могут совместно использовать одну строку представления. / you want to share an implementation among multiple objects (perhaps using reference counting), and this fact should be hidden from the client. A simple example is Coplien's String class, in which multiple objects can share the same string representation. /

## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
