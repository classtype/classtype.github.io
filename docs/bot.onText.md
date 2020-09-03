# Обработчик onText

Исходный код находится 
[здесь](https://github.com/classtype/app.init/tree/master/examples/bot.onText)

`$.Bot.onText` — Слушает текстовые сообщения.

В примере ниже обработчик будет срабатывать на любые текстовые сообщения.

```js
$.Bot.onText(function() {
    this.send(`Вы отправили:\n"${this.text}"`);
});
```

Результат в Telegram:

<span class="img">![](./img/bot.onText1.gif)</span>



Также можно задать определенное сообщение.

Здесь обработчик сработает если от пользователья придет сообщение `Привет бот`

```js
$.Bot.onText('Привет бот', function() {
    this.send(`Привет ${this.chat.first_name}!`);
});
```

Результат в Telegram:

<span class="img">![](./img/bot.onText2.gif)</span>



## Смотрите также

- [this.send](./bot.this.send.md) — Отправляет сообщение от бота.
- [$.Bot.onClick](./bot.onClick.md) — Слушает клик по кнопке со встроенной клавиатуры.
- [$.Bot.onCommand](./bot.onCommand.md) — Слушает присланные команды.
- [$.Bot.onStart](./bot.onStart.md) — Слушает команду `/start`
- [$.Bot.onHelp](./bot.onHelp.md) — Слушает команду `/help`
- [$.Bot.onSettings](./bot.onSettings.md) — Слушает команду `/settings`
