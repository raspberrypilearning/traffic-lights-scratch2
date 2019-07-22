## A közlekedési lámpa ciklusa

\--- task \---

Próbáld meg sorrendben ki és bekapcsolni a lámpákat:

```blocks
⚑ -ra kattintáskor
mindig 
 set gpio [22 v] to [output high v] :: extension
 várj [1] mp-et
 set gpio [27 v] to [output high v] :: extension
 várj [1] mp-et
 set gpio [17 v] to [output high v] :: extension
 várj [1] mp-et
 set gpio [22 v] to [output low v] :: extension
 várj [1] mp-et
 set gpio [27 v] to [output low v] :: extension
 várj [1] mp-et
 set gpio [17 v] to [output low v] :: extension
 várj [1] mp-et
end
```

\--- /task \---

\--- task \---

Most már tudod, hogyan kell egyedileg irányítani a fényeket, és a parancsok közötti szünetek idejét beállítani, létre tudod hozni a közlekedési lámpa ciklust? A fények sorrendje:

- Zöld világít
- Sárga világít
- Piros világít
- Piros és sárga világít
- Zöld világít

It's important to think about timing. How long should the lights stay on for at each stage?

\--- /task \---

Once you have completed the traffic light sequence, you might want to try adding in a button and a buzzer to make an interactive traffic light for a pedestrian crossing.