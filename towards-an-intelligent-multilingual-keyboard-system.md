# Review
## Towards an Intelligent Multilingual Keyboard System

### INTRODUCTION
For Thai users, there are always two annoyances while typing Thai-English bilingual documents, which are usual for Thais.
- The first is when the users want to switch from typing Thai to English, they have to input a special key to tell the operating system to change the language mode.
- The second is that Thai has more than 100 alphabets, to input about half of all Thai characters, the user has to use combinations of two keys(chift key + another key) to input them.
This paper proposes a practical solution for these disturbances by applying trigram character probabilistic model and error-correction rules.

### THE APPROACH
#### Overview
To solve this problem, there are basically two steps: language identification and Thai key prediction.

#### Language Identification
In general, different languages are not typed connectedly without spaces between them.
The language-identification process starts when a non-space character is typed atfer a space.
The language being inputted is identified by comparing the key sequence probability.

### EXPERIMENTS
#### Language Identification
As a conclusion the first 6 characters of the token are enough to yield a high accuracy on English-Thai language identificaion.

### CONCLUSION
Through this system typing is much more easier and enjoyable for Thais.
This technique is expected to be able to apply to other Aisan languages.
