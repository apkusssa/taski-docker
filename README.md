<h1 style="text-align:center;">Taski</h1> 
Taski Docker - это проект, представляющий собой систему управления задачами с использованием Docker-контейнеров.
С помощью Taski Docker вы можете легко создавать и управлять различными задачи.

<h2 style="text-align:center;">Инструкция по запуску:</h2>

- Клонировать репозиторий с github на сервер `git clone git@github.com:apkusssa/taski-docker.git`
- Установить Curl `sudo apt update && sudo apt install curl`
- Скачать установщик Docker'а `curl -fSL https://get.docker.com -o get-docker.sh`
- Установить Docker `sudo sh ./get-docker.sh`
- Установить Docker compose `sudo apt install docker-compose-plugin`
- Создать файл .env с переменными
- Запустить сценарий установки проекта `sudo docker compose -f docker-compose.production.yml up -d`
- Выполнить миграции `sudo docker compose -f docker-compose.production.yml exec backend python manage.py migrate`
- Собрать статику контейнера backend `sudo docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic`
- Скопировать статику из контейнера в вольюм `sudo docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /backend_static/static/`


<h2 style="text-align:center;">Используемые технологии:</h2>
<ul>
    <li> Ubuntu 22.04 <a href="https://help.ubuntu.com/"> Documentation</a> </li>
    <li>Python 3.10.12 <a href="https://docs.python.org/3/index.html"> Documentation</a> </li>
    <li>Django 3.2.3 <a href="https://docs.djangoproject.com/en/4.2/"> Documentation</a></li>
    <li>Django Rest Framework 3.12.4 <a href="https://www.django-rest-framework.org/topics/documenting-your-api/"> Documentation</a></li>
    <li>Gunicorn 20.1.0 <a href="https://docs.gunicorn.org/en/stable/"> Documentation</a></li>
    <li>React JS 18.2.0 <a href="https://legacy.reactjs.org/docs/getting-started.html?url=https%3A%2F%2Freactjs.org%2Fdocs%2Fgetting-started.html"> Documentation</a></li>
    <li>Nginx 1.18.0 (Ubuntu) <a href="https://nginx.org/ru/docs/"> Documentation</a></li>
    <li>Docker 24.0.7 <a href="https://docs.docker.com/"> Documentation</a></li>
    <li>Docker compose 2.21.0 <a href="https://docs.docker.com/compose/"> Documentation</a></li>
    
</ul>
<h3>Автор: Афанасий Павлов</h3>
