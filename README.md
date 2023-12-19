## Афиша пользовательских мероприятий

## Функционал
Бот предоставляет пользователям возможность:
1. Создавать свои мероприятия.
2. Обозначать своё участие в событиях других пользователей.
3. Вступать в чаты, посвящённые мероприятию.
4. Оставлять рецензии на событие/организатора.

## Начало работы

Стартовый промпт бота:
```
Приветствую, это Мирон -- бот для поиска людей со схожим досугом, для начала работы напиши \start
```
Ответ пользователя:
```
/start
```

Ответ бота: 
```
1 - Афиша событий
2 - Мои участия
3 - Cтать организатором / создать событие
4 - Моё портфолио
5 - Оставить отзыв 
```

# Выбор из главного меню
## 1 - Афиша событий

Промпт бота состоит из 3 популярных событий и 3 новых: 
```
Сейчас актуальны следующие события!
Популярные:
1. <Название>. <дата>.
Участников: <кол-во участников>
Организатор: <никнейм>(<рейтинг организатора>)
Код: <трёхзначное число>
...
Новые:
...
```
Популярные ранжированы по количеству участников по убыванию.
Новык ранжированны по времени, прошедшему с момента создания события, по возрастанию.

Следующее сообщение бота содержит меню ответов:

```
1. Чтобы узнать больше, введи код мероприятия!
2. Показать больше популярных событий.
3. Показать больше новых событий.
```

### 1.1 Узнать больше

Пользователь ввёл трёхзначный код.

Промпт бота:
```
<Название события>. <дата>.
<Описание, созданное организатором>
Участников: <кол-во участников>
Организатор: <никнейм>(<рейтинг организатора>)
```
Следующее сообщение бота содержит меню ответов:
```
1. Стать участником.
2. Узнать больше об организаторе.
3. Назад.
```
#### 1.1.1 Стать участником
Промпт бота:
```
Ты стал участником события "<Название события>".
Вступи в чат мероприятия, чтобы найти новых знакомых и провести время вместе!
<ссылка на тг чат события>
```
Следующее сообщение бота содержит меню ответов:
```
Введи /start, чтобы вернуться в главное меню, либо /end, чтобы завершить сессию.
```
#### 1.1.2 Узнать об организаторе
Промпт бота:
```
Организатор <никнейм>(<рейтинг организатора>).
<Статус, написанный самим организатором>
Завершённых мероприятий: <кол-во мероприятий>.
```
Следующее сообщение бота содержит меню ответов:
```
1. Посмотреть отзывы.
2. Назад.
```
##### 1.1.2.1 Посмотреть отзывы
Промпт бота состоит из 5 отзывов в следующем виде:
```
<Название>. <дата>. Участвовали: <кол-во участников>
Оценка: <оценка>.
Комментарий: <Комментарий>.
```
Пулл отзывов составляется так, чтобы присутствовали только отзывы с комментариями.

Следующее сообщение бота содержит меню ответов:
```
1.Назад.
Введи /start, чтобы вернуться в главное меню, либо /end, чтобы завершить сессию.
```

### 1.2 Показать больше популярных событий

Промпт бота состоит из 5 популярных событий: 
```
1. <Название>. <дата>.
Участвуют: <кол-во участников>
Организатор: <никнейм>(<рейтинг организатора>)
Код: <трёхзначное число>
...
```
Следующее сообщение бота содержит меню ответов:
```
1. Чтобы узнать больше, введите код мероприятия!
2. Показать больше популярных событий.
3. Показать больше новых событий.
```

### 1.3 Показать больше новых событий
Промпт бота состоит из 5 новых событий: 
```
1. <Название>. <дата>.
Участников: <кол-во участников>
Организатор: <никнейм>(<рейтинг организатора>)
Код мероприятия: <трёхзначное число>
...
```
Следующее сообщение бота содержит меню ответов:
```
1. Чтобы узнать больше, введи код мероприятия!
2. Показать больше популярных событий.
3. Показать больше новых событий.
```
## 2 Мои участия

