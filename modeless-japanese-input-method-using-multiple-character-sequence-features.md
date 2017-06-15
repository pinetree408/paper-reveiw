# Review
## Modeless Japanese Input Method Using Multiple Character Sequence Features

### INTRODUCTION
Recently, the rapid growth of globalization has increased opportunities/situations where multilingual documents, such as mixed with Japanese and another language, are created.
We use Japanese input software for inputting Japanese. However, to produce such documents with a conventional Japanese input method, the input mode must be switched between Japanese and Alphanumeric(Alphabet plus numbers) frequently, which requires so much time.
To solve such problems, this paper proposes a modeless Japanese input method to distinguish whether to convert into Kana from ASCII character sequences, as a pre-process for the Kana-to-Kanji conversion.

### RELATED WORK
In this paper, we focus on Japanese input method to input multilingual texts.
- The Chinese input method proposed by Chen and Lee can discriminate Chinese and English.
- The Pinyin-to-Chinese conversion is similar to alphabet-to-Kana, but the approach has room for improvement
- Microsoft IME allows Japanese-English mixed texts by the stroke of Shift key, which is needed to clearly show for computers, if the input language is Japanese or English, making the operation more complicated.
- PUNTO switcher aims at switches only between Russian and English
- Keyboard Ninja allows multi-language switches.

### DISCRIMINATING FOR KANA CONVERSION USING SOME FEATURES
- In our discriminating process, a language tag t = {t1, t2 ... tn} is output for each ASCII character x = {x1, x2 ... xn} when our system receives user's input.
- A character n-gram is a substring of backward and forward at discriminating focus point i.
- A character-type n-gram is a sequence converted character into a character-type.
- A history sequence is a sequence of the tag of dicriminated result in the range of i-m to i-1.

### PROCEDURE
#### Outline
- the system receives ACSII character sequence input by user.
- it discriminates the necessity of Kana conversion against each ASCII character in ASCII sequence

#### The process of Generating Kana Conversion Discriminative Model
- Kanji included in a corpus to generate our model are converted into Kana using a Japanese morphological analyzer called MeCab.
- Kana ara converted into ASCII character sequences using a typical Kana-to-ASCII table of the Mozc Japanese input software.
- the charcater n-gram and character-type n-gram are generated from ASCII sequences.

#### CONCLUSION
This paper proposes a modeless Japanese input method to discriminate whether to convert into Kana from ASCII character sequence by using n-grams of character and character-type, and a history sequence, instead of dictionares.
