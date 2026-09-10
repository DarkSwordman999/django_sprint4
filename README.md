<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20&height=180&section=header&text=Blogicum&fontSize=70&fontAlignY=35&desc=Django%20Blog%20Platform%20%7C%20Yandex%20Practicum&descAlignY=55&descSize=18" alt="Blogicum Banner" width="100%">

<img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/Django-3.2.16-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django">
<img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite">
<img src="https://img.shields.io/badge/Bootstrap-5.0.1-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap">

<br>

<img src="https://img.shields.io/badge/Pytest-7.1.3-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" alt="Pytest">
<img src="https://img.shields.io/badge/pytest--django-4.5.2-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" alt="pytest-django">
<img src="https://img.shields.io/badge/Flake8-5.0.4-yellow?style=for-the-badge&logo=python&logoColor=white" alt="Flake8">
<img src="https://img.shields.io/badge/Yandex-Practicum-red?style=for-the-badge&logo=yandex&logoColor=white" alt="Yandex Practicum">

<br><br>

<h2>📝 Blogicum — блог-платформа на Django</h2>

<p>
  <b>Учебный проект в рамках курса «Python-разработчик» от Яндекс Практикума</b>
</p>

</div>

---

## 📖 О проекте

**Blogicum** — веб-платформа для ведения блогов. Пользователи могут публиковать записи, привязывать их к категориям и локациям, просматривать публикации других авторов, регистрироваться, входить в систему и управлять своим паролем.

В рамках **четвёртого спринта** проект получил полноценную систему аутентификации на базе `django.contrib.auth`, а также расширенное покрытие автоматическими тестами.

На этом этапе реализованы:

* 🔐 регистрация и авторизация пользователей;
* 🔑 смена и восстановление пароля;
* 💬 работа с комментариями;
* ✏️ редактирование контента;
* 📧 отправка писем для восстановления пароля;
* ⚠️ обработка страниц ошибок;
* 🧪 расширенный набор тестов.

---

## ✨ Основные возможности

### 📝 Публикации

* Просмотр ленты записей.
* Просмотр отдельных публикаций.
* Фильтрация записей по категориям.
* Работа с категориями и локациями.
* Управление публикациями через интерфейс.

### 🔐 Аутентификация

Для авторизации используется стандартная система Django `django.contrib.auth`.

Реализованы:

* регистрация пользователей;
* вход и выход из системы;
* смена пароля;
* восстановление пароля через email;
* перенаправление пользователя обратно на закрытую страницу после авторизации.

Формы аутентификации оформлены с помощью `django-bootstrap5` и Bootstrap-карточек.

---

## 🔑 Страницы аутентификации

Все шаблоны авторизации находятся в:

```text
templates/registration/
```

| Шаблон                         | Назначение                               |
| :----------------------------- | :--------------------------------------- |
| `login.html`                   | Вход в систему и ссылка «Забыли пароль?» |
| `logged_out.html`              | Подтверждение успешного выхода           |
| `registration_form.html`       | Регистрация нового пользователя          |
| `password_change_form.html`    | Смена пароля                             |
| `password_change_done.html`    | Подтверждение смены пароля               |
| `password_reset_form.html`     | Запрос на восстановление пароля          |
| `password_reset_done.html`     | Подтверждение отправки письма            |
| `password_reset_confirm.html`  | Установка нового пароля                  |
| `password_reset_complete.html` | Завершение восстановления пароля         |

### 🔄 Параметр `next`

В `login.html` предусмотрена обработка параметра `next`.

Если неавторизованный пользователь пытается открыть закрытую страницу:

```text
Закрытая страница
       ↓
   Авторизация
       ↓
Успешный вход
       ↓
Возврат на исходную страницу
```

---

## 🧪 Расширенное тестирование

В четвёртом спринте значительно расширено тестовое покрытие проекта.

Проверяются:

* пользователи и аутентификация;
* посты;
* комментарии;
* категории и локации;
* редактирование;
* отправка писем;
* страницы ошибок;
* статические страницы;
* формы;
* контент приложения.

---

## 🚧 В разработке

Следующие возможности планируется развивать дальше:

* 👤 Полноценные профили пользователей с возможностью редактирования.
* 🖼️ Загрузка изображений к публикациям.
* ✏️ Расширенное управление постами через интерфейс.

---

## 🛠️ Технологический стек

| Технология            | Версия | Назначение                   |
| :-------------------- | :----: | :--------------------------- |
| **Python**            |  3.10+ | Основной язык разработки     |
| **Django**            | 3.2.16 | Веб-фреймворк                |
| **django-bootstrap5** |  22.2  | Рендеринг форм в Bootstrap 5 |
| **Pillow**            |  9.3.0 | Работа с изображениями       |
| **SQLite**            |    —   | База данных                  |
| **Bootstrap**         |  5.0.1 | Стилизация интерфейса        |
| **Pytest**            |  7.1.3 | Автоматическое тестирование  |
| **pytest-django**     |  4.5.2 | Интеграция Pytest с Django   |
| **mixer**             |  7.2.2 | Генерация тестовых данных    |
| **Faker**             | 12.0.1 | Создание тестовых данных     |
| **beautifulsoup4**    | 4.11.2 | Проверка и парсинг HTML      |
| **Flake8**            |  5.0.4 | Линтинг Python-кода          |

---

## 📂 Структура проекта

