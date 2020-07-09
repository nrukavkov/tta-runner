# tta-runner

![CI](https://github.com/nrukavkov/tta-runner/workflows/CI/badge.svg)

Actions, который 25 числа каждого месяца запускается и используя docker образ (собранный из https://github.com/appulate/tta), заполняет Time Tracker.

## Базовая настройка

 1. Сделать [fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) проекта.
 2. Прописать логин и пароль пользователя tt в [Secrets](https://docs.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets): **AD_PASSWORD , AD_USERNAME**. 
 ![enter image description here](https://github.com/nrukavkov/tta-runner/raw/master/readme/example_01.png)
 3. Задаем персональные настройки категории и описания. Находим файл tta-runner/.github/workflows/CI.yml, жмем edit. Находим строки, где заданы настройки и заполняем нужными значениями. Номер нужной категории можно найти в описании репозитория [appulate/tta](https://github.com/appulate/tta/blob/master/README.rst)
 ![enter image description here](https://github.com/nrukavkov/tta-runner/raw/master/readme/example_03.png)

### Автоматический запуск

После того как вы сделали базовую настройку, ежемесячно 25 числа у вас будет заполняться tt. 

### Ручной запуск

Для проверки работы (или других целей) вы можете использовать ручной запуск. Переходим в Actions, заполняем вручную необходимые поля и жмем Run Workflow
![enter image description here](https://github.com/nrukavkov/tta-runner/raw/master/readme/example_04.png)

:warning: Обращаю ваше внимание, что приложение работает таким образом, что оно не перезаписывает данные уже внесенные в ТТ, гарантируя что ручные правки не будут удалены. 
