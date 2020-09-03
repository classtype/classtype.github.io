# Обработчик onHelp

Исходный код находится 
[здесь](https://github.com/classtype/app.init/tree/master/examples/bot.onCommand)

`$.Bot.onHelp` — Слушает команду `/help`

В примере ниже обработчик сработает если от пользователья придет команда `/help`

```js
$.Bot.onHelp(function() {
    this.send('Высылаю помощь...');
});
```

Результат в Telegram:

<span class="img">![](./img/bot.onHelp.gif)</span>



## Смотрите также

- [this.send](./bot.this.send.md) — Отправляет сообщение от бота.
- [$.Bot.onText](./bot.onText.md) — Слушает текстовые сообщения.
- [$.Bot.onClick](./bot.onClick.md) — Слушает клик по кнопке со встроенной клавиатуры.
- [$.Bot.onCommand](./bot.onCommand.md) — Слушает присланные команды.
- [$.Bot.onStart](./bot.onStart.md) — Слушает команду `/start`
- [$.Bot.onSettings](./bot.onSettings.md) — Слушает команду `/settings`
