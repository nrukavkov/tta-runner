# tta-runner

![CI](https://github.com/nrukavkov/tta-runner/workflows/CI/badge.svg)

Actions, который 27 числа каждого месяца запускается и используя docker образ (собранный из https://github.com/appulate/tta), заполняет Time Tracker.

## Пример использования

 1. Сделать [fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) проекта.
 2. Прописать обязательные [Secrets](https://docs.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets): **AD_PASSWORD , AD_USERNAME , CATEGORY ,DESCRIPTION**.

Номер нужной категории можно найти в описании репозитория [appulate/tta](https://github.com/appulate/tta)

![enter image description here](https://github.com/nrukavkov/tta-runner/raw/master/readme_example.png)
