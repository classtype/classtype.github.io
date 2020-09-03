# Быстрый старт

Для начала у вас уже должны быть установлены [node.js](https://nodejs.org/) и [npm](https://www.npmjs.com/)

Далее нам нужно установить пакет [app.init](https://www.npmjs.com/package/app.init)

```
npm install --save app.init
```


## Инициализация нового приложения

Для быстрого старта нам нужно создать два файла
`index.js` и `events.js`

Исходный код находится 
[здесь](https://github.com/classtype/app.init/tree/master/examples/bot.get.start)

```app_init
.
├── index.js        # Cтартовая точка.
└── events.js       # Обработчики
```



### index.js

Это наша стартовая точка. Здесь подгружаются модуль `Bot` и файл `events.js` в котором будут
обработчики событий.

Также нам нужно задать токен, для примера сейчас он равен `1234567890:AbCdefGhIJKlmNoPQRsTUVwxyZ`

```js {highlight:[4, 9, 13]}
require('app.init')(
// Базовые модули
    [
        'Bot'// Модуль для работы с телеграм ботом
    ],
    
// Пользовательские модули
    [
        './events.js'// Обработчики
    ]
);

$.Bot.token = process.env.BOT_TOKEN||'1234567890:AbCdefGhIJKlmNoPQRsTUVwxyZ';
$.Bot.launch();// Запускаем бота
```



### events.js

Так как задача просто проверить работает-ли бот.
Нам достаточно добавить текстовый обработчик.

`$.Bot.onText` — будет слушать все текстовые сообщения. Соответственно когда от пользователя придет какое-то сообщение,
бот скопирует его и отправит обратно.

Также для наглядности вместе с сообщением будет отправлена кнопка в название которой будет добавлен скопированный текст.

Кроме того в консоль будет выведена информация о чате с которого пришло сообщение и собственно сам текст сообщения.

```js
// Слущает все сообщения от пользователя
$.Bot.onText(function() {
// Отправляем сообещние от бота
    this.send(
    // Текст
        this.text,
        
    // Клавиатура
        [
            [this.text]// Кнопка
        ]
    );
    
// Выводим в консоль сообщение от пользователя
    console.log('this.text =', this.text);
    
// Выводим в консоль информацию о чате с которого пришло сообщение
    console.log('this.chat =', this.chat);
});
```

Результат в Telegram:

<span class="img">![](./img/bot.get.start.gif)</span>



Результат в консоли:

```js
this.text = Любой текст
this.chat = {
  id: 19793244,
  first_name: 'John',
  username: 'john33',
  type: 'private'
}
```



## Смотрите также

**Методы:**

- [this.send](./bot.this.send.md) — Отправляет сообщение от бота.


**Обработчики:**

- [$.Bot.onText](./bot.onText.md) — Слушает текстовые сообщения.
- [$.Bot.onClick](./bot.onClick.md) — Слушает клик по кнопке со встроенной клавиатуры.
- [$.Bot.onCommand](./bot.onCommand.md) — Слушает присланные команды.
- [$.Bot.onStart](./bot.onStart.md) — Слушает команду `/start`
- [$.Bot.onHelp](./bot.onHelp.md) — Слушает команду `/help`
- [$.Bot.onSettings](./bot.onSettings.md) — Слушает команду `/settings`