```text
django_sprint4/
├── templates/
│   ├── blog/                    # Шаблоны приложения blog
│   ├── includes/                # Общие шаблонные включения
│   ├── pages/                   # Статические страницы
│   │
│   ├── registration/            # Аутентификация
│   │   ├── login.html
│   │   ├── logged_out.html
│   │   ├── registration_form.html
│   │   ├── password_change_form.html
│   │   ├── password_change_done.html
│   │   ├── password_reset_form.html
│   │   ├── password_reset_done.html
│   │   ├── password_reset_confirm.html
│   │   └── password_reset_complete.html
│   │
│   └── base.html                # Базовый шаблон
│
├── tests/
│   ├── adapters/                # Адаптеры для тестов
│   ├── fixtures/                # Фикстуры
│   ├── form/                    # Тесты форм
│   ├── conftest.py              # Общие настройки pytest
│   ├── test_comment.py          # Тесты комментариев
│   ├── test_content.py          # Тесты постов, категорий и локаций
│   ├── test_edit.py             # Тесты редактирования
│   ├── test_emails.py           # Тесты отправки писем
│   ├── test_err_pages.py        # Тесты страниц ошибок
│   ├── test_post.py             # Тесты публикаций
│   ├── test_static_pages.py     # Тесты статических страниц
│   └── test_users.py            # Тесты пользователей
│
├── .gitignore                   # Исключения Git
├── LICENSE                      # Лицензия проекта
├── README.md                    # Документация
├── db.json                      # Дамп данных
├── pytest.ini                   # Конфигурация pytest
├── requirements.txt             # Зависимости проекта
├── setup.cfg                    # Конфигурация Flake8
└── manage.py                    # Управляющий скрипт Django
```

---

## 🚀 Запуск проекта

### 📋 Требования

Перед началом работы убедитесь, что установлены:

* **Python 3.10+**
* **pip**
* **Git**

<details>
<summary><b>1. Клонирование репозитория</b></summary>

```bash
git clone https://github.com/DarkSwordman999/django_sprint4.git
cd django_sprint4
```

</details>

<details>
<summary><b>2. Создание виртуального окружения</b></summary>

```bash
python -m venv venv
```

**Windows:**

```bash
venv\Scripts\activate
```

**macOS / Linux:**

```bash
source venv/bin/activate
```

</details>

<details>
<summary><b>3. Установка зависимостей</b></summary>

```bash
pip install -r requirements.txt
```

</details>

<details>
<summary><b>4. Применение миграций</b></summary>

```bash
python manage.py migrate
```

</details>

<details>
<summary><b>5. Загрузка данных</b></summary>

```bash
python manage.py loaddata db.json
```

</details>

<details>
<summary><b>6. Запуск сервера</b></summary>

```bash
python manage.py runserver
```

После запуска проект доступен по адресу:

```text
http://127.0.0.1:8000/
```

Административная панель:

```text
http://127.0.0.1:8000/admin/
```

</details>

### 📧 Восстановление пароля

Для тестирования восстановления пароля используется **консольный email-бэкенд Django**.

Письмо не отправляется на реальный email — его содержимое выводится непосредственно в терминал, где запущен:

```bash
python manage.py runserver
```

---

## 🧪 Тестирование

Для запуска тестов используется связка **Pytest + pytest-django**.

Конфигурация находится в:

```text
pytest.ini
```

Запуск полного набора тестов:

```bash
pytest
```

### 🔍 Что проверяется

| Тест                   | Назначение                             |
| :--------------------- | :------------------------------------- |
| `test_comment.py`      | Работа комментариев                    |
| `test_content.py`      | Посты, категории и локации             |
| `test_edit.py`         | Редактирование постов и профиля        |
| `test_emails.py`       | Восстановление пароля и отправка писем |
| `test_err_pages.py`    | Страницы ошибок 404 и 500              |
| `test_post.py`         | Работа с публикациями                  |
| `test_static_pages.py` | Статические страницы                   |
| `test_users.py`        | Пользователи и аутентификация          |
| `form/`                | Тестирование форм                      |

Для подготовки тестовых данных используются:

* `mixer`;
* `Faker`.

Для проверки HTML применяется:

* `beautifulsoup4`.

Общие фикстуры и адаптеры находятся в:

```text
tests/conftest.py
tests/fixtures/
tests/adapters/
```

---

## 🧹 Линтинг

Для проверки качества и соответствия кода стандартам используется **Flake8**.

В проекте также используются плагины:

* `flake8-docstrings`;
* `pep8-naming`.

Конфигурация находится в:

```text
setup.cfg
```

Запуск проверки:

```bash
flake8 .
```

---

## 📄 Лицензия

Проект распространяется в соответствии с лицензией, указанной в файле [`LICENSE`](./LICENSE).

---

## 👤 Автор

<div align="center">

### DarkSwordman999

<a href="https://github.com/DarkSwordman999">
  <img src="https://img.shields.io/badge/GitHub-DarkSwordman999-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
</a>

</div>

---

<div align="center">

### ⭐ Понравился проект?

Если **Blogicum** оказался полезным или интересным,
**поставьте ⭐ репозиторию на GitHub** — это лучшая поддержка проекта!

<a href="https://github.com/DarkSwordman999/django_sprint4">
  <img src="https://img.shields.io/github/stars/DarkSwordman999/django_sprint4?style=for-the-badge&logo=github&label=Star%20repository" alt="Star repository">
</a>

<br><br>

<i>Спасибо за интерес к проекту! 🚀</i>

</div>

---

<div align="center">

### 🎓 Yandex Practicum

**Проект создан в рамках курса «Python-разработчик» от Яндекс Практикума.**

<i>Учебный проект. Создан в образовательных целях.</i>

</div>
