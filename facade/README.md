---
layout: pattern
title: Facade
folder: facade
permalink: /patterns/facade/
categories: Structural
tags:
 - Java
 - Gang Of Four
 - Difficulty-Beginner
---

## Назначение  / Intent /
Обеспечивает унифицированный интерфейс для множества интерфейсов в подсистеме. Фасад обеспечивает высокий уровень управления в подсистеме для облегчения ее использования. Фасад  позволяет скрыть сложность системы путём сведения всех возможных внешних вызовов к одному объекту, делегирующему их соответствующим объектам системы. / Provide a unified interface to a set of interfaces in a subsystem.
Facade defines a higher-level interface that makes the subsystem easier to use. /

![alt text](./etc/facade_1.png "Facade")

## Применение  / Applicability /
Используйте шаблон фасада когда   / Use the Facade pattern when /

* ты обеспечиваешь простой интерфейс в подсистеме. Подсистемы часто становятся все более сложными по мере их развития. Большинство шаблонов используются в большом количестве маленьких классов. Это позволяет подсистеме многократно использоваться и легче настраиваться, но для клиентов становиться труднее в использовании без настройки. /   you want to provide a simple interface to a complex subsystem. Subsystems often get more complex  as they evolve. Most patterns, when applied, result in more and smaller classes. This makes the subsystem more reusable and easier to customize, but it also becomes harder to use for clients that don't need to customize it. A facade can provide a simple default view of the subsystem that is good enough for most clients. Only clients needing more customizability will need to look beyond the facade. /
* Много зависимостей между клиентами и реализацией классов абстракции. there are many dependencies between clients and the implementation classes of an abstraction. Создайте фасад чтобы отделить подсистему от клиентов и других подсистем, способствуя тем самым независимость и портативность.  / Introduce a facade to decouple the subsystem from clients and other subsystems, thereby promoting subsystem independence and portability. /
* you want to layer your subsystems. Use a facade to define an entry point to each subsystem level. If subsystems are dependent, the you can simplify the dependencies between them by making them communicate with each other solely through their facades

## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
