The micro:bit V2 has a microphone input to sense sound levels.

## Use the sound level to trigger an action

You can use the value of `sound level`{:class='microbitinput'} in a comparison block to trigger an action.

```microbit
loops.everyInterval(500, function () {
    if (input.soundLevel() > 200) {
        basic.showIcon(IconNames.Sad)
    } else {
        basic.showIcon(IconNames.Happy)
    }
})
```

In this code:

A loop is called every half second (500 ms).

- You can find the `every`{:class='microbitloops'} block in the `Loops`{:class='microbitloops'} menu in your Toolbox.

There is a comparison to check if the `sound level`{:class='microbitinput'} has a value of more than 200.

- You can find the `if`{:class='microbitlogic'} block and the `>`{:class='microbitlogic'} block in the `Logic`{:class='microbitlogic'} menu in your Toolbox.
- You can find the `sound level`{:class='microbitinput'} block in the `Input`{:class='microbitinput'} menu in your Toolbox.

If the result of the comparison is True, then a sad face icon is shown. If it is False, then a smiley face icon is shown.

- You can find `show icon`{:class='microbitbasic'} blocks in the `Basic`{:class='microbitbasic'} menu in your Toolbox.

Slide the microphone level up to 200 on the simulator to trigger the LEDs to change.

<div style="position:relative;height:0;padding-bottom:127%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:60%;height:100%;" src="https://makecode.microbit.org/---run?id=_Ccg0vpbm2PdF" allowfullscreen="allowfullscreen" sandbox="allow-popups allow-forms allow-scripts allow-same-origin" frameborder="0"></iframe></div>

## Display the sound level

In the Sound meter project, you learnt how to plot a bar graph of the sound level.

```microbit
loops.everyInterval(500, function () {
    led.plotBarGraph(
    input.soundLevel(),
    255
    )
})
```

In this code:

A loop is called every half second (500 ms).

- You can find the `every`{:class='microbitloops'} block in the `Loops`{:class='microbitloops'} menu in your Toolbox.

The value of `sound level`{:class='microbitinput'} is used as the value to display on the LEDs.

- You can find the `sound level`{:class='microbitinput'} block in the `Input`{:class='microbitinput'} menu in your Toolbox.
- You can find the `plot bar graph`{:class='microbitled'} block in the `Led`{:class='microbitled'} menu in your Toolbox.
