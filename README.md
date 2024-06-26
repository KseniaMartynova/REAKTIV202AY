# Reactive Programming Patterns
## Содержание
- [Observer](#Observer_pattern)
- [Пример из жизни для Observer](#Пример_из_жизни_для_Observer)
- [Преимущества Observer](#Преимущества_Observer)
- [Недостатки Observer](#Недостатки_Observer)
- [Chain of responsibility](#Chain_of_responsibility_pattern)
- [Пример из жизни для Chain_of_responsibility](#Пример_из_жизни_для_Chain_of_responsibility)
- [Преимущества Chain_of_responsibility](#ПреимуществаChain_of_responsibility)
- [Недостатки Chain_of_responsibility](#Недостатки_Chain_of_responsibility)
- [ФанФакты](#ФанФакты_о_Chain_of_responsibility)
- [Команда](#команда)
## Observer_pattern
Паттерн наблюдатель (Observer) - это поведенческий паттерн проектирования, который создаёт механизм подписки, позволяющий одним объектам следить и реагировать на события, происходящие в других объектах.

![image](https://github.com/KseniaMartynova/REAKTIV202AY/assets/113133074/2ac48a20-2f99-4c3c-8a1e-863773b6629f)

Он остоит из двух основных компонентов: наблюдаемого (Subject) и наблюдателя (Observer). Наблюдаемый объект содержит список наблюдателей и методы для добавления, удаления и уведомления наблюдателей. Наблюдатели, в свою очередь, содержат метод, который вызывается при обновлении наблюдаемого объекта.

Паттерн позволяет реализовать слабую связанность между объектами, облегчает расширение системы. Его использование особенно полезно в ситуациях, когда один объект должен уведомлять много других объектов об изменениях.

### Пример из жизни для Observer
Мы согласились на уведомления по почте от "Золотого Яблока" о скидках и акциях на наш любимый бренд косметики. И нам больше не нужно ежедневно ездить в магазин и проверять есть скидка на крем или нет. Вместо этого "Золотое Яблоко" пришлет нам письмо со всеми акциями и скидками прямо на наш смартфон. Магазин ведет список подписчиков и знает, кому отправлять письма. Но в любой момент мы можем отписаться от рассылки.

### Преимущества Observer
+Издатели не зависят от конкретных классов подписчиков и наоборот.

+Вы можете подписывать и отписывать получателей на лету.

### Недостатки Observer
-Подписчики оповещаются в случайном порядке.

## Chain_of_responsibility_pattern
Паттерн "Цепочка обязанностей" (Chain of Responsibility) - это поведенческий паттерн проектирования, который позволяет передавать запросы последовательно по цепочке объектов, пока один из них не обработает запрос или запрос не достигнет конца цепочки.

![image](https://github.com/KseniaMartynova/REAKTIV202AY/assets/113133074/ab6e7d68-98ff-4ed4-9124-11b144d8e39c)

Здесь участвуют несколько объектов, называемых обработчиками (handlers), которые образуют цепочку. Когда поступает запрос, он передается по цепочке от одного обработчика к другому.

Каждый обработчик в цепочке имеет ссылку на следующий обработчик в цепи. Это позволяет объектам в цепочке не иметь информации о других объектах в цепи и обеспечивает гибкость в добавлении новых обработчиков или изменении порядка их вызова.

### Пример из жизни для Chain_of_responsibility
Мы купили видеокарту, но она не работает. Звоним в поддержку в надежде, что они подскажут, что делать. Звоним и слышим голос автоответчика, который предлагает выбор из пяти стандартных решений. Все, что он предлагает нам не подходит и мы просим связать нас с оператором. Но наш оператор достаточно глуп и у него и так много работы помимо нашей видеокарты, поэтому мы просим связать нас с человеком действительно разбирающимся. Им оказывается дежурный инжинер, который решает нашу проблему с помощью скачивания каких то драйверов. Мы удовлетворены, мы кладем трубку.

### Преимущества Chain_of_responsibility
+Уменьшение зависимости между отправителем запроса и обработчиками, что обеспечивает гибкость и упрощает добавление новых функций

+Реализует принцип единственной обязанности и принцип открытости/закрытости.

### Недостатки Chain_of_responsibility
-Запрос может остаться никем не обработанным.

### ФанФакты о Chain_of_responsibility
-Цепочку обязанностей часто используют вместе с Компоновщиком. В этом случае запрос передаётся от дочерних компонентов к их родителям.

-Цепочка обязанностей и Декоратор имеют очень похожие структуры. Оба паттерна базируются на принципе рекурсивного выполнения операции через серию связанных объектов.
## Команда
Акентьева Анна, Кашлинова Мария, Мартынова Ксения, Шаропина Ирина
