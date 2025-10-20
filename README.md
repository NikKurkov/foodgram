# 🍽️ Foodgram — Продуктовый помощник

Онлайн-сервис, где пользователи публикуют рецепты, подписываются на авторов, добавляют любимые блюда в избранное и формируют удобные списки покупок.  
Проект создан в рамках диплома курса **«Backend-разработка»** от Яндекс.Практикума.

---

## 🌐 Онлайн-демо
🔗 **[foodgram.kurkov.biz](https://foodgram.kurkov.biz/)**

## 🎬 Видео-демо
<p align="center">
  <a href="https://vimeo.com/1128971020" target="_blank">
    <img src="assets/demo.gif" alt="Смотреть демо на Vimeo" width="640">
  </a>
</p>

---

## ⚙️ Технологический стек

- 🐍 **Python 3.12**
- 🌿 **Django 4.x** + **Django REST Framework**
- 🐘 **PostgreSQL**
- 🐳 **Docker & Docker Compose**
- 🧩 **Gunicorn** + **Nginx**
- ⚙️ **GitHub Actions (CI/CD)**
- 📦 **DockerHub** для автоматического деплоя

---

## 🚀 Особенности реализации

- Проект полностью контейнеризован в **Docker**;
- Образы `foodgram_frontend` и `foodgram_backend` опубликованы на DockerHub;
- Автодеплой на сервер с помощью **GitHub Actions**;
- После успешного деплоя отправляется уведомление в **Telegram**;
- Поддерживается документация API через **Redoc**.

---

## 🧭 Развертывание проекта локально

1. Установите на сервере `docker` и `docker-compose`.
2. Создайте файл `.env` по шаблону из `.env.example`.
3. Соберите и запустите контейнеры:
   ```bash
   docker compose up -d --build
   ```
4. Выполните миграции:
   ```bash
   docker compose exec backend python manage.py migrate
   ```
5. Создайте суперпользователя:
   ```bash
   docker compose exec backend python manage.py createsuperuser
   ```
6. Соберите статику:
   ```bash
   docker compose exec backend python manage.py collectstatic --no-input
   ```
7. Заполните базу ингредиентами:
   ```bash
   docker compose exec backend python manage.py load_ingredients
   ```
8. Для корректного создания рецептов через фронт добавьте теги в админке.
9. Документация API:  
   👉 [http://localhost/api/docs/redoc.html](http://localhost/api/docs/redoc.html)

---

## 👨‍💻 Автор

**Николай Курков**  
📫 Telegram: [@nikkur](https://t.me/nikkur)  
📘 GitHub: [NikKurkov](https://github.com/NikKurkov)

---

## 🏆 Лицензия

Этот проект создан в образовательных целях и распространяется под лицензией MIT.
