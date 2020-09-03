# Обработчик onStart

Исходный код находится 
[здесь](https://github.com/classtype/app.init/tree/master/examples/bot.onCommand)

`$.Bot.onStart` — Слушает команду `/start`

В примере ниже обработчик сработает если от пользователья придет команда `/start`

```js
$.Bot.onStart(function() {
    this.send('Начинаю запуск...');
});
```

Результат в Telegram:

<span class="img">![](./img/bot.onStart.gif)</span>



## Смотрите также

- [this.send](./bot.this.send.md) — Отправляет сообщение от бота.
- [$.Bot.onText](./bot.onText.md) — Слушает текстовые сообщения.
- [$.Bot.onClick](./bot.onClick.md) — Слушает клик по кнопке со встроенной клавиатуры.
- [$.Bot.onCommand](./bot.onCommand.md) — Слушает присланные команды.
- [$.Bot.onHelp](./bot.onHelp.md) — Слушает команду `/help`
- [$.Bot.onSettings](./bot.onSettings.md) — Слушает команду `/settings`
