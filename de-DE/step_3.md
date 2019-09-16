## Steuere die LEDs

\--- task \---

Öffne **Scratch 2** aus dem Programmiermenü (**Scratch 2**, nicht **Scratch**).

\--- /task \---

\--- task \---

Add the **Pi GPIO** extension.

[[[rpi-scratch-add-pi-gpio]]]

You should then see two new blocks appear in `More Blocks`{:class="blockmoreblocks"}:

![pi gpio blocks in ](images/scratch2-1-annotated.png)

\--- /task \---

\--- task \---

Open the `Events`{:class="blockevents"} panel and drag in a `when flag clicked`{:class="blockevents"} block.

```blocks
when green flag clicked
```

\--- /task \---

\--- task \---

Open the `More Blocks`{:class="blockmoreblocks"} panel, drag in a `set gpio to output high`{:class="blockmoreblocks"} block and dock it under the previous block.

Set the gpio to number `22`.

```blocks
when green flag clicked
set gpio [22 v] to [output high v] :: extension
```

\--- /task \---

\--- task \---

Klicke jetzt auf die grüne Flagge, um deinen Code zu starten. Du solltest sehen, dass die rote LED aufleuchtet.

\--- /task \---

\--- task \---

Now add a `wait 1 secs`{:class="blockcontrol"} block before and after turning the LED off with `set gpio 22 to output low`{:class="blockmoreblocks"}, and wrap it in a **forever** block to blink continuously:

```blocks
when green flag clicked
forever
set gpio [22 v] to [output high v] :: extension
wait [1] secs
set gpio [22 v] to [output low v] :: extension
wait [1] secs
end
```

\--- /task \---

\--- task \---

Klicke erneut auf die grüne Flagge und du solltest die LED blinken sehen.

\--- /task \---

\--- task \---

Now add some more `set gpio`{:class="blockmoreblocks"} blocks to introduce the other two lights on gpio 27 & 17, and make them all flash on and off:

```blocks
when green flag clicked
forever
set gpio [22 v] to [output high v] :: extension
set gpio [27 v] to [output high v] :: extension
set gpio [17 v] to [output high v] :: extension
wait [1] secs
set gpio [22 v] to [output low v] :: extension
set gpio [27 v] to [output low v] :: extension
set gpio [17 v] to [output low v] :: extension
wait [1] secs
end
```

Klicke erneut auf die grüne Flagge und du solltest sehen, dass alle drei Lichter zusammen blinken.

\--- /task \---

\--- task \---

Can you change the number in `wait 1 secs`{:class="blockcontrol"} to speed up or slow down the sequence?

\--- /task \---