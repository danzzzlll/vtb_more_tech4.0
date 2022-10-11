Ссылка на бота: https://t.me/Hack4career3_bot

Ссылка на презентацию и видео: https://drive.google.com/drive/u/0/folders/111FEEGkzDmaxg-CHem8UDJbl0lT9pw0f

res_model.ipynb - предсказание на данных после парсинга
model_creating.ipynb - обучение классификатора и кластеризатора, предобработка данных

Наша команда реализовала телеграм бота, в котором есть возможность выбрать роль: бухгалтер или владелец бизнеса.
Далее выводится дайджест из 2-3 новостей и тренд.
Для выдачи и анализа новостей реализован парсер, который собирает данные с новостных сайтов rbc.ru и lenta.ru за последнюю неделю. 


Алгоритм работы состоит из нескольких частей.

Сбор данных на классификации по ролям. Для этого мы используем парсер собирающий данные с сайта BuhOnline.ru и готовые датасеты из библиотеки Natasha
Предобработка данных: удаление лишних символов, приведение к нижнему регистру, токенизация, лемматизация
Сама классификация по ролям – с помощью библиотеки для составления эмбеддингов fasttext
Далее передаем данные на алгоритм topic modeling LDA, который выделяет тренды, используя частоту встречаемости слов
Выдаем для каждой роли отдельный дайджест из 2-3 новостей по метрике cosine similarity
