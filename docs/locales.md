# Локализация

В любом запросе к API можно указывать параметр `?locale=` для передачи значения
локали (языка).

`GET /locales` возвращает список возможных значений (доступных
локалей) в поле `id`.

```json
[
    {
        "id": "RU",
        "name": "Русский"
    },
    {
        "id": "EN",
        "name": "Английский"
    }
]
```

В справочнике возможны другие значения.

Список локалей будет зависить от [указанного сайта (параметр `host`)](hosts.md).


## Локали резюме

`GET /locales/resume` возвращает справочник возможных локалей резюме.
Подколлекция справочника локалей.

Изменив локаль, можно, например, создать резюме на английском языке.

