Το micro:bit V2 διαθέτει είσοδο μικροφώνου για την ανίχνευση των επιπέδων ήχου.

## Χρησιμοποίησε το επίπεδο ήχου για να ενεργοποιήσεις μια ενέργεια

Μπορείς να χρησιμοποιήσεις την τιμή του `sound level`{:class='microbitinput'} σε ένα μπλοκ σύγκρισης για να ενεργοποιήσεις μια ενέργεια.

```microbit
loops.everyInterval(500, function () {
    if (input.soundLevel() > 200) {
        basic.showIcon(IconNames.Sad)
    } else {
        basic.showIcon(IconNames.Happy)
    }
})
```

Σε αυτόν τον κώδικα:

Ένας βρόχος καλείται κάθε μισό δευτερόλεπτο (500 ms).

- Μπορείς να βρες το μπλοκ `every`{:class='microbitloops'} στο μενού `Βρόχοι`{:class='microbitloops'} στην Εργαλειοθήκη σου.

Υπάρχει μια σύγκριση για να ελέγξεις αν το `sound level`{:class='microbitinput'} έχει τιμή μεγαλύτερη από 200.

- Μπορείς να βρεις το μπλοκ `εάν`{:class='microbitlogic'} και το μπλοκ `>`{:class='microbitlogic'} στο μενού `Λογική`{:class='microbitlogic'} στην Εργαλειοθήκη σου.
- Μπορείς να βρεις το μπλοκ `sound level`{:class='microbitinput'} στο μενού 'Είσοδος\`{:class='microbitinput'} στην Εργαλειοθήκη σου.

Εάν το αποτέλεσμα της σύγκρισης είναι Αληθές, τότε εμφανίζεται ένα εικονίδιο λυπημένου προσώπου. Εάν είναι Ψευδές, τότε εμφανίζεται ένα εικονίδιο με χαμογελαστό πρόσωπο.

- Μπορείς να βρεις μπλοκ `εμφάνιση εικονιδίου`{:class='microbitbasic'} στο μενού `Βασικά`{:class='microbitbasic'} στην Εργαλειοθήκη σου.

Σύρε το επίπεδο του μικροφώνου μέχρι το 200 στον προσομοιωτή για να ενεργοποιήσεις την αλλαγή των LED.

<div style="position:relative;height:0;padding-bottom:127%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:60%;height:100%;" src="https://makecode.microbit.org/---run?id=_Ccg0vpbm2PdF" allowfullscreen="allowfullscreen" sandbox="allow-popups allow-forms allow-scripts allow-same-origin" frameborder="0"></iframe></div>

## Εμφάνιση της στάθμης ήχου

Στο έργο Μετρητής ήχου, έμαθες πώς να σχεδιάζεις ένα γράφημα ράβδων της στάθμης του ήχου.

```microbit
loops.everyInterval(500, function () {
    led.plotBarGraph(
    input.soundLevel(),
    255
    )
})
```

Σε αυτόν τον κώδικα:

Ένας βρόχος καλείται κάθε μισό δευτερόλεπτο (500 ms).

- Μπορείς να βρες το μπλοκ `every`{:class='microbitloops'} στο μενού `Βρόχοι`{:class='microbitloops'} στην Εργαλειοθήκη σου.

Η τιμή του `sound level`{:class='microbitinput'} χρησιμοποιείται ως η τιμή που εμφανίζεται στα LED.

- Μπορείς να βρεις το μπλοκ `sound level`{:class='microbitinput'} στο μενού `Είσοδος`{:class='microbitinput'} στην Εργαλειοθήκη σου.
- Μπορείς να βρεις το μπλοκ `plot bar graph`{:class='microbitled'} στο μενού `Led`{:class='microbitled'} στην Εργαλειοθήκη σου.
