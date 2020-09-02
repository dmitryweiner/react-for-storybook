# Учебный репозиторий для освоения Storybook + Loki

## Запуск дев-сервера
```
npm run dev
```


## Установка Storybook
```
npx -p @storybook/cli sb init --type react_scripts
```

## Как писать сторис
https://storybook.js.org/docs/react/writing-stories/introduction

## Установка Loki
```
npm i -D loki
npx loki init
```

### Конфиг
```
"loki": {
  "configurations": {
    "chrome.laptop": {
      "target": "chrome.app",
      "width": 1366,
      "height": 768,
      "deviceScaleFactor": 1,
      "mobile": false
    },
    "chrome.iphone7": {
      "target": "chrome.app",
      "preset": "iPhone 7"
    }
  }
}
```

### Добавить скрипты в scripts:
```
"loki:test": "npm run build-storybook && npx loki test --reactUri file:./storybook-static",
"loki:update": "npm run build-storybook && npx loki update --reactUri file:./storybook-static",
"loki:approve": "npx loki approve"
```

## Задание:
1. Написать сторис для имеющихся компонентов
2. Написать стори для нового компонента, потом написать сам компонент
3. Запустить локи, изменить компонент, запустить loki:test.
