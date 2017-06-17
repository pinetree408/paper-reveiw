# Review
## Multilingual Text Entry using Automatic Lanaguage Detection

### INTRODUCTION
Globalization has increased the need to produce multilingual text - i.e., text written in more one language -  for many users.
When producing a text in a language other than English, a user has to use text entry software corresponding to the other language which will transform the user's key stroke sequences into text of the desired language.
When producing a multilingual text on a typical computer interface, though the user has to switch IMEs every time the language changes in a multiligual text.
TypeAny detects the language that the user is using to enter text and dynamically switches IMES.

### Design of TypeAny
TypeAny solves the problem of changing IME. It is situated between the user's key entry and various IMEs.
The user's key entry sequence is input to our client software.
The client sends the sequence to the server which has the language identifier module.
This module detects the language of the key sequence and then sends the key sequence to the appropricate IME.
The selected IME then converts the key entries into text of the detected language.
- Two types of detection failure occur in TypeAny.
    - Failure A: the language should switch, but the new language is incorrectly selected.
    - Failure B: the language should not switch, but TypeAny misjudges that it should.

### Langugage Detection
#### Language Detection Model
- HMM

### Evalutaion
#### Language Detection Accuracy
We obtained 97.5% accuracy for test data consisting of 90% English, 5% Finnish and 5% Turkish; this accuracy was higher than the average for all test sets.
#### Number of Control Actions
There was a substantial decrease in the number of necessary control actions with TypeAny, over 93%, for both articles.
An especially large decrease was observed for Article 2, even though the text was almost all in English(98.9%).
