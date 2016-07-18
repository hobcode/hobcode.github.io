# Главная страница

`index-nav` - кнопки переключения категорий автомобилей.
`index-catalog` - блок категорий автомобилей.

Для переключения используются `id` вида `c1`, `c2` и т. д. Где `c1` - первая категория, `c2` - вторая категория и т. д. То есть, не привязано к содержимому.

## Кнопка "Смотреть еще авто"
В каждый таб выводиться по 6 позиций сразу. Потом аяксом подгружается по 6 дополнительно.

При загрузке аяксом серверу передается номер таба и сдвиг для этого таба, например:
`tab=c1&offset=2`.

Значит, что в первый таб загружено 2 * 6 = 12 позиций, и выбирать из БД надо следуйющие 6, начиная с 13. Обратно от сервера скрипт ждет html-код для новых 6 блоков с автомобилями. Когда аякс вернет пустой файл (позиции кончились), то кнопка станет не активной для этого таба.