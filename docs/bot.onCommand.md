# Обработчик onCommand

Исходный код находится 
[здесь](https://github.com/classtype/app.init/tree/master/examples/bot.onCommand)

`$.Bot.onCommand` — Слушает присланные команды.

В примере ниже обработчик будет срабатывать на любые присланные команды.

```js
$.Bot.onCommand(function() {
    this.send(`Вы отправили команду:\n/${this.command}`);
});
```

Результат в Telegram:

<span class="img">![](./img/bot.onCommand1.gif)</span>



Также можно задать определенную команду.

Здесь обработчик сработает если от пользователья придет команда `/test`

```js
$.Bot.onCommand('test', function() {
    this.send('Запускаю тест!');
});
```

Результат в Telegram:

<span class="img">![](./img/bot.onCommand2.gif)</span>



## Смотрите также

- [this.send](./bot.this.send.md) — Отправляет сообщение от бота.
- [$.Bot.onText](./bot.onText.md) — Слушает текстовые сообщения.
- [$.Bot.onClick](./bot.onClick.md) — Слушает клик по кнопке со встроенной клавиатуры.
- [$.Bot.onStart](./bot.onStart.md) — Слушает команду `/start`
- [$.Bot.onHelp](./bot.onHelp.md) — Слушает команду `/help`
- [$.Bot.onSettings](./bot.onSettings.md) — Слушает команду `/settings`
