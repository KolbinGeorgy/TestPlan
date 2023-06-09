#  Тестирование возможности записаться на обучение профессии "Тестировщик ПО"

 Описание: план автоматизации тестирования сценария перехода к форме записи на обучение профессии "Тестировщик ПО" и заполнения этой формы

<b>1. Перечень автоматизируемых сценариев.</b>

_Сценарии навигации к форме для записи на обучение профессии "Тестировщик ПО"_

1 сценарий. Зайти на начальную страницу https://netology.ru/ , нажать на меню `Каталог курсов`, слева выбрать `Программирование`, из всплывающего перечня профессий выбрать `Тестировщик ПО`, осуществится переход на страницу https://netology.ru/programs/qa.

2 сценарий. Зайти на начальную страницу https://netology.ru/ , найти подзаголовок `Направления обучения` и выбрать `Программирование`, осуществится переход на страницу https://netology.ru/development, нажать на `Тестировщик ПО` (первая в списке профессия), осуществится переход на страницу https://netology.ru/programs/qa.

_<b>Способы записи на обучение</b>_

Перейдя на страницу професии "Тестировщик ПО" https://netology.ru/programs/qa, записаться на обучение можно тремя способами:

1 способ. В начале страницы слева зеленая кнопка `Записаться`.

2 способ. Начать пролистывать вниз и сверху справа (рядом с кнопкой `Войти`) появится голубая кнопка `Записаться`.

3 способ. Пролистать всю страницу профессии вниз до формы записи.

_API тестирование_

-Позитивные проверки

Проверка поддержки MySQL Проверка поддержки Postgres Проверка корректности данных записанных в БД

_UI тестирование_

Перечень сценариев заполнения и отправки формы записи

Позитивное тестирование:

Ввести валидное имя на кириллице в поле Имя (Георгий)

Ввести валидный номер телефона из 11 цифр (79656934207)

Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об успешной отправки заявки

Негативное тестирование `1`:

1. Ввести невалидное значение (спецсимволы) в поле Имя (@#$%^&*!"№;%:?)

2. Ввести валидный номер телефона из 11 цифр (79656934207)

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Имя не может содержать спец символы

Негативное тестирование `2`:

1. Ввести пробел в поле Имя

2. Ввести валидный номер телефона из 11 цифр (79656934207)

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некорректно

Негативное тестирование `3`:

1. Ввести невалидное имя на латинице в поле Имя (Oleg)

2. Ввести валидный номер телефона из 11 цифр (79176118894)

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некорректно

Негативное тестирование `4`:

1. Ввести невалидное имя, состоящее из 1 буквы на кириллице (А)

2. Ввести валидный номер телефона из 11 цифр (79656934207)

3.Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некорректно

Негативное тестирование `5`:

1. Оставить поле Имя пустым

2. Ввести валидный номер телефона из 11 цифр (79876543210)

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Имя должно быть заполнено

Негативное тестирование `6`:

1. Ввести невалидное имя, состоящее из цифр (123456789)

2. Ввести валидный номер телефона из 11 цифр (79876543210)

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некорректно

Негативное тестирование `7`:

1. Ввести невалидное имя, состоящее из 70 букв на латинице

2. Ввести валидный номер телефона из 11 цифр (79876543210)

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Имя заполнено некорректно

Негативное тестирование `8`:

1. Ввести валидное имя на кириллице в поле Имя (Георгий)

2. Ввести невалидный номер телефона из 1 цифры (8)

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Телефон заполнено некорректно

Негативное тестирование `9`:

1. Ввести валидное имя на кириллице в поле Имя (Георгий)

2. Ввести невалидный номер телефона из 13 цифр (7999888776655)

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Телефон заполнено некорректно

Негативное тестирование `10`:

1. Ввести валидное имя на кириллице в поле Имя (Георгий)

2. Ввести буквы кириллицы в поле Телефон (фывапрол)

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Телефон заполнено некорректно

Негативное тестирование `11`:

1. Ввести валидное имя на кириллице в поле Имя (Георгий)

2. Поле Телефон оставить пустым

3. Нажать на копку Записаться

Ожидаемый результат - Появляется сообщение об ошибке, поле Телефон должно быть заполнено

<b>2. Перечень используемых инструментов с обоснованием выбора.</b>

-IDEA - интегрированная среда разработки ПО

-Gradle -  система автоматической сборки приложений

-JUnit - библиотека для модульного тестирования программ Java

-Selenide -  фреймворк для процесса автоматизированного тестирования ПО

-Docker - платформа для быстрой разработки, тестирования и развертывания приложений

-Faker - генерация случайных тестовых данных

-Git и Github - система контроля версий, сервис для совместной разработки и хостинга проектов

-AppVeyor - веб-сервис непрерывной интеграции, для сборки и тестирования ПО на GitHub 

-Jira- сервис для создания баг-репортов


<b>3. Перечень необходимых разрешений, данных и доступов.</b>

При выполнении автоматизированного тестирования сайта необходимо получить `разрешение на выполнение таких работ` у владельца сайта.
Необходим доступ к API и БД.

<b>4. Перечень и описание возможных рисков при автоматизации.</b>

Отсутсвие тестовых меток в коде страницы

<b>5. Перечень необходимых специалистов для автоматизации.</b>

Automation QA инженер

<b>6. Интервальная оценка с учётом рисков в часах.</b>

Написание автотестов, тестирование и отладка автотестов - неделя.
