# Обработчик onSettings

Исходный код находится 
[здесь](https://github.com/classtype/app.init/tree/master/examples/bot.onCommand)

`$.Bot.onSettings` — Слушает команду `/settings`

В примере ниже обработчик сработает если от пользователья придет команда `/settings`

```js
$.Bot.onSettings(function() {
    this.send('Загружаю настройки...');
});
```

Результат в Telegram:

<span class="img">![](./img/bot.onSettings.gif)</span>



## Смотрите также

- [this.send](./bot.this.send.md) — Отправляет сообщение от бота.
- [$.Bot.onText](./bot.onText.md) — Слушает текстовые сообщения.
- [$.Bot.onClick](./bot.onClick.md) — Слушает клик по кнопке со встроенной клавиатуры.
- [$.Bot.onCommand](./bot.onCommand.md) — Слушает присланные команды.
- [$.Bot.onStart](./bot.onStart.md) — Слушает команду `/start`
- [$.Bot.onHelp](./bot.onHelp.md) — Слушает команду `/help`
