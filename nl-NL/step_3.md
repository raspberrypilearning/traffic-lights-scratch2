## Bedien de LED's

--- task ---

Open **Scratch 2** uit het Start menu (**Scratch 2**, niet **Scratch**).

--- /task ---

--- task ---

Voeg de **Pi GPIO** uitbreiding toe.

[[[rpi-scratch-add-pi-gpio]]]

Je zou dan twee nieuwe blokken moeten zien verschijnen bij `Meer blokken`{:class="blockmoreblocks"}:

![pi gpio blokkken in ](images/scratch2-1-annotated.png)

--- /task ---

--- task ---

Open het `Gebeurtenissen`{:class="blockevents"} paneel en sleep een blok `wanneer de goene vlag wordt aangeklikt`{:class="blockevents"} naar binnen.

```blocks
wanneer op de groene vlag wordt geklikt
```

--- /task ---

--- task ---

Open het paneel `Meer blokken`{:class="blockmoreblocks"}, sleep een `set gpio to output high`{:class="blockmoreblocks"} blok onder het vorige blok.

Zet het gpio nummer op `22`.

```blocks
wanneer groene vlag wordt aangeklikt
set gpio [22 v] to [output high v] :: extension
```

--- /task ---

--- task ---

Klik nu op de groene vlag om je code uit te voeren. Je zou de rode LED moeten zien oplichten.

--- /task ---

--- task ---

Voeg nu een blok met `wacht 1 sec.`{:class="blockcontrol"} toe voor en na het uitschakelen van de LED met `set gpio 22 to output low`{:class="blockmoreblocks"} en voeg daaromheen een **herhaal** blok toe om continu te knipperen:

```blocks
wanneer groene vlag wordt aangeklikt
herhaal 
 set gpio [22 v] to [output high v] :: extension
 wacht [1] sec.
 set gpio [22 v] to [output low v] :: extension
 wacht [1] sec.
einde
```

--- /task ---

--- task ---

Klik nogmaals op de groene vlag en je zou de LED moeten zien knipperen.

--- /task ---

--- task ---

Voeg nu wat meer `set gpio`{:class="blockmoreblocks"} blokken toe voor gpio 27 & 17, om de andere twee lichtjes ook te laten knipperen:

```blocks
wanneer groene vlag wordt aangeklikt
herhaal 
set gpio [22 v] to [output high v] :: extension
set gpio [27 v] to [output high v] :: extension
set gpio [17 v] to [output high v] :: extension
wacht [1] sec.
set gpio [22 v] to [output low v] :: extension
set gpio [27 v] to [output low v] :: extension
set gpio [17 v] to [output low v] :: extension
wacht [1] sec.
einde
```

Klik nogmaals op de groene vlag en je zou alle drie LED's moeten zien knipperen.

--- /task ---

--- task ---

Kun je de tijd in `wacht 1 sec.` wijzigen om de reeks te versnellen of te vertragen?

--- /task ---