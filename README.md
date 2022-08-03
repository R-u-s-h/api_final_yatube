# Проект cоциальная сеть YaTube + API

### Описание
В социальной сети YaTube реализован следующие функции:
- Создание постов
- Группы
- Комментирование постов
- Подписка на посты автора

### Технологии
- Python 3.8.10
- Django 2.2.16
- Django REST Framework 3.12.4
- JWT + Joser

### Запуск проекта dev-режиме
- Клонируйте проект
```
git clone git@github.com:R-u-s-h/api_final_yatube.git
```
- Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt
``` 
- В папке с файлом manage.py выполните команду:
```
python3 manage.py runserver
```

### Примеры API запросов
- Получение всех постов с пагинацией и лимитом вывода постов
```
GET http://127.0.0.1:8000/api/v1/posts/?limit=2&offset=1
```
- Создание поста с авторизаций по токену автора
```
POST http://127.0.0.1:8000/api/v1/posts/
content-type: application/json
Authorization: Bearer {{access_token}}

{
    "text": "Публикация номер 01",
    "image": null,
    "group": 0
}
```
### Полную документацию к API проекту Yatube вы найдете по ссылке http://127.0.0.1:8000/redoc/