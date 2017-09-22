<a name="accept-kids"></a>
# Вакансия доступна для соискателей от 14 лет

Публикация вакансий для соискателей от 14 лет допустима только на территории Российской Федерации. 
Права публиковать вакансии с пометкой для соискателей от 14 лет есть у подтвержденных Российских работодателей. Для получения права для иностранной компании обратитесь к персональному менеджеру.

После получения права, появится возможность публиковать новые вакансии с данным параметром, либо обновлять имеющиеся вакансии.

## Публикация вакансии

Для пубилкации вакансии, доступной для соискателей от 14 лет, необходимо в тело запроса `POST /vacancies` добавить параметр
```json
{
    "accept_kids": "true"
}
```
[Основная статья про публикацию вакансии](employer_vacancies.md#creation)

## Обновление вакансии

Для обновления вакансии, выполните запрос

`PUT /vacancies/{vacancy_id}` 

Тело запроса:
```json
{
    "accept_kids": "true"
}
```
[Основная статья про редактирование вакансии](employer_vacancies.md#edit)

<a name="edit-results"></a>
## Ошибка и код ответа

В случае, если у пользователя недостаточно прав на редактирование поля accept_kids, либо вакансия публикуется за пределами РФ, то дополнительно к HTTP коду `403 Forbidden` сервер вернет описание причины ошибки: 
```json
{
    "errors": [
        {
            "type": "vacancies",
            "value": "can_not_accept_kids"
        }
    ]
}
```

## Дополнительная информация

[https://hh.ru/article/20732](https://hh.ru/article/20732)