# Учебный проект: написние API для соц. сети  Yatube.

Проект создавался для отработки написания API.  Разработка осуществлялась на основании предоставленой документации API по которой следовало настроить работу API
## Технологии:
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![DjangoREST](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray)
## Как запустить проект:
+ Клонировать репозиторий и перейти в него в командной строке:

  `git clone git@github.com:evgenii-erokhin/api_for_yatube.git`

   `cd api_for_yatube`

+ Cоздать и активировать виртуальное окружение:

  `python -m venv venv`

  `source venv/Scripts/activate`

+ Установить зависимости из файла requirements.txt:

  `pip install -r requirements.txt`

+ Выполнить миграции:

  `python manage.py migrate`

+ Запустить проект:

  `python manage.py runserver`
### Примеры запросов для аутентифицированных пользователей:
1. `POST` запрос на эндпоинт - http://127.0.0.1:8000/api/v1/posts/

   Тело запроса:
   ```
   {
    "text": "Текст поста.",
    "group": 1
   } 
   ```
    Ответ эндпоинта:
    ```
    {
    "id": 1,
    "text": "Текст поста 1.",
    "author": "superuser",
    "image": null,
    "group": 1,
    "pub_date": "2023-08-09T08:47:11.084589Z"
   } 
    ```
3. `GET` запрос на эндпоинт - http://127.0.0.1:8000/api/v1/groups/3/

   Ответ эндпоинта:
   ```
   {
    "id": 3,
    "title": "Название группы 3",
    "slug": "slug-группы 3",
    "description": "Описание группы 3"
   } 
   ```
### Примеры запросов для неаутентифицированных пользователей:
1. `GET` запрос на эндпоинт - http://127.0.0.1:8000/api/v1/posts/
   
   ```
   [
   {
        "id": 1,
        "author": "superuser",
        "image": null,
        "text": "Текст поста 1.",
        "pub_date": "2023-08-09T08:47:11.084589Z",
        "group": 1
   },
   {
        "id": 2,
        "author": "test_user",
        "image": "http://127.0.0.1:8000/media/posts/photo_2023-08-08_12.14.10.jpeg",
        "text": "Текст поста 2.",
        "pub_date": "2023-08-09T12:10:21.084589Z",
        "group": null
    }
    ]
2. `GET` запрос на эндпоинт  http://127.0.0.1:8000/api/v1/groups/

    ```
    {
        "id": 1,
        "title": "Название группы 1",
        "slug": "slug-группы 1",
        "description": "Описание группы 1"
   },
   {
        "id": 2,
        "title": "Название группы 2",
        "slug": "slug-группы 2 ",
        "description": "Описание группы 2"
   } 
    ```
### Контакты:
<a href="https://t.me/juandart" target="_blank">
<img src=https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white />
</a>
<a href="mailto:evgeniierokhin@proton.me?">
<img src=https://img.shields.io/badge/ProtonMail-8B89CC?style=for-the-badge&logo=protonmail&logoColor=white />
</a>
