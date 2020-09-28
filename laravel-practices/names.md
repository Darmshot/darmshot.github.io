---
layout: page
title: Соглашения об именовании
---

Эта статья - попытка собрать в одном месте все существующие на данный момент соглашения об именовании, гласно или негласно принятые сообществом Laravel. Я решил собрать всю информацию в виде удобной таблицы, актуальную версию которой вы всегда сможете найти [здесь](https://github.com/alexeymezenin/laravel-best-practices/blob/master/russian.md#%D0%A1%D0%BE%D0%B1%D0%BB%D1%8E%D0%B4%D0%B0%D0%B9%D1%82%D0%B5-%D1%81%D0%BE%D0%B3%D0%BB%D0%B0%D1%88%D0%B5%D0%BD%D0%B8%D1%8F-%D1%81%D0%BE%D0%BE%D0%B1%D1%89%D0%B5%D1%81%D1%82%D0%B2%D0%B0).


Что | Правило | Принято | Не принято
------------ | ------------- | ------------- | -------------
Контроллер | ед. ч. | ArticleController | ArticlesController
Маршруты | мн. ч. | articles/1 | article/1
Имена маршрутов | snake_case | users.show_active | users.show-active, show-active-users
Модель | ед. ч. | User | Users
Отношения hasOne и belongsTo | ед. ч. | articleComment | articleComments, article_comment
Все остальные отношения | мн. ч. | articleComments | articleComment, article_comments
Таблица | мн. ч. | article_comments | article_comment, articleComments
Pivot таблица | имена моделей в алфавитном порядке в ед. ч. | article_user | user_article, articles_users
Столбец в таблице | snake_case без имени модели | meta_title | MetaTitle; article_meta_title
Внешний ключ | имя модели ед. ч. и _id | article_id | ArticleId, id_article, articles_id
Первичный ключ | - | id | custom_id
Миграция | - | 2017_01_01_000000_create_articles_table | 2017_01_01_000000_articles
Метод | camelCase | getAll | get_all
Метод в контроллере ресурсов | [таблица](https://laravel.com/docs/master/controllers#resource-controllers) | store | saveArticle
Метод в тесте | camelCase | testGuestCannotSeeArticle | test_guest_cannot_see_article
Переменные | camelCase | $articlesWithAuthor | $articles_with_author
Коллекция | описательное, мн. ч. | $activeUsers = User::active()->get() | $active, $data
Объект | описательное, ед. ч. | $activeUser = User::active()->first() | $users, $obj
Индексы в конфиге и языковых файлах | snake_case | articles_enabled | ArticlesEnabled; articles-enabled
Представление | snake_case | show_filtered.blade.php | showFiltered.blade.php, show-filtered.blade.php
Конфигурационный файл | snake_case | google_calendar.php | googleCalendar.php, google-calendar.php
Контракт (интерфейс) | прилагательное или существительное | Authenticatable | AuthenticationInterface, IAuthentication
Трейт | прилагательное | Notifiable | NotificationTrait

Если у вас есть дополнения к таблице, пишите их в комментариях или в [подфоруме о хороших практиках](https://laravel.ru/forum/viewforum.php?id=17).

Хотите увидеть больше статей на тему хороших практик? Поддержите проект поставив звезду в [репозитории хороших практик Laravel](https://github.com/alexeymezenin/laravel-best-practices/blob/master/russian.md). Это показывает есть ли интерес к этой теме, а также здорово мотивирует автора на написание других полезных материалов.
