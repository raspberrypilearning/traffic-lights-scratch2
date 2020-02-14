## ट्रैफिक लाइट अनुक्रम

\--- task \---

एल. ई. डी. को क्रमानुसार चालू और बंद करने का प्रयास करें:

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

अब आप जानते हैं कि एल. ई. डी. को अलग-अलग कैसे नियंत्रित किया जा सकता है, और आदेशों के बीच अंतराल कैसे उत्पन्न किया जाता है, क्या आप ट्रैफिक लाइट का अनुक्रम बना सकते हैं? अनुक्रम इस प्रकार है:

- हरा चालू (Green on)
- पीली चालू (Amber on)
- लाल चालू (Red on)
- लाल और पीली चालू (Red and amber on)
- हरा चालू (Green on)

समय के बारे में सोचना महत्वपूर्ण है। प्रत्येक चरण में रोशनी कितनी देर तक चालू रेहनी चाहिए?

\--- /task \---

ट्रैफिक लाइट अनुक्रम पूरा करने के बाद, आप एक पैदल यात्री क्रॉसिंग के लिए इंटरैक्टिव ट्रैफिक लाइट बनाने के लिए बटन और बजर जोड़ने का प्रयास कर सकते हैं।