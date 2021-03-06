# BATTLE NEXUS stream setup guide

## Гайд
### Основной инструмент (OBS)
Мы пользуемся OBS. Поэтому в гайде фигурировать будет именно он. Если есть иные предпочтения, тот же `streamlabs` умеет делать то же самое.
1. Устанавливаем OBS [с официального сайта](https://obsproject.com/ru/download).
2. Открываем OBS. В верхней панели нажимаем `Файл -> Настройки`. В настройках выбираем `Трансляция`.
3. Сервис указываем `YouTube - RTMPS`. Ниже нажимаем кнопку `Использовать ключ потока`. Ключ потока в появившийся текстбоксе вставляем. Получить его можно на Youtube, будучи залогиненным под аккаунтом battle nexus. Как найти? Нажимаем справа сверху на ютубе "Создать" (кнопочка изображена ниже), начать трансляцию. В появившемся окне будет ключ трансляции в виде скрытых символов (точечки, как у паролей)\
![](assets/readme/create_button.png)
4. Переходим во вкладку `Вывод` в OBS. У меня стоят такие настройки:\
![Output settings](assets/readme/output_settings.png)
5. Можно еще поковыряться в настройках, если интересно. Но мы идем делать сцены. Закрыли настройки, и в главном окне OBS есть такое окошко (как ниже). Там плюсик нажимаем и делаем так, чтобы у нас было две сцены.\
![Output settings](assets/readme/scenes.png)
6. Настроим главную сцену. Сначала сделаем донаты. Для этого кликаем на сцену в списке сцен и кликаем в окошке справа ("источники") ПКМ. Выбираем браузер. Жмем ок. В появившемся окне вставляем в поле адрес URL вот эту ссылку `https://www.donationalerts.com/widget/alerts?group_id=1&token=q8rPK2BtssdWVAL5srJf`. Теперь добавим игру. Для этого ее надо запустить. Потом, как и в случае с донатами, добавляем источник "захват игры". Меня уже заебало писать это как для особо одаренных поэтому тут сами разберетесь. Далее расскажу про плашки.
7. Из этого репозитория надо скачать программу `Score Board Edit 1.4`. Запускаем ее. Приложение позволяет выбрать либо `Filer path`, либо `Folder path`. Выбираем второе. В выбранную далее директорию он высрет несколько файлов. Нас интересуют четыре: два никнейма (`P1.txt`, `P2.txt`) и два счетчика (`scrP1.txt`, `scrP2.txt`) для левого и правого игроков соответственно. После выбора директории тыкаем `Select/Read files`. Меняем необходимую информацию и нажимаем `Update`. Если игроки меняются местами, нажимаем `Switch`.
8. Теперь нам нужно сделать так, чтобы это как-то отображалось. Добавляем источник-текст. Обзываем его, жмем ок. В настройках после выбора шрифта (про это позже) ставим галочку `Чтение из файла`. Указываем один из четырех файлов, которые ывсрало приложение в прошлом пункте. Далее копируем настройки ниже. Потом поправим по верстке.\
![](assets/readme/text_settings.png)
9. Да, про шрифты. Мы везде используем `Roboto Condensed`. Мы делаем это, потому что NRS используют этот шрифт, и он прекрасно подходит к шрифту МК. Не надо изобретать велосипед. Просто используй то, что работает. И если у тебя зачешутся руки поменять его, просто вспомни, что там сидят нормальные дизайнеры, которые умеют подбирать шрифты, а мы в среднем за час стрима получаем 10 рублей донатов. Если этого шрифта у тебя нет - я положил его в папочку `fonts`. Просто открываешь его и видишь кнопку в новом окошке вроде "установить шрифт".
10. В папочке `fonts` лежит шрифт `MKX Title`. Мы используем его для, внимание... Заголовков! Рекомендую использовать только капс, потому что строчные буквы у него странные, да и зачем они тебе в заголовках :) .
11. В папке `Score Board Edit 1.4` лежат также баннеры для счета. Левый и правый. Давай, ты сам разберешься, как в источники добавить картинки. Далее про верстку.
12. Баннеры надо сделать красиво. У нас есть возможность расположить их по образцу. Для этого [идем сюда](https://www.figma.com/file/MnWWydNWfUcn2V4ZgslKc0/Untitled?node-id=103%3A9). Тыкаем слева сверху фрейм `ScoresLayout`. Справа сверху выбираем `Export`, чуть ниже центра тыкаем `Export ScoresLayout`. У тебя есть картинка. Добавь ее временно в OBS и по ней откалибруй это все дело.
13. Если какие-то ресурсы выглядят как пожатые или растянутые, то жмем на этом источнике ПКМ. Выбираем фильтры. Добавляем фильтр (слева снизу в новом окне плюсик). Находим `Масштабирование\соотношение сторон`. Выбираем `бикубический`.
14. Рекомендую все, что связано со счетом, объединить в одну группу. Просто в источниках создаем источник типа группа и скидываем все в нее (перетаскиваем). Там Можно будет напротив нее нажать глазик, и все исчезнет.
15. Переходим к другой сцене. Нам нужен глаынй экран. Для этого [идем сюда](https://www.figma.com/file/MnWWydNWfUcn2V4ZgslKc0/Untitled?node-id=2%3A3). Берем фрейм `StreamWaiting` (как в пункте 12 берем).
16. Добавляем таймер. Это приложение, которое лежит в этом репозитории: `StreamTimer3.1`. Работает оно просто: вводим в него время, нажимаем старт. И он будет в файлик `Timer.txt` рядом с собой логать время. Нужно только расположить его вот так:\
![](assets/readme/timer_layout.png)
17. На эту сцену тоже добавляем донаты.
18. На эту сцену добавляем захват игры, но меньше :). У меня это вот так выглядело:\
![](assets/readme/waiting_screen.png)
19. Текст справа, понятно дело, зависит от контента стрима. `VS` красненькие, потому что в фигме я отдельно их подкрашивал. То есть текст этот конкретно не в OBS сделан. Прямо сейчас париться с доступом я не успею, поэтому если тоже так хочешь, скопируй как-нибудь проект из фигмы и сам там подпиши. Иначе просто черех OBS текст делать.