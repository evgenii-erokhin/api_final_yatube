# Учебный проект: написние API для соц. сети  Yatube.

Проект создавался для отработки написания API.  Разработка осуществлялась на основании предоставленой документации API по которой следовало настроить работу API
## Как запустить проект:
+ Клонировать репозиторий и перейти в него в командной строке:
```git clone git@github.com:evgenii-erokhin/api_final_yatube.git```

   `cd api_final_yatube`

+ Cоздать и активировать виртуальное окружение:
    `python -m venv venv`

  `source venv/Scripts/activate`

+ Установить зависимости из файла requirements.txt:
`pip install -r requirements.txt`

+ Выполнить миграции:
`python manage.py migrate`
+ Запустить проект:
`python manage.py runserver`

### Автор
Evgenii Erokhin
