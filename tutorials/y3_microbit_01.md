# My Name Badge & Health Reminder

```template
basic.showString("Hello World!")
```

## Step 1: Check Your micro:bit!
Look at the bottom-left corner of your screen at the purple button:

* **First time using this micro:bit?** Tap the **purple Download button** (or the **...** dots next to it) 
* **Wait for next instructions.**

* **Already paired before?** You are all set! 

*(Swipe or scroll this tutorial box up if the Next button is hidden at the bottom)*. Tap **Next** to start!

```blocks
basic.showString("Hello World!")
```

## Step 2: The Name Badge Puzzle! @unplugged
Here is the puzzle! Can you assemble your name badge to show your name and a badge icon?


```block
basic.showString("NAME")
basic.showIcon(IconNames.Happy)
```

Look at the pieces above:
1. Tap inside `"Hello World!"` and type **YOUR FIRST NAME**.
2. Open the blue ``||basic:Basic||`` drawer and grab a ``||basic:show icon||`` block.
3. Snap it right under your name!
4. Tap download when you're done.

Tap **Next** to assemble your pieces!

## Step 3: Assemble Your Badge!
1. Tap inside `"Hello World!"` and type **YOUR FIRST NAME**.
2. Open the blue ``||basic:Basic||`` drawer.
3. Drag a ``||basic:show icon||`` block and snap it right under your name!
4. Tap the heart to pick your favorite badge icon!
5. Tap download when you're done.

```blocks
basic.showString("NAME")
basic.showIcon(IconNames.Happy)
```

## Step 4: Health Reminder Challenge! @showdialog
Time for a new mission: Let's create a **Health Reminder Badge** to help people live healthier lives!

* **Your Mission:** Remind someone to drink water, stretch, or take a deep breath **every 30 seconds** (30,000 ms).
* Drag your name blocks to the left to delete them, or build right next to them!
* Open the blue ``||basic:Basic||`` drawer:
  1. Grab a ``||basic:forever||`` loop.
  2. Put your health message (like `"DRINK WATER!"` or a heart icon) inside it.
  3. Add a ``||basic:pause (ms)||`` block and set it to **30000** ms!

```blocks
basic.forever(function () {
    basic.showString("DRINK WATER!")
    basic.showIcon(IconNames.Heart)
    basic.pause(30000)
})
```

```ghost
basic.showString("DRINK WATER!")
basic.showIcon(IconNames.Heart)
basic.pause(30000)
basic.forever(function () {})
```
