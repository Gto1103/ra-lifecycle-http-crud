[![Build status](https://ci.appveyor.com/api/projects/status/vnvwffy8mwvyx9ps?svg=true)](https://ci.appveyor.com/project/Gto1103/ra-lifecycle-http-crud)

[Страница проекта](https://gto1103.github.io/ra-forms-steps/)

CRUD
===

Вам необходимо реализовать базовый CRUD без обновления при работе с HTTP.

Backend вы можете либо написать сами, либо взять готовый из каталога `backend`.



![CRUD](https://github.com/netology-code/ra16-homeworks/raw/master/lifecycle-http/crud/assets/crud.png)

## Общая механика

Первоначальная загрузка: делается http-запрос GET на адрес http://localhost:7070/notes, полученные данные отображаются в виде карточек с возможностью удаления.

Добавление:
1. Вы заполняете форму и нажимаете кнопку «Добавить».
1. Выполняется http-запрос POST на адрес http://localhost:7070/notes, в теле запроса передаётся следующий JSON:
```json
{
    "id": 0,
    "content": "То, что было введено в поле ввода"
}
```
3. После чего делается запрос на получение всех записей и происходит обновление списка — GET http://localhost:7070/notes.

Удаление:
1. Вы нажимаете на крестик на одной из карточек.
1. Выполняется http-запрос DELETE на адрес http://localhost:7070/notes/{id}, где id — это идентификатор заметки.
1. После чего делается запрос на получение всех записей и происходит обновление списка — GET http://localhost:7070/notes.

Обновление:
1. Вы нажимаете на кнопку «Обновить» — две зелёные стрелочки.
1. После чего делается запрос на получение всех записей и происходит обновление списка — GET http://localhost:7070/notes.
