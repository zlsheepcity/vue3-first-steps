# Vue3 First Steps Project
November 10, 2020

Создал тестовый проект Vue 3
и записал последовательность действий.

Published Result:
https://zlsheepcity.github.io/vue3-first-steps/dist/

## Step 1. Create default project with Vue CLI

Official documentation:
https://cli.vuejs.org/guide/

```
npm install -g @vue/cli
vue create hello-world
```

При создании спрашиваются опции.
Мой выбор для простого начала:

```
» Manually

» Choose Vue version
» Router
» Vuex

» Vue 3 (Preview)

» History mode → No

» Config in package.json
```

После успешного завершения можно посмотреть как работает сайт «из коробки».

```
cd hello-world
npm run serve
```

![Screenshot](docs/screen-001.png)

Внутри можно найти две тестовые страницы Home/About (в местной терминологии это views) и тестовый компонент с описанием фреймворка.

Создание новой страницы и нового компонента — хорошее начало для самостоятельной работы.


## Step 2. Make Build

```
npm run build
```

Команда сгенерирует сайт в папку dist. После первой попытки я создал дополнительный конфигурационный файл, чтобы сгенерированный сайт можно было смотреть локально в браузере и публиковать на гитхабе.

https://github.com/zlsheepcity/vue3-first-steps/blob/main/vue.config.js
