[Логи rasa](./rasa-debug.log)

### Запуск веб-приложения
```shell
npm install
npm run build
npm run start
```

### Запуск rasa
#### Установить rasa
```shell
pip3.9 install rasa
```

#### Запуск экшенов
```shell
cd rasa
```
```shell
rasa run actions
```

#### Запуск модели и api
```shell
rasa run --enable-api --cors "*"
```

