# Клавиатура (встроенная)

Исходный код находится 
[здесь](https://github.com/classtype/app.init/tree/master/examples/bot.this.send)

Вместе с сообщением мы можем передавать два вида клавиатуры [обычную](./bot.keyboard.md) и `встроенную`

```js {highlight:['3-5']}
$.Bot.onText('Встроенная клавиатура.', function() {
    this.send('Пример встроенной клавиатуры.', [
        ['Кнопка 1','button_1'],
        ['Кнопка 2','button_2'],
        ['Кнопка 3','button_3']
    ]);
});

$.Bot.onClick(function() {
    this.send(`Вы кликнули по кнопке:\n"${this.button_id}"`);
    this.complete();
});
```

Результат в Telegram:

<span class="img">![](./img/bot.inlineKeyboard.gif)</span>



## Смотрите также

- [Клавиатура (обычная)](./bot.keyboard.md)
- [this.send](./bot.this.send.md) — Отправляет сообщение от бота.
- [$.Bot.onText](./bot.onText.md) — Слушает текстовые сообщения.
- [$.Bot.onClick](./bot.onClick.md) — Слушает клик по кнопке со встроенной клавиатуры.
