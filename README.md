# FinalProject

## Обязательное задание (обязательно к выполнению):
С использованием Selenium Webdriver, применяя паттерн проектирования Page Object
и сохраняя веб-локаторы в отдельном yaml-файле выполнить следующие тесты в
браузере Google Chrome для линукс:
- логин на сайт https://test-stand.gb.ru
- клик по ссылке About
- проверка, что шрифт в заголовке открывшегося окна имеет размер 32 px

## Дополнительное задание 1:
Выполнить быструю проверку сайта на уязвимости при помощи утилиты командной
строки nikto;

## Дополнительное задание 2:
С использованием библиотеки requests выполнить авторизацию на сайте с
использованием токена авторизации в headers, получить данные о текущем
пользователе и проверить, что они соответствуют данным, возвращенным в ответе на
запрос авторизации;

## Блоки с подсказками:

### Обязательное задание
Браузер Google Chrome не входит в стандартную поставку Ubuntu, его нужно
установить командами:
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i --force-depends google-chrome-stable_current_amd64.deb
Или вручную скачать файл по указанной выше ссылке и установить пакет.

### Дополнительное задание 1
Перед написанием тестов нужно вручную установить утилиту nikto командой sudo apt install nikto.
Нужно проверить что в выводе команды
nikto -h https://test-stand.gb.ru/ -ssl -Tuning 4
присутствует текст
0 error(s)

### Дополнительное задание 2
Нужно проверить, что запрос к https://test-stand.gb.ru/api/users/profile/{id} возвращает
json с правильным username