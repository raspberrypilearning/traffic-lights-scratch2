## Eine Verkehrsampel steuern

--- task ---

Versuche die Leuchtdioden der Reihe nach ein- und auszuschalten:

```blocks
Wenn die grüne Flagge angecklickt
wiederhole fortlaufend
set gpio [22 v] to [output high v] :: extension
warte [1] Sek.
set gpio [27 v] to [output high v] :: extension
warte [1] Sek.
set gpio [17 v] to [output high v] :: extension
warte [1] Sek.
set gpio [22 v] to [output low v] :: extension
warte [1] Sek.
set gpio [27 v] to [output low v] :: extension
warte [1] Sek.
set gpio [17 v] to [output low v] :: extension
warte [1] Sek.
ende
```

--- /task ---

--- task ---

Jetzt weisst du, wie man die Leuchtdioden individuell steuert und Pausen zwischen den Befehlen einstellt. Kannst du die Abfolge einer Verkehrsampel zusammenstellen? Die Reihenfolge ist:

- Rot an
- Rot und Gelb an
- Grün an
- Gelb an
- Rot an

Um eine gute Verkehrsampel zu bekommen, ist es wichtig darüber nachzudenken, wie lange die einzelnen Leutdioden an sein sollen. Wie lange sollten die Leutdioden in jeder Phase eingeschaltet bleiben?

--- /task ---

Sobald du die Steuerung der Verkehrsampel abgeschlossen hast, kannst du versuchen, einen Taster und einen Summer hinzuzufügen, um eine interaktive Fußgängerampel zu erstellen.


***
Dieses Projekt wurde von freiwilligen Helfern übersetzt:

Holger Wittmann

Sandra Gavin

Karl Schuh

Helmut Schlimper

Dank freiwilliger Helfer können wir Menschen auf der ganzen Welt die Möglichkeit geben, in ihrer eigenen Sprache zu lernen. Du kannst uns helfen, mehr Menschen zu erreichen, indem Du dich freiwillig zum Übersetzen meldest - weitere Informationen unter [rpf.io/translate](https://rpf.io/translate).