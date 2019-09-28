## Steuere die LEDs (Leuchtdioden)

\--- task \---

Öffne **Scratch 2** unter dem Menüpunkt Entwicklung(**Scratch 2**, nicht **Scratch**).

\--- /task \---

\--- task \---

Füge die **Pi GPIO** Erweiterung hinzu.

[[[rpi-scratch-add-pi-gpio]]]

Es sollten nun unter `Weitere Blöcke`{:class="blockmoreblocks"} zwei neue Befehlsblöcke zu sehen:

![pi gpio blocks in ](images/scratch2-1-annotated.png)

\--- /task \---

\--- task \---

Klick auf die Gruppe `Ereignisse`{:class="blockevents"} und ziehe den Block `Wenn die grüne Flagge angeklickt wird`{:class="blockevents"} in den Skript Bereich.

```blocks
Wenn die grüne Flagge angeklickt 
```

\--- /task \---

\--- task \---

Klick auf die Gruppe `Weitere Blöcke`{:class="blockmoreblocks"} und ziehe den `set gpio to output high`{:class="blockmoreblocks"} Block in den Skript Bereich und hänge es unter den vorherigen Block ein.

Setze die gpio Nummer auf `22`.

```blocks
when green flag clicked
set gpio [22 v] to [output high v] :: extension
```

\--- /task \---

\--- task \---

Klicke jetzt auf die grüne Flagge, um deinen Code zu starten. Die rote LED (Leuchtdiode) sollte nun aufleuchtet.

\--- /task \---

\--- task \---

Nun hänge einen `warte 1 Sek.`{:class="blockcontrol"} Block unter die vorherigen Blöcke. Und um die Leuchtdiode auszuschalten einen `set gpio 22 to output low`{:class="blockmoreblocks"} Block, gefolgt von einem <0>warte 1 Sek.</0>{:class="blockcontrol"} Block. Umklammere das alles mit einem **wiederhole fortlaufend** Block, um alles fortlaufend blinken zu lassen:

```blocks
Wenn die grüne Flagge angeklickt
wiederhole fortlaufend
set gpio [22 v] to [output high v] :: extension
warte [1] Sek.
set gpio [22 v] to [output low v] :: extension
warte [1] Sek.
ende
```

\--- /task \---

\--- task \---

Klicke wieder auf die grüne Flagge und du solltest die Leuchtdiode blinken sehen.

\--- /task \---

\--- task \---

Füge nun weitere `set gpio`{:class="blockmoreblocks"} Blöcke hinzu, um die beiden anderen Leuchtdioden an gpio 27 und 17 einzubinden, so dass alle Leuchtdioden blinken:

```blocks
Wenn die grüne Flagge angeklickt
wiederhole fortlaufend
set gpio [22 v] to [output high v] :: extension
set gpio [27 v] to [output high v] :: extension
set gpio [17 v] to [output high v] :: extension
warte [1] Sek.
set gpio [22 v] to [output low v] :: extension
set gpio [27 v] to [output low v] :: extension
set gpio [17 v] to [output low v] :: extension
warte [1] Sek.
ende
```

Klicke erneut auf die grüne Flagge und du solltest alle drei Leuchtdioden zusammen blinken sehen.

\--- /task \---

\--- task \---

Can you change the number in `wait 1 secs`{:class="blockcontrol"} to speed up or slow down the sequence?

\--- /task \---