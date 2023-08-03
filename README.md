![CI/CD Status](https://github.com/VlKazmin/kittygram_final/actions/workflows/main.yml/badge.svg)
#  [Kittygram](http://cattime.ddns.net/)

## Описание проекта
Социальная сеть любителей котиков.
Позволяет пользователям публиковать фотографии своих котов и делиться впечатлениями об их достижениях
## Инструкция по разворачиванию

Приложение запускается из контейнеров
 * скачайте файл **`docker-compose.production.yml`** в папку проекта.
 * в этой же папке  создайте файл **`.env`**  и добавьте необходимые переменные (пример в описании)

## Описание переменных окружения
Ниже пример файла **`.env`** c переменными окружения, необходимыми для запуска приложения
```
# POSTGRES_SQL
POSTGRES_USER=django_user
POSTGRES_PASSWORD=mysecretpassword
POSTGRES_DB=django
DB_HOST=db
DB_PORT=5432

# DJANGO
SECRET_KEY = 'your_secret_key'
DEBUG = False
ALLOWED_HOSTS = ['server_ip', 'domain_name']
```
для запуска проекта выполните
```
sudo docker compose -f docker-compose.production.yml up --build
```
Локально приложение будет доступно по адресу
[http://127.0.0.1:9000](http://127.0.0.1:9000)
