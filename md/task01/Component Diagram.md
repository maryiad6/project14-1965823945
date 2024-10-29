## Диаграмма компонентов (Component Diagram)
Диаграмма компонентов представляет собой визуальное отображение структуры системы на уровне компонентов. Она показывает, как различные компоненты системы взаимодействуют друг с другом и какие интерфейсы они используют. Компоненты могут представлять собой модули, библиотеки или другие части системы, которые могут быть независимыми и заменяемыми.

**Основные элементы диаграммы:**
- Компоненты: представляют собой основные части системы, которые выполняют определенные функции.
- Интерфейсы: определяют точки взаимодействия между компонентами, позволяя им обмениваться данными и вызывать функции друг друга.
- Связи: показывают, как компоненты связаны друг с другом и как они взаимодействуют через интерфейсы.

<details>
<summary>код puml</summary>

```
@startuml
package "Система блога" {
  [Веб-интерфейс] --> [Сервер приложений]
  [Сервер приложений] --> [База данных]
  [Сервер приложений] --> [Внешний API]
}
@enduml
```
</details>

![替代文本](../../out/lab3/project14-1965823945.wiki/puml/task01/Component%20Diagrams/Component%20Diagrams.png)
