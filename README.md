# workshop_2026_marketplace

Маркетплейс скілів і плагінів для Claude Code.

## Підключення

```
/plugin marketplace add wiksval/workshop_2026_marketplace
/plugin install tone-of-voice@workshop_2026_marketplace
```

## Плагіни

| Плагін | Що робить |
|---|---|
| [tone-of-voice](plugins/tone-of-voice) | Переписує будь-який текст у tone of voice продукту: дружньо, коротко, без канцеляризмів. |

### tone-of-voice

Скіл `tone-of-voice` приймає текст і повертає його переписаним у стилі продукту. Факти, цифри, плейсхолдери та форматування він не змінює.

Приклад:

> **Було:** Шановний користувачу! У зв'язку з технічними роботами на даний момент надання послуг тимчасово неможливе.
>
> **Стало:** Ми трохи оновлюємо сервіс, тож він ненадовго недоступний. Скоро повернемось!

## Структура

```
.claude-plugin/marketplace.json   # каталог маркетплейсу
plugins/
  tone-of-voice/
    .claude-plugin/plugin.json
    skills/tone-of-voice/SKILL.md
```

## Додати новий плагін

1. Створіть папку `plugins/<назва>` з `.claude-plugin/plugin.json` та `skills/`.
2. Додайте запис у `plugins` у `.claude-plugin/marketplace.json`.
3. Перевірте: `claude plugin validate .`
