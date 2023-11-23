De micro:bit V2 heeft een microfoon om geluidsniveaus te detecteren.

## Gebruik de microfoon om een actie te activeren

Je kunt de waarde van `geluidsniveau`{:class='microbitinput'} gebruiken in een vergelijkingsblok om een actie te starten.

```microbit
loops.everyInterval(500, function () {
    if (input.soundLevel() > 200) {
        basic.showIcon(IconNames.Sad)
    } else {
        basic.showIcon(IconNames.Happy)
    }
})
```

In deze code:

Wordt elke halve seconde (500 ms) een lus aangeroepen.

- Je kunt het blok `elk`{:class='microbitloops'} vinden in het `Lussen`{:class='microbitloops'} menu in je Toolbox.

Er is een vergelijking om te controleren of het `geluidsniveau`{:class='microbitinput'} een waarde van meer dan 200 heeft.

- Je kunt het blok `als`{:class='microbitlogic'} en het `>`{:class='microbitlogic'} blok in het `Logisch`{:class='microbitlogic'} menu vinden in je Toolbox.
- Je kunt het blok `geluidsniveau`{:class='microbitinput'} vinden in het `Invoer`{:class='microbitinput'} menu in je Toolbox.

Als het resultaat van de vergelijking waar is, dan wordt er een pictogram van een verdrietig gezicht getoond. Als het onwaar is, dan wordt een smiley getoond.

- Je kunt `toon pictogram`{:class='microbitbasic'} blokken vinden in het `Basis`{:class='microbitbasic'} menu in je Toolbox.

Schuif het niveau van de microfoon tot 200 op de simulator om de LED's te laten veranderen.

<div style="position:relative;height:0;padding-bottom:127%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:60%;height:100%;" src="https://makecode.microbit.org/---run?id=_Ccg0vpbm2PdF" allowfullscreen="allowfullscreen" sandbox="allow-popups allow-forms allow-scripts allow-same-origin" frameborder="0"></iframe></div>

## Geef het geluidsniveau weer

In het project Geluidsmeter heb je geleerd hoe je een staafdiagram van het geluidsniveau kunt tekenen.

```microbit
loops.everyInterval(500, function () {
    led.plotBarGraph(
    input.soundLevel(),
    255
    )
})
```

In deze code:

Wordt elke halve seconde (500ms) een lus aangeroepen.

- Je kunt het blok `elk`{:class='microbitloops'} vinden in het `Lussen`{:class='microbitloops'} menu in je Toolbox.

De waarde van `geluidsniveau`{:class='microbitinput'} wordt gebruikt als de waarde die op de LED's moet worden weergegeven.

- Je kunt het blok `geluidsniveau`{:class='microbitinput'} vinden in het `Invoer`{:class='microbitinput'} menu in je Toolbox.
- Je kunt het blok `plot bar graph`{:class='microbitled'} vinden in het menu `Lichtjes`{:class='microbitled'} in je Toolbox.
