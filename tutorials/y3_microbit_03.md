# Smart Step Counter

```template
let steps = 0
basic.showNumber(steps)
```

## Step 1: Build Your Step Counter!
Look at your screen! Your red ``||variables:steps||`` variable starts at `0`.

Every time you take a step, your micro:bit feels a **shake**. Let's count your steps!

1. Open the pink ``||input:Input||`` drawer and drag out ``||input:on shake||``.
2. Open the red ``||variables:Variables||`` drawer and snap ``||variables:change steps by 1||`` inside ``||input:on shake||``.
3. Open the blue ``||basic:Basic||`` drawer and snap ``||basic:show number||`` underneath.
4. Drag the round red ``||variables:steps||`` block into ``||basic:show number||``.

**Test it!** Tap **SHAKE** on the simulator a few times. Does it count your steps?

```blocks
let steps = 0
basic.showNumber(steps)
input.onGesture(Gesture.Shake, function () {
    steps += 1
    basic.showNumber(steps)
})
```

## Step 2: Add a Reset Button!
Starting a new walk? Let's use **Button A+B** (pressing both buttons together) to reset your ``||variables:steps||`` back to `0`!

1. Open the pink ``||input:Input||`` drawer and drag out ``||input:on button A pressed||``.
2. Tap the `A` dropdown and change it to **`A+B`**.
3. Open the red ``||variables:Variables||`` drawer and snap ``||variables:set steps to 0||`` inside.
4. Snap a blue ``||basic:show number||`` underneath, and put the round red ``||variables:steps||`` block inside it!

**Test it!** Shake to count up, then tap the **A+B** button on the simulator to reset to `0`!

```blocks
input.onButtonPressed(Button.AB, function () {
    steps = 0
    basic.showNumber(steps)
})
```

## Step 3: Set a Step Goal (Condition)!
Let's make your step counter **smart**! What if it cheers for you when you reach a goal of **10 steps**?

To make the micro:bit check a rule, we use a green ``||logic:if||`` condition block!

1. Open the green ``||logic:Logic||`` drawer, grab an ``||logic:if true then||`` block, and snap it at the **bottom** inside your ``||input:on shake||`` block.
2. Open the green ``||logic:Logic||`` drawer again, grab a ``||logic:0 = 0||`` comparison block, and drop it over the word `true` inside your ``||logic:if||`` block.
3. Put the round red ``||variables:steps||`` into the **first `0`**, and type **`10`** into the **second `0`** so it reads: `if steps = 10 then`.
4. Open the blue ``||basic:Basic||`` drawer, grab ``||basic:show icon||``, and snap it inside the mouth of the ``||logic:if||`` block!

**Test it!** Shake 10 times on the simulator. Does the heart appear on step 10?

```blocks
input.onGesture(Gesture.Shake, function () {
    steps += 1
    basic.showNumber(steps)
    if (steps == 10) {
        basic.showIcon(IconNames.Heart)
    }
})
```

## Step 4: Bigger Goals Challenge! @showdialog
You mastered **Variables** and **Conditions** (`if ... then`)! Ready to level up your Smart Step Counter?

* **Challenge 1 (Custom Celebration):** Inside your ``||logic:if steps = 10||`` block, add a ``||basic:show string||`` block (like `"GOOD JOB!"`) after your icon!
* **Challenge 2 (At Least 10 Steps):** Tap the `=` sign in ``||logic:steps = 10||`` and change it to **`≥`** (greater than or equal to), OR drag another ``||logic:if||`` block underneath to celebrate a **Super Goal at 20 steps** (`steps = 20`)!
* Tap **Download** and test your Smart Step Counter by walking around!

```blocks
input.onGesture(Gesture.Shake, function () {
    steps += 1
    basic.showNumber(steps)
    if (steps == 10) {
        basic.showIcon(IconNames.Happy)
        basic.showString("YAY!")
    }
})
```

```ghost
let steps = 0
basic.showNumber(steps)
input.onGesture(Gesture.Shake, function () {
    steps += 1
    basic.showNumber(steps)
    if (steps >= 10) {
        basic.showIcon(IconNames.Heart)
        basic.showString("GOOD JOB!")
    }
})
input.onButtonPressed(Button.AB, function () {
    steps = 0
    basic.showNumber(steps)
})
```
