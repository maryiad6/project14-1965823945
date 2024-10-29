## Диаграммы классов (Class Diagrams)
Диаграммы классов представляют собой статическое отображение структуры системы, показывая классы, их атрибуты и методы, а также отношения между классами. Они помогают разработчикам понять, как различные компоненты системы взаимодействуют друг с другом.

**Основные элементы диаграммы:**
- Классы: представляют собой сущности системы с определенными атрибутами и методами.
- Атрибуты: характеристики классов, которые хранят данные.
- Методы: функции, которые определяют поведение классов.
- Связи: показывают отношения между классами, такие как ассоциации, агрегации и композиции.

<details>
<summary>код puml</summary>

```
@startuml
class Пользователь {
  +String имя
  +String email
  +войти()
  +выйти()
}

class Пост {
  +String заголовок
  +String содержание
  +Date датаСоздания
  +добавитьКомментарий()
}

class Комментарий {
  +String текст
  +Date датаПубликации
}

Пользователь "1" -- "0..*" Пост : создает >
Пост "1" -- "0..*" Комментарий : содержит >
@enduml
```
</details>

![替代文本](../../out/lab3/project14-1965823945.wiki/puml/task01/Class%20Diagram/Class%20Diagram.png)
<details>
<summary>код puml</summary>

```
@startuml
class Озеро {
  +String название
  +double площадь
  +double глубина
  +получитьДетали()
}

class Река {
  +String название
  +double длина
  +String источник
  +String устье
  +получитьДетали()
}

Озеро "1" -- "0..*" Река : питается >
@enduml
```
</details>

![替代文本](../../out/lab3/project14-1965823945.wiki/puml/task01/Class%20Diagram/Class%20Diagram-1.png)
<details>
<summary>код puml</summary>

```
@startuml
class ПрофильПользователя {
  +String имяПользователя
  +String пароль
  +String биография
  +обновитьПрофиль()
}

class ПрофильАдминистратора {
  +String имяАдминистратора
  +String emailАдминистратора
  +управлятьПользователями()
}

ПрофильПользователя <|-- ПрофильАдминистратора
@enduml
```
</details>

![替代文本](../../out/lab3/project14-1965823945.wiki/puml/task01/Class%20Diagram/Class%20Diagram-2.png)
<details>
<summary>код puml</summary>

```
@startuml
class Тег {
  +String название
  +добавитьТег()
}

class Пост {
  +String заголовок
  +String содержание
  +добавитьТег()
}

Пост "0..*" -- "0..*" Тег : помечен >
@enduml
```
</details>

![替代文本](../../out/lab3/project14-1965823945.wiki/puml/task01/Class%20Diagram/Class%20Diagram-3.png)
<details>
<summary>код puml</summary>

```
@startuml
class Уведомление {
  +String сообщение
  +Date дата
  +отправитьУведомление()
}

class Пользователь {
  +String имя
  +String email
  +получитьУведомление()
}

Пользователь "1" -- "0..*" Уведомление : получает >
@enduml
```
</details>

![替代文本](../../out/lab3/project14-1965823945.wiki/puml/task01/Class%20Diagram/Class%20Diagram-4.png)