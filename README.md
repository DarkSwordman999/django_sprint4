<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20&height=180&section=header&text=Blogicum&fontSize=70&fontAlignY=35&desc=Django%20Blog%20Platform%20%7C%20Yandex%20Practicum&descAlignY=55&descSize=18" alt="Banner" width="100%">

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

<h2>🐍 Blogicum — блог-платформа на Django</h2>

<p><b>Учебный проект в рамках курса «Python-разработчик» от Яндекс Практикума</b></p>

</div>

<hr>

<h2>📖 О проекте</h2>

<p><b>Blogicum</b> — площадка для ведения блогов. Пользователи могут публиковать посты, привязывать их к категориям и локациям, просматривать записи других авторов, регистрироваться, входить в систему и управлять своим паролем.</p>

<p>В четвёртом спринте к работающему блогу добавлена <b>полноценная система аутентификации</b> на базе <code>django.contrib.auth</code>, а также расширено покрытие тестами: комментарии, редактирование, отправка писем, страницы ошибок.</p>

<hr>

<h2>✅ Что уже сделано</h2>

<ul>
  <li>Django-проект с приложениями <code>blog</code> и <code>pages</code>.</li>
  <li>Модели <code>Category</code>, <code>Location</code>, <code>Post</code>.</li>
  <li>Базовый шаблон <code>base.html</code> с наследованием.</li>
  <li>Инклюды: шапка, подвал, карточка поста, ссылка на категорию.</li>
  <li>Страницы: лента записей, пост, категория, «О проекте», «Наши правила».</li>
  <li>Маршрутизация с namespace (<code>blog:</code>, <code>pages:</code>).</li>
  <li>Дамп данных <code>db.json</code> для загрузки в БД.</li>
  <li>Настроены линтеры и тесты.</li>
</ul>

<hr>

<h2>🔐 Аутентификация</h2>

<p>Реализована на стандартных вьюхах Django. Все формы рендерятся через <code>django-bootstrap5</code> и обёрнуты в карточки Bootstrap. Шаблоны находятся в <code>templates/registration/</code>:</p>

<div align="center">

<table>
  <thead>
    <tr>
      <th align="left">Шаблон</th>
      <th align="left">Назначение</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><code>login.html</code></td><td>Вход в систему + ссылка «Забыли пароль?»</td></tr>
    <tr><td><code>logged_out.html</code></td><td>Успешный выход</td></tr>
    <tr><td><code>registration_form.html</code></td><td>Регистрация нового пользователя</td></tr>
    <tr><td><code>password_change_form.html</code></td><td>Форма смены пароля</td></tr>
    <tr><td><code>password_change_done.html</code></td><td>Пароль успешно изменён</td></tr>
    <tr><td><code>password_reset_form.html</code></td><td>Запрос на сброс пароля по email</td></tr>
    <tr><td><code>password_reset_done.html</code></td><td>Письмо со ссылкой отправлено</td></tr>
    <tr><td><code>password_reset_confirm.html</code></td><td>Ввод нового пароля по ссылке</td></tr>
    <tr><td><code>password_reset_complete.html</code></td><td>Сброс пароля завершён</td></tr>
  </tbody>
</table>

</div>

<p>В <code>login.html</code> предусмотрена обработка параметра <code>next</code>: если неавторизованный пользователь пытается зайти на закрытую страницу, его перенаправляет на форму входа, а после успешного входа — обратно.</p>

<hr>

<h2>🚧 Что в разработке</h2>

<ul>
  <li>Профили пользователей с возможностью редактирования.</li>
  <li>Загрузка изображений к постам.</li>
  <li>Возможность создавать и редактировать посты через интерфейс.</li>
</ul>

<hr>

<h2>🛠️ Технологии</h2>

<div align="center">

<table>
  <thead>
    <tr>
      <th align="left">Технология</th>
      <th align="left">Версия</th>
      <th align="left">Назначение</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><b>Python</b></td><td>3.10+</td><td>Язык разработки</td></tr>
    <tr><td><b>Django</b></td><td>3.2.16</td><td>Веб-фреймворк</td></tr>
    <tr><td><b>django-bootstrap5</b></td><td>22.2</td><td>Рендеринг форм в Bootstrap 5</td></tr>
    <tr><td><b>Pillow</b></td><td>9.3.0</td><td>Работа с изображениями</td></tr>
    <tr><td><b>SQLite</b></td><td>—</td><td>База данных</td></tr>
    <tr><td><b>Bootstrap</b></td><td>5.0.1</td><td>CSS-фреймворк</td></tr>
    <tr><td><b>Pytest</b></td><td>7.1.3</td><td>Тестирование</td></tr>
    <tr><td><b>pytest-django</b></td><td>4.5.2</td><td>Интеграция pytest с Django</td></tr>
    <tr><td><b>mixer</b></td><td>7.2.2</td><td>Генерация тестовых данных</td></tr>
    <tr><td><b>Faker</b></td><td>12.0.1</td><td>Фейковые данные для тестов</td></tr>
    <tr><td><b>beautifulsoup4</b></td><td>4.11.2</td><td>Парсинг HTML в тестах</td></tr>
    <tr><td><b>Flake8</b></td><td>5.0.4</td><td>Линтинг кода</td></tr>
  </tbody>
</table>

</div>

<hr>

<h2>📂 Структура проекта</h2>

