# Проект API Yatube (финальная версия)
## Описание:

API позволяет осуществлять работу с базой данных социальной сети YaTube.
Пользователю доступен широкий функционал. Настроен доступ по авторизации.

## Начало работы:

Клонировать репозиторий с GitHub:

```
git clone https://github.com/dthursdays/api_final_yatube.git
```

Перейти в созданную директорию проекта:

```
cd api_final_yatube
```

Создать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить все необходимые зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

## Примеры работы с API:

### Эндпоинты, доступные без аутентификации:

- /api/v1/posts/ 
- /api/v1/posts/{post_id}/
- /api/v1/groups/
- /api/v1/groups/{group_id}/
- /api/v1/posts/{post_id}/comments/{comment_id}/

...Запросы, необходимые для получения, обновления и проверки токена...

- /api/v1/jwt/create/
```
{
"username": "string",
"password": "string"
}
```
- /api/v1/jwt/refresh/
- /api/v1/jwt/validate/


### Эндпоинты, доступные после аутентификации:
Перечень всех эндпоинтов, примеры запросов и ответов будет представлен по адресу:
http://127.0.0.1:8000/redoc/ после запуска проекта на вашей локальной машине

## Автор:

Свашенко Денис
2022 год