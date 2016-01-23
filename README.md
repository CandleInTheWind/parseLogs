Дарова. 

Тут короче типа ТЗ. 

Во-первых цель. 
Цель - получить практические навыки, и это всё что пока имеет значения. 
Соотвественно исходя из этого я предлагаю выбрать задачу, которая с одной стороны 
не такая уж оторванная от жизни, с другой стороны легко масштабируется. 

Итак, что я хочу написать. 

Хочу программу, которая умеет красиво работать с логами. В идеале - ты ей даешь логи, а потом с ними что-то делаешь. 

Формат логов наверное не имеет значение, поэтому давай возьмем стандартный логер с его форматом. Ну например log4j (http://www.mkyong.com/logging/log4j-hello-world-example/). 

%d{yyyy-MM-dd HH:mm:ss} %-5p %c{1}:%L - %m%n

%d{yyyy-MM-dd HH:mm:ss} = Date and time format, refer to SimpleDateFormat JavaDoc.
%-5p = The logging priority, like DEBUG or ERROR. The -5 is optional, for the pretty print format.
%c{1} = The logging name we set via getLogger(), refer to log4j PatternLayout guide.
%L = The line number from where the logging request.
%m%n = The message to log and line break.

2014-07-02 20:52:39 DEBUG className:200 - This is debug message

2014-07-02 20:52:39 DEBUG className:201 - This is debug message2


В качестве поэтапной работы, я предлагаю делать следующее. 

1)  На первом этапе мы пишем что-то простое и консольное. 
  a) Приложение должно иметь консольный интерфейс.
  b) Возможность выбора файла с логами.
  c) Различные фильтры для поиска в логах  (по времени, по уровню, по вхождению слов и т.п.). 
      (Этот пункт логично развивать на протяжении всей работы, поэтому в него упираться сразу наверное не стоит).

2) Добавляем к работе с файлами - работу с БД. 

Учимся сохранять логи в бд, и работать (фильтры и т.п.) с логами через бд.  Например говорим "Хочу сохранить все логи типа Error в базу" и т..п

3) Добавляем UI (тут возможны варианты, кому какой UI интересен, но мне интересно лично web). Делаем простой UI который умеет фильтровать.

4) Если всё это у нас получится - предлагаю посмотреть в сторону интеграции с технологаями.
Есть всевозможные elasticsearch, kafka и т.п. с помощью которых можно решать нашу задачу "красиво". Можно поиграться с ними. Я думаю тут будет всякая тесная связь с java-кодом и т.п. 

5) Наверное заняться чем-нить другим :)