Промпт бота:
```
Вы участвуете в следующих событиях:
1. <Название>. <дата>.
Участников: <кол-во участников>
Код мероприятия: <трёхзначное число>
Чат мероприятия: <ссылка на тг чат>
...
```
Следующее сообщение бота содержит меню ответов:
```
1. Если хочешь отказаться от участия, напиши трёхзначный код мероприятия.
2. Назад.
```

## 3 Стать организатором
Промпт бота:
```
Чтобы стать организатором, нужно зарегистрироваться в системе с помощью номера телефона. Без него регистрация не произойдёт!
А пока давай заполним информацию "о себе". Для начала выбери себе никнейм.
```
Следующее сообщение бота содержит меню ответов:
```
1. Если хочешь ввести ник, просто напиши его.
2. Назад
```
### 3.1 Ник введён
Промпт бота:
```
Отлично! Теперь опиши себя, свою деятельность и т.д.
Эта информация будет доступна всем и может как привлечь участников, так и отпугнуть, так что будь внимателен!
Придётся использовать побольше букв...
```
Следующее сообщение бота содержит меню ответов:
```
1. Если хочешь создать свой репрезент, напиши его.
2. Назад
```
#### 3.1.1 Создан репрезент
Промпт бота:
```
Мы уже на финишной прямой, неплохо было бы приложить свои соцсети, чтобы повысить к себе доверие.
Мы добавимых в описание, если ты согласен!
```
Следующее сообщение бота содержит меню ответов:
```
1. Если хочешь добавить соцсети, напиши ссылки в одном сообщении одна под другой.
2. Назад
3. Продолжить без соцсетей
```
##### 3.1.1.1/3 Соцсети готовы
Промпт бота:
```
Итак, финал, ты же ещё помнишь о необходимом условии регистрации?
Да... нужно ввести свой номер телефона.
```
Следующее сообщение бота содержит меню ответов:
```
1. Если согласен завершить регистрацию, просто напиши свой номер.
2. Назад
3. Отказаться от регистрации((
```
Ответ 3 <=> /start

##### 3.1.1.1/3.1 Регистрация завершена
Промпт бота:
```
Победа!!!
Твой статус выглядит следующим образом:
Никнейм: <никнейм>.
О себе: <описание + соцсети>
P.S. Ты всегда можешь удалить свою регистрацию в "портфолио".
```
Следующее сообщение бота содержит меню ответов:
```
Введи /start, чтобы вернуться в главное меню, либо /end, чтобы завершить сессию.
```
## *3 Создать событие*
Промпт бота:
```
Итак, для того, чтобы создать событие, нужно придумать для него короткое название,
которое пользователи будут видеть в афише, указать дату, а также придумать описание.
Не теряя времени, начнём с названия!
```
Следующее сообщение бота содержит меню ответов:
```
1. Если хочешь задать название, просто напиши его
2. Назад
```
### *3.1 Название введено*
Промпт бота:
```
Название принято, теперь дата.
```
Следующее сообщение бота содержит меню ответов:
```
1. Если хочешь задать дату, просто напиши её в виде дд.мм.гг
2. Назад
```
#### *3.1.1 Дата введена*
Промпт бота:
```
И последнее -- описание.
```
Следующее сообщение бота содержит меню ответов:
```
1. Если хочешь задать описание, просто напиши его
2. Назад
```
#### *3.1.1.1 Описание введено*
Промпт бота:
```
Супер! В афшие твоё мероприятие выглядит так:
<Название>. <дата>.
Участников: 1.
Организатор: <никнейм>(<рейтинг организатора>)
Код: <трёхзначное число>
Полная страница мероприятия выглядит так:
<Название события>. <дата>.
<Описание, созданное организатором>
Участников: 1
Организатор: <никнейм>(<рейтинг организатора>).
P.S. Ты всегда можешь удалить своё мероприятие в "портфолио".
```
Следующее сообщение бота содержит меню ответов:
```
Введи /start, чтобы вернуться в главное меню, либо /end, чтобы завершить сессию.
```
## 4 Моё портфолио
Портфолио бывает двух типов: 
1. Участник.
2. Организатор.
   
