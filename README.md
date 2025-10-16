# Бэкенд

* Бэкенд: 
  * Основной сервис: Nest.js
  * Модуль расчётов: Express
* База данных: PostgreSQL
* Развертывание: Docker Compose

### Требования к системе

* Установленный [Docker](https://www.docker.com/products/docker-desktop/)

### Запуск

#### Локальная сборка
```
docker-compose --env-file .env.development up --build -d
```

#### Продовая сборка

```
docker compose --env-file .env.production -f docker-compose.production.yml up --build -d
```

* Перед каждым запуском приложения происходит очистка бд и затем заполнение моковыми данными

### Правила оформления Pull Requests

1. Ветка создается с названием `task-###`, где ### - номер задачи в Jira.
2. Коммиты должены быть названы по шаблону `<тип>: <описание>` согласно [соглашению о коммитах](https://www.conventionalcommits.org/ru/v1.0.0/)
3. При создании Pull Request'а нужно указать в описании ссылку на задачу в Jira.
4. Для того, чтобы залить изменения в ветку main нужно получить апрув от [Ярослава](https://t.me/Yaroslav738)