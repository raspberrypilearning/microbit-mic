Le micro:bit V2 dispose d'une entrée microphone pour détecter les niveaux sonores.

## Utiliser le niveau sonore pour déclencher une action

Tu peux utiliser la valeur de `niveau sonore`{:class='microbitinput'} dans un bloc de comparaison pour déclencher une action.

```microbit
loops.everyInterval(500, function () {
    if (input.soundLevel() > 200) {
        basic.showIcon(IconNames.Sad)
    } else {
        basic.showIcon(IconNames.Happy)
    }
})
```

Dans ce code :

Une boucle est appelée toutes les demi-secondes (500 ms).

- Tu peux trouver le bloc `chaque`{:class='microbitloops'} dans le menu `Boucles`{:class='microbitloops'} dans ta boîte à outils.

Il existe une comparaison pour vérifier si le `niveau sonore`{:class='microbitinput'} a une valeur supérieure à 200.

- Tu peux trouver le bloc `si`{:class='microbitlogic'} et le bloc `>`{:class='microbitlogic'} dans le menu `Logique`{:class='microbitlogic'} dans ta boîte à outils.
- Tu peux trouver le bloc `niveau sonore`{:class='microbitinput'} dans le menu `Entrée`{:class='microbitinput'} dans ta boîte à outils.

Si le résultat de la comparaison est vrai, alors une icône de visage triste est affichée. Si c'est faux, une icône de visage souriant s'affiche.

- Tu peux trouver les blocs `montrer l'icône`{:class='microbitbasic'} dans le menu `Base`{:class='microbitbasic'} dans ta boîte à outils.

Fais glisser le niveau du microphone jusqu'à 200 sur le simulateur pour déclencher le changement des LED.

<div style="position:relative;height:0;padding-bottom:127%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:60%;height:100%;" src="https://makecode.microbit.org/---run?id=_Ccg0vpbm2PdF" allowfullscreen="allowfullscreen" sandbox="allow-popups allow-forms allow-scripts allow-same-origin" frameborder="0"></iframe></div>

## Afficher le niveau sonore

Dans le projet Sonomètre, tu as appris à tracer un graphique à barres du niveau sonore.

```microbit
loops.everyInterval(500, function () {
    led.plotBarGraph(
    input.soundLevel(),
    255
    )
})
```

Dans ce code :

Une boucle est appelée toutes les demi-secondes (500 ms).

- Tu peux trouver le bloc `chaque`{:class='microbitloops'} dans le menu `Boucles`{:class='microbitloops'} dans ta boîte à outils.

La valeur de `niveau sonore`{:class='microbitinput'} est utilisée comme valeur à afficher sur les LED.

- Tu peux trouver le bloc `niveau sonore`{:class='microbitinput'} dans le menu `Entrée`{:class='microbitinput'} dans ta boîte à outils.
- Tu peux trouver le bloc `tracer graphique en barres`{:class='microbitled'} dans le menu `LED`{:class='microbitled'} dans ta boîte à outils.
