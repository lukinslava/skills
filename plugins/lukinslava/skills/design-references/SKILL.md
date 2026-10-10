---
name: design-references
description: "Curated list of design references: where to look for UI, landing page, component, motion and portfolio examples before designing or building an interface. Use when the user asks for references, inspiration, examples, or 'how others do it', or when starting a new screen, landing page, component or animation without a clear visual direction."
---

# design-references

Личный список сайтов с референсами. Перед тем как придумывать интерфейс,
компонент или анимацию с нуля, посмотри сюда.

## Сайты

| Сайт | Что там | Когда смотреть |
| --- | --- | --- |
| [whatships — design](https://whatships.com/?category=design) | Подборка в категории design | Нужны свежие примеры и идеи для дизайна |
| [21st.dev](https://21st.dev/) | Каталог React-компонентов от сообщества (Tailwind, Radix, shadcn), а также шейдеры и градиенты | Нужен готовый компонент или пример, как его сделать красиво |

## Портфолио и кейсы

Для задач про портфолио, кейсы и поиск дизайнеров используй инструменты
MCP-сервера **Foliobin** (плагин `foliobin`): поиск по 1100+ реальным портфолио
с фильтрами по компаниям, странам и навыкам. Опирайся на найденные кейсы и
давай ссылки на источники. Сервер в бете: есть лимиты на запросы, может
отвечать медленно. Если инструментов Foliobin нет в сессии, скажи
пользователю, что нужно включить плагин `foliobin@lukinslava-skills`.

## Как пользоваться

1. Выбери 1–2 сайта из таблицы под задачу и открой их (WebFetch или браузер).
2. Если сайт не открывается (закрыт сетью, требует входа или рендерится только
   скриптами), не выдумывай его содержимое: дай пользователю ссылку и попроси
   скинуть скриншоты или ссылки на конкретные примеры.
3. Опиши, что именно берёшь из референса (сетка, типографика, ритм, анимация),
   а не копируй его целиком.
4. Компонент с 21st.dev ставится через shadcn CLI:
   `npx shadcn@latest add "https://21st.dev/r/<author>/<component>"`.
   Ссылку на компонент бери со страницы компонента.

## Добавить сайт

Допиши строку в таблицу выше: ссылка, что там, когда смотреть.
