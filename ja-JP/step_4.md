## LEDの制御

\--- task \---

Try turning the lights on and off in sequence:

```blocks
制御のパネルを開き、<strong>1秒待つ</strong>のブロックを <strong>set gpio 赤 to output high 、set gpio 赤 to output low</strong>のブロック前後に追加します。連続的に点滅させるために、<strong>ずっと</strong>ブロックの中に入れます。：
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