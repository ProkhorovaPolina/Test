# Test
Тестовое задание QA:
Дано веб-приложение, которое имеет 4 сущности: база, категория, файл, тег.
Все 4 сущности имеют CRUD операции и древовидную структуру: у базы есть свои категории, в категориях лежат файлы, файлы могут иметь тег – некий атрибут, закрепленный за ними.

При этом имеются ограничения:
- Внутри приложения не может быть баз с одинаковым названием.
- Внутри одной базы не может быть категорий с одинаковым названием.
- Внутри одной категории не может быть файлов с одинаковым названием.
- Имя тега должно быть уникальным внутри всего приложения.

База, как и категория, могут быть пустыми, файл может не иметь тега.
При создании/изменении указываются все аттрибуты сущности, кроме id.
При удалении базы/категории удаляются вложенные в них категории и файлы.
Теги не закреплены за отдельными базами или категориями, их можно только прикрепить к одному или нескольким файлам.
При удалении файла с тегом, тег не удаляется из всего приложения и может быть применен к другим файлам.
Необходимо написать набор функциональных тестов, которые проверяют корректность работы бизнес-логики. Стоит уделить особое внимание проверкам ограничений и взаимодействию компонентов между собой.
Максимальное количество тест-кейсов: 20. 
Оформления кейса:
–	Шаги (не обязательно должны иметь глобальные шаги, не относящиеся к проверке).
–	Ожидаемый результат.
Пример:
1.	Создать файл в одной категории.
2.	Создать файл с таким же названием в другой категории этой же базы.
3.	Перенести первый файл из одной категории в другую.
Ожидаемый результат: файл не переместился.

Проверки могут быть оформлены и в виде чек-листа, например:
–	Перемещение файла из одной категории в другую, в которой имеется файл с таким же названием.