## 41 Портфолио участника
Промпт бота:
```
Приветствую в портфолио участника!
Здесь ты можешь посмотреть архив событий, в которых ты принял участие,
а также свои текущие участия.
```
Следующее сообщение бота содержит меню ответов:
```
1. Архив участий.
2. Текущие участия.
3. Назад.
```

### 41.1 Архив участий
Промпт бота:
```
Ты был участником следующих событий:
1. <Название события>. <дата>.
<Описание, созданное организатором>
Участвовали: <кол-во участников>
Организатор: <никнейм>(<рейтинг организатора>)
Код: <трёхзначное число>
...
```
Выводятся события, ранжирванные по дате: сначала новые, потом старые.
Следующее сообщение бота содержит меню ответов:
```
1. Чтобы узнать больше, введи код мероприятия!
2. Оставить отзыв о событии.
```
#### 41.1.1 Узнать больше
Промпт бота:
```
<Название события>. <дата>.
<Описание, созданное организатором>
Участвовали: <кол-во участников>
Организатор: <никнейм>(<рейтинг организатора>)
```
Следующее сообщение бота содержит меню ответов:
```
1. Узнать больше об организаторе.
2. Назад.
```
##### 41.1.1.1 Узнать больше об организаторе
аналогично 1.1.2
### 41.1.2 Оставить отзыв
Промпт бота:
```
1. Чтобы оставить отзыв о событии, напиши его трёхзначный код.
2. Назад
```
#### 41.1.2.1 Составление отзыва
аналогично 5.1

### 41.2 Текущие участия
Промпт бота:
```
Сейчас ты участвуешь в следующих событиях:
1. <Название>. <дата>.
Участников: <кол-во участников>
Организатор: <никнейм>(<рейтинг организатора>)
Код: <трёхзначное число>
Чат: <ссылка на тг чат>.
...
```
Следующее сообщение бота содержит меню ответов:
```
1. Чтобы отказаться от участия, напиши трёхзначный код события.
2. Назад.
```
#### 41.2.1 Отказ от участия
Промпт бота:
```
Ты больше не участвуешь в событии "<название>".
```
Следующее сообщение бота содержит меню ответов:
```
1. Если передумал, введи /join***, где вместо *** будет код события.
2. Назад
Введи /start, чтобы вернуться в главное меню, либо /end, чтобы завершить сессию.
```
## 42 Портфолио Организатора
Промпт бота:
```
Приветствую в порфтолио организатора!
Здесь ты можешь управлять своей деятельность и узнать всё, что о тебе думают пользователи!
Твой рейтинг: <рейтинг>.
```
Следующее сообщение бота содержит меню ответов:
```
1. Архив участий.
2. Архив организованных событий.
3. Текущие участия.
4. Текущие организованные события.
5. Удалить регистрацию.
```
### 42.1 Архив участий
Аналогично 41.1
### 42.2 Архив организованных событий
Промпт бота:
```
Ты был организатором следующих мероприятий:
1. <Название>. <дата>.
Участвовали: <кол-во участников>
Рейтинг: <рейтинг>
Код мероприятия: <трёхзначное число>
...
```
Следующее сообщение бота содержит меню ответов:
```
1. Чтобы узнать больше, введи код мероприятия!
2. Назад.
```
### 42.2.1 Узнать больше
Промпт бота:
```
<Название события>. <дата>.
<Описание, созданное организатором>
Участвовали: <кол-во участников>
Рейтинг: <рейтинг>
```
Следующее сообщение бота содержит меню ответов:
```
1. Посмотреть отзывы.
2. Назад.
```
#### 42.2.1.1 Посмотреть отзывы
Промпт бота:
```
Отзывы на событие "<название>":
1. Оценка: <оценка>
Комментарий: <Комментарий при наличии>
...
```
Следующее сообщение бота содержит меню ответов:
```
1. Назад.
Введи /start, чтобы вернуться в главное меню, либо /end, чтобы завершить сессию.
```
### 42.3 Текущие участия
Аналогично 41.2
### 42.4 Текущие организованные события
Промпт бота:
```
Сейчас ты являешься организатором следующих мероприятий:
1. <Название события>. <дата>.
Участников: <кол-во участников>
Код мероприятия: <трёхзначное число>.
...
```
Следующее сообщение бота содержит меню ответов:
```
1. Заполнить информацию о событии заново.
2. Удалить событие.
3. Назад.
```
#### 42.4.1 Заполнить заново
Промпт бота:
```
1. Чтобы заполнить информацию о событии заново, напиши его код.
2. Назад
```
##### 42.4.1.1 Начало заполнения
Аналогично 3

