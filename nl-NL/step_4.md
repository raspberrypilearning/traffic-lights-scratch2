## Verkeerslichten volgorde

--- task ---

Probeer de lichten achter elkaar in en uit te schakelen:

```blocks
wanneer groene vlag wordt aangeklikt
herhaal 
 set gpio [22 v] to [output high v] :: extension
 wacht [1] sec.
 set gpio [27 v] to [output high v] :: extension
 wacht [1] sec.
 set gpio [17 v] to [output high v] :: extension
 wacht [1] sec.
 set gpio [22 v] to [output low v] :: extension
 wacht [1] sec.
 set gpio [27 v] to [output low v] :: extension
 wacht [1] sec.
 set gpio [17 v] to [output low v] :: extension
 wacht [1] sec.
einde
```

--- /task ---

--- task ---

Nu weet je hoe je de lichten en de pauzes tussen opdrachten afzonderlijk kunt besturen, kun je nu een goede volgorde en tijdsduur voor een verkeerslicht maken? De volgorde is:

- Rood uit, groen aan
- Groen uit, oranje aan
- Oranje uit, rood aan
- Rood en oranje aan
- Groen aan

Het is belangrijk om na te denken over de tijdsduur van elk licht. Hoe lang moet het licht in elke fase aan blijven?

--- /task ---

Nadat je de volgorde van het verkeerslicht hebt voltooid, kunt je proberen een knop en een zoemer toe te voegen om een ​​interactief verkeerslicht te maken voor een zebrapad.


**Door de community geleverde vertaling**

Dit project werd vertaald door **Cor Groot** en gecontroleerd door **Jeroen Dekker**/**Robert-Jan Kempenaar**.

Onze geweldige vertalers helpen ons om kinderen over de hele wereld de kans te geven te leren coderen. Jij kunt ons helpen nog meer kinderen te bereiken door onze projecten te vertalen - lees meer op [rpf.io/translators](https://rpf.io/translators).