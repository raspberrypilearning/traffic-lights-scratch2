## Contrôler les LED

\--- task \---

Try turning the lights on and off in sequence:

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

Now you know how to control the lights individually, and time the pauses between commands, can you create a traffic lights sequence? The sequence goes:

- Green on
- Amber on
- Red on
- Red and amber on
- Green on

It's important to think about timing. How long should the lights stay on for at each stage?

\--- /task \---

Once you have completed the traffic light sequence, you might want to try adding in a button and a buzzer to make an interactive traffic light for a pedestrian crossing.