#### 42.4.2 Удалить событие
Промпт бота:
```
1. Чтобы удалить событие, напиши его код.
2. Назад
```
##### 42.4.2.1 Удалено
Промпт бота:
```
Событие "<название>" успешно удалено.
Введи /start, чтобы вернуться в главное меню, либо /end, чтобы завершить сессию.
```
### 42.5 Удалить регистрацию
Промпт бота:
```
Ты уверен, что хочешь удаить регистрацию?
Ты больше не сможешь создавать свои события, а твоё портфолио с никнеймом "<никнейм>" станут архивными.
```
Следующее сообщение бота содержит меню ответов:
```
1. Чтобы подтвердить удаление, введи свой никнейм.
2. Назад
```
#### 42.5.1 Удалено
Промпт бота:
```
Регистрация успешно удалена.
Введи любое сообщение, чтобы завершить сессию.
```
Любое сообщение <=> /end

## 5 Оставить отзыв
Промпт бота:
```
1. Чтобы оставить отзыв о событии, введи его трёхзначный код.
2. Назад.
```

### 5.1 Создание отзыва
Промпт бота:
```
Окей, приступим к созданию отзыва на мероприятие "<название>".
```
Следующее сообщение бота содержит меню ответов:
```
Напиши число от 1 до 10 -- твоя оценка мероприятия.
0. Назад
```
#### 5.1.1 Оценка задана
Промпт бота:
```
Оценка принята, теперь комментарий.
```
Следующее сообщение бота содержит меню ответов:
```
1. Чтобы задать комментарий, просто напиши его.
2. Пропустить.
3. Назад.
```
##### 5.1.1.1/2 Отзыв готов
Промпт бота:
```
Отзыв успешно создан!
```
Следующее сообщение бота содержит меню ответов:
```
Введи /start, чтобы вернуться в главное меню, либо /end, чтобы завершить сессию.
```
## В случае некорректных запросов
Неопознанная команда:
```
Ой, кажется, это некорекктный запрос, обрати внимание на меню ответов и try again.
Ты также всегда можешь выйти в главное меню(/start) или завершить сессию(/end).
```
Закончились мероприятия для просмотра:
```
Увы, больше мероприятий нет(
Но ты можешь организовать своё, став организатором!
1. Назад.
Введи /start, чтобы вернуться в главное меню, либо /end, чтобы завершить сессию.
```
Оставлять отзыв можно только на мероприятия, в которых пользователь участвовал. В случае попытки нарушения будет выводится следующее сообщение:
```
Оставлять отзывы можно только на мероприятия, в которых ты участвовал!
1. Назад.
```
## Примечания
Рейтинг организатора составляется как среднее арифметическое оценок его мероприятий.

В главном меню у пользователя, не имеющего статуса "организатор", пункт 3 выглядит как:

3. Стать организатором.
4. 
Иначе:

3. Создать событие.
