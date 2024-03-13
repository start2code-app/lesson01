# My Tutorial xxx

## Introduction step @showhint

![Lights flashing](https://github.com/start2code-app/mytutorial/blob/master/docs/static/games-sprite.jpg?raw=true)


## Step 1: Make a variable
Get a ``||input:temperature||`` block and place it in the value slot of ``||basic:show number||``.

```blocks
input.onButtonPressed(Button.A, function () {
    if (pad_x > 0) {
        led.unplot(pad_x, pad_y)
        pad_x += -1
        led.plot(pad_x, pad_y)
    }
})
input.onButtonPressed(Button.B, function () {
    if (pad_x < 4) {
        led.unplot(pad_x, pad_y)
        pad_x += 1
        led.plot(pad_x, pad_y)
    }
})
let ypos = 0
let xpos = 0
let pad_x = 0
let pad_y = 0
basic.clearScreen()
game.setScore(1)
pad_y = 4
pad_x = 0
led.plot(pad_x, pad_y)
basic.forever(function () {
    xpos = randint(0, 4)
    for (let index = 0; index <= 4; index++) {
        ypos = index
        led.plot(xpos, ypos)
        basic.pause(150)
        led.unplot(xpos, ypos)
    }
    led.plot(pad_x, pad_y)
    if (pad_x == xpos && pad_y == ypos) {
        basic.showNumber(game.score())
        basic.pause(2000)
        game.addScore(1)
    }
})
```


# step3

Get a ``||input:temperature||`` block and place it in the value slot of ``||basic:show number||``.

```blocks
forever(function() {
    basic.showNumber(input.temperature())
    basic.pause(1000)
})
```

Try it on your microbit

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>