<pre><code>django_sprint4/
├── templates/
│   ├── blog/                    # Шаблоны приложения blog
│   ├── includes/                # Общие инклюды (header, footer, post_card)
│   ├── pages/                   # Статические страницы
│   ├── registration/            # Шаблоны аутентификации
│   │   ├── login.html
│   │   ├── logged_out.html
│   │   ├── registration_form.html
│   │   ├── password_change_form.html
│   │   ├── password_change_done.html
│   │   ├── password_reset_form.html
│   │   ├── password_reset_done.html
│   │   ├── password_reset_confirm.html
│   │   └── password_reset_complete.html
│   └── base.html                # Базовый шаблон
├── tests/
│   ├── adapters/                # Адаптеры для тестов
│   ├── fixtures/                # Фикстуры
│   ├── form/                    # Тесты форм
│   ├── conftest.py              # Общие настройки pytest
│   ├── test_comment.py          # Тесты комментариев
│   ├── test_content.py          # Тесты контента (посты, категории, локации)
│   ├── test_edit.py             # Тесты редактирования
│   ├── test_emails.py           # Тесты отправки писем
│   ├── test_err_pages.py        # Тесты страниц ошибок
│   ├── test_post.py             # Тесты постов
│   ├── test_static_pages.py     # Тесты статических страниц
│   └── test_users.py            # Тесты пользователей
├── .gitignore                   # Исключения Git
├── LICENSE                      # Лицензия проекта
├── README.md                    # Документация
├── db.json                      # Дамп данных для загрузки в БД
├── pytest.ini                   # Конфигурация pytest
├── requirements.txt             # Зависимости проекта
├── setup.cfg                    # Конфигурация flake8
└── manage.py                    # Управляющий скрипт Django</code></pre>

<hr>

<h2>🚀 Запуск</h2>

<h3>Требования</h3>
<ul>
  <li><b>Python</b> 3.10 или выше.</li>
  <li><b>pip</b> для установки зависимостей.</li>
</ul>

<h3>Шаги</h3>
<ol>
  <li>
    <b>Клонируйте репозиторий:</b>
    <pre><code>git clone https://github.com/DarkSwordman999/django_sprint4.git
cd django_sprint4</code></pre>
  </li>
  <li>
    <b>Создайте и активируйте виртуальное окружение:</b>
    <pre><code>python -m venv venv

# Windows:
venv\Scripts\activate

# macOS / Linux:
source venv/bin/activate</code></pre>
  </li>
  <li>
    <b>Установите зависимости:</b>
    <pre><code>pip install -r requirements.txt</code></pre>
  </li>
  <li>
    <b>Примените миграции:</b>
    <pre><code>python manage.py migrate</code></pre>
  </li>
  <li>
    <b>Загрузите данные из дампа:</b>
    <pre><code>python manage.py loaddata db.json</code></pre>
  </li>
  <li>
    <b>Запустите сервер разработки:</b>
    <pre><code>python manage.py runserver</code></pre>
  </li>
</ol>

<p>После запуска проект доступен по адресу <code>http://127.0.0.1:8000/</code>, админ-панель — <code>http://127.0.0.1:8000/admin/</code>.</p>

<p>Для тестирования сброса пароля по email в настройках используется консольный бэкенд: письмо выводится прямо в терминал, где запущен <code>runserver</code>.</p>

<hr>

<h2>🧪 Тестирование</h2>

<p>Тесты запускаются через <b>pytest</b> с плагином <b>pytest-django</b>. Конфигурация — в <code>pytest.ini</code>.</p>

<pre><code>pytest</code></pre>

<p>Что проверяется:</p>
<ul>
  <li><b><code>test_comment.py</code></b> — комментарии к постам.</li>
  <li><b><code>test_content.py</code></b> — контент: посты, категории, локации.</li>
  <li><b><code>test_edit.py</code></b> — редактирование постов и профиля.</li>
  <li><b><code>test_emails.py</code></b> — отправка писем (сброс пароля).</li>
  <li><b><code>test_err_pages.py</code></b> — страницы ошибок (404, 500).</li>
  <li><b><code>test_post.py</code></b> — посты.</li>
  <li><b><code>test_static_pages.py</code></b> — статические страницы.</li>
  <li><b><code>test_users.py</code></b> — пользователи и аутентификация.</li>
  <li><b><code>form/</code></b> — тесты форм.</li>
</ul>

<p>Для генерации тестовых данных используются <b>mixer</b> и <b>Faker</b>, для проверки HTML — <b>beautifulsoup4</b>. Общие фикстуры и адаптеры — в <code>conftest.py</code>, <code>fixtures/</code> и <code>adapters/</code>.</p>

<hr>

<h2>🧹 Линтинг</h2>

<p>Код проверяется линтером <b>flake8</b> с плагинами <code>flake8-docstrings</code> и <code>pep8-naming</code>. Настройки — в файле <code>setup.cfg</code>.</p>

<pre><code>flake8 .</code></pre>

<hr>

<h2>📄 Лицензия</h2>

<p>Проект распространяется под лицензией, указанной в файле <a href="./LICENSE">LICENSE</a>.</p>

<hr>

<h2>👤 Автор</h2>

<div align="center">

<p><b>DarkSwordman999</b></p>

<a href="https://github.com/DarkSwordman999">
  <img src="https://img.shields.io/badge/GitHub-DarkSwordman999-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
</a>

</div>

<hr>

<div align="center">

<h3>🎓 Проект создан в рамках курса «Python-разработчик» от <a href="https://practicum.yandex.ru/">Яндекс Практикума</a></h3>

<p><i>Учебный проект. Создан в образовательных целях.</i></p>

</div>
