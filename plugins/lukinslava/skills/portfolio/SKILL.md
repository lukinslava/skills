---
name: portfolio
description: "Designer portfolio and case study work: structure a portfolio, write or improve a case study, design the first screen of a portfolio site, find how designers at strong companies present their work, or find designers for a role. Use whenever the user mentions портфолио, кейс, case study, portfolio site, or hiring designers. Uses the Foliobin MCP (1,100+ real designer portfolios) instead of guessing from the web."
---

# portfolio

Работай от реальных портфолио, а не от общих шаблонов. Источник — MCP-сервер
**Foliobin** (плагин `foliobin`): 1100+ портфолио дизайнеров, фильтры по
компаниям, странам и навыкам.

## 1. Загрузи инструменты Foliobin

Инструменты отложенные. Найди их через ToolSearch по запросу `foliobin`.
Полные имена начинаются с `mcp__plugin_foliobin_foliobin__`.

Если инструментов нет, скажи пользователю, что нужно включить плагин
`foliobin@lukinslava-skills`, а в облаке ещё и разрешить домен `foliobin.com`.
Не подменяй данные Foliobin выдуманными примерами.

## 2. Выбери инструмент под задачу

| Задача | Инструмент |
| --- | --- |
| Структура портфолио: какие разделы, в каком порядке | `portfolio_outline` |
| Написать или улучшить кейс | `case_study_kit`, затем `case_study_examples` |
| Как делают кейсы дизайнеры конкретных компаний | `case_study_examples`, `search_portfolios` |
| Первый экран сайта-портфолио | `first_screens` |
| Найти портфолио по компании, стране, навыку | `search_portfolios`, потом `get_portfolio` |
| Найти похожие по картинке или скриншоту | `search_by_image` |
| Найти дизайнеров под роль или вакансию | `find_designers_for_role` |
| Что вообще есть в каталоге | `catalog_stats` |

Параметры смотри в схеме инструмента после загрузки.

## 3. Как работать

1. Уточни контекст, если его нет: роль и уровень, на какие компании или
   рынок целится человек, какие проекты есть.
2. Возьми 3–5 подходящих примеров из Foliobin, а не один.
3. Объясни, что именно берёшь из примеров: структуру, подачу проблемы,
   метрики, визуальный ритм. Не копируй чужие тексты.
4. Всегда давай ссылки на портфолио и кейсы, на которые опираешься.
5. Сервер в бете: есть лимиты на запросы, он может отвечать медленно.
   Не делай десятки вызовов подряд; если упёрся в лимит, скажи об этом.

## Вместе с другими скиллами

- Тексты на русском — `sasha`.
- Вёрстка сайта-портфолио — `design-taste-frontend` и `design-references`.
- Видео для кейса — `video`.
