# Технический репозиторий для сервиса рекомендации игр

## Клонирование проектов в репозиторий
- Запустить `clone.sh`

Либо 

- Просто выполните строчки из `clone.sh` вручную

## Запуск
После клонирования проектов выполните:
- `docker compose up --build` 

## Добавление новых моделей

1. Создайте новую модель для таблицы в `game_recommender_back/app/models`
2. Добавить модель в  `game_recommender_back/app/models/__init__.py`
3. Теперь можете генерировать миграцию alembic

## Генерация миграций

1. Подключитесь к контейнеру `back` при помощи `docker compose run back sh`
2. Выполните команду `alembic revision --autogenerate -m "your message"`

## Накат миграций на БД

1. Подключитесь к контейнеру `back` при помощи `docker compose run back sh`
2. Выполните команду `alembic upgrade head`
