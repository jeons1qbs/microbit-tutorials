# My Name Badge

```template
basic.showString("HELLO")
```

## Step 1: Type Your Name! 
Look at your screen! You already have a ``||basic:show string||`` block.

1. Tap inside the white oval where it says `"Hello World!"`.
2. Use the iPad keyboard to delete `"Hello World!"` and type **YOUR FIRST NAME**.
3. Look at the simulator on the left or bottom. Can you see your name scrolling?

*If your name is scrolling, you are ready! Show your neighbor, or click Next for a bonus challenge!*

```blocks
basic.showString("Hello World!")
```

## Step 2: Add a Badge Icon!
Want to add a picture after your name?

1. Open the blue ``||basic:Basic||`` drawer.
2. Drag a ``||basic:show icon||`` block and snap it right under your name block.
3. Tap the heart to pick a picture that matches you (smiley, star, animal)!

Check your simulator. Does it show your name, and then your icon?

```blocks
basic.showString("NAME")
basic.showIcon(IconNames.Happy)
```

## Step 3: Fast Finisher Challenge!
Want your badge to repeat forever, or want to draw your own picture?

* **Idea A:** Open blue ``||basic:Basic||``, grab a ``||basic:forever||`` loop, and move show string block into the forever block so your badge never stops!
* **Idea B:** Grab a ``||basic:show leds||`` block and tap the squares to draw your own custom pixel badge!

```blocks
basic.forever(function () {
    basic.showString("NAME")
    basic.showIcon(IconNames.Happy)
})
```

## Step 4: Ready for Download! @showdialog
Stop here! Look at your simulator on the left:

* Is your name spelled correctly?
* Does it light up on the screen?

**Hands off your iPad now.** Look up at the front screen and wait for the teacher to show you how to assemble and pair your real micro:bit!

```ghost
basic.showString("NAME")
basic.showIcon(IconNames.Happy)
basic.showLeds(`
    . . . . .
    . . . . .
    . . # . .
    . . . . .
    . . . . .
    `)
basic.forever(function () {
	
})
basic.pause(500)
basic.clearScreen()
```
