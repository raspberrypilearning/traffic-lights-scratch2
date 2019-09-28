## Die Verkehrsampel Folge

\--- task \---

Versuche die Leuchtdioden der Reihe nach ein- und auszuschalten:

```blocks
when green flag clicked
forever
set gpio [22 v] to [output high v] :: extension
wait [1] secs
set gpio [27 v] to [output high v] :: extension
wait [1] secs
set gpio [17 v] to [output high v] :: extension
wait [1] secs
set gpio [22 v] to [output low v] :: extension
wait [1] secs
set gpio [27 v] to [output low v] :: extension
wait [1] secs
set gpio [17 v] to [output low v] :: extension
wait [1] secs
end
```

\--- /task \---

\--- task \---

Jetzt weisst du, wie man die Lichter individuell steuert und die Pausen zwischen den Befehlen einstellt. Kannst du eine Ampelsequenz erstellen? Die Reihenfolge lautet:

- Grün ein
- Gelb an
- Rot an
- Rot und Gelb an
- Grün an

Es ist wichtig, über das Timing nachzudenken. Wie lange sollten die Lichter in jeder Phase eingeschaltet bleiben?

\--- /task \---

Wenn du die Ampelsequenz abgeschlossen hast, kannst du versuchen, eine Schaltfläche und einen Summer hinzuzufügen, um eine interaktive Ampel für einen Fußgängerübergang zu erstellen.