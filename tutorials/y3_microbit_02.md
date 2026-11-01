# Super Counter & Inputs

```template
let count = 0
basic.showNumber(count)
```

## Step 1: Count with Button A!
Look at your screen! You already have a red variable called ``||variables:count||`` that starts at `0` and shows on the LED screen.

Let's make ``||variables:count||`` go up by `1` every time you press **Button A**!

1. Open the pink ``||input:Input||`` drawer and drag out ``||input:on button A pressed||``.
2. Open the red ``||variables:Variables||`` drawer, drag ``||variables:change count by 1||``, and snap it inside ``||input:on button A pressed||``.
3. Open the blue ``||basic:Basic||`` drawer, drag ``||basic:show number||``, and snap it right underneath.
4. Open the red ``||variables:Variables||`` drawer, grab the round ``||variables:count||`` block, and drop it into ``||basic:show number||`` (replacing the `0`).

**Test it!** Tap **Button A** on the simulator. Does your number go up: `1, 2, 3`?

```blocks
let count = 0
basic.showNumber(count)
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
})
```

## Step 2: Count a Clap (Loud Sound)!
Can your micro:bit count using its **ears** (microphone) instead of a button? Let's count loud sounds like claps!

1. Open the pink ``||input:Input||`` drawer and drag out ``||input:on loud sound||``.
2. Inside ``||input:on loud sound||``, build the **same two-block pattern**:
   * Red ``||variables:change count by 1||``
   * Blue ``||basic:show number||`` with the round red ``||variables:count||`` inside!

**Test it!** On the simulator, slide the pink microphone bar up past the triangle (or tap **Download** and clap near your micro:bit)!

```blocks
input.onSound(DetectedSound.Loud, function () {
    count += 1
    basic.showNumber(count)
})
```

## Step 3: Count a Shake!
Now you know the secret counter pattern! Can you make it count when you **shake** your micro:bit?

1. Open the pink ``||input:Input||`` drawer and grab ``||input:on shake||``.
2. Snap the **same two blocks** inside ``||input:on shake||``:
   * ``||variables:change count by 1||``
   * ``||basic:show number||`` with ``||variables:count||`` inside!

**Test it!** Tap the white **SHAKE** dot on the simulator (or download and shake your micro:bit)!

```blocks
input.onGesture(Gesture.Shake, function () {
    count += 1
    basic.showNumber(count)
})
```

## Step 4: Reset Your Counter! @showdialog
What happens when your number gets too big and you want to start over at **zero**? Let's make a **Reset Button**!

* **Your Mission:** Make **Button B** reset ``||variables:count||`` back to `0`!
* Look closely: Instead of *changing* ``||variables:count||``, you need to **set** ``||variables:count||`` to `0`.

1. Open pink ``||input:Input||``, drag out ``||input:on button A pressed||``, and tap the `A` dropdown to change it to **`B`**.
2. Open red ``||variables:Variables||`` and snap ``||variables:set count to 0||`` inside.
3. Add blue ``||basic:show number||`` with the round red ``||variables:count||`` inside so the screen updates to `0`!
4. Tap **Download** and test all your inputs and your Reset button!

```blocks
input.onButtonPressed(Button.B, function () {
    count = 0
    basic.showNumber(count)
})
```

```ghost
let count = 0
basic.showNumber(count)
input.onButtonPressed(Button.A, function () {
    count += 1
    basic.showNumber(count)
})
input.onSound(DetectedSound.Loud, function () {
    count += 1
    basic.showNumber(count)
})
input.onGesture(Gesture.Shake, function () {
    count += 1
    basic.showNumber(count)
})
input.onButtonPressed(Button.B, function () {
    count = 0
    basic.showNumber(count)
})
```
