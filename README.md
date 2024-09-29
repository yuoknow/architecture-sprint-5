[Логи rasa](./rasa-debug.log)

>А это точно лог с работой AI ассистента?
Не вижу записей старта сервера и приема сообщений от пользователя.

1. Добавил лог старта сервера

2. Сообщения от пользователя:

Строка 626 "Привет"

```
2024-09-29 20:00:30 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'приветствие', 'confidence': 0.4273204803466797} parse_data_text=Привет
```

Строка 690 "Что такое микросервисы"

```
2024-09-29 20:00:41 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'микросервисы', 'confidence': 0.14258264005184174} parse_data_text=Что такое микросервисы
```

[Скрин диалога](dialogue.png)

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
#### Запуск сервера с actions
```shell
rasa run actions
```
