# Review
## Error Correcting Romaji-kana Conversion for Japanese Lanaguage Education
### INTRODUCTION
In this paper, we present an attempt to make the learner's sentences easier to read and correct for a native Japanese editor by converting errorneous text written in Roman characters into correct text written in kana while leaving foreign words unchanged.

### RELATED WORK
Our interest is mainly focused on how to deal with erroneous inputs.

### Error Tolerant Romaji-kana Conversion system
The system consists of three components
- language identification
- error correction wit approximate matching
- Roman-to-kana conversion

#### Language Identification
Language identification is done by exact matching inpuut sequences in English with a romanized Japanese dictionary.

#### Error Correction
Words which are not matched in either the English of the Japanese dictionary in the language identification step are corrected by the following method.
Spelling error correction is implemented by approximate word matching with two different measures.
- One is the cosine similarity of character unigrams.
- The other is edit distance. We use only IPADic to get approximate words.

#### Converting Roman Characters into Kana
We greedily convert Roman characters into the longest match kana characters.

### Experimental Results
The word accuracy of the proposed system is 85.0% which is about 10 points higher than Anthy's 74.5%.
The accuracy of our method with out approximate word matching is 84.5%, showing that language identification is the crucial component of our method.

### Discussion
- Matching with valid word: Matching with valid word occurs when the input mathces a word in the dictionary.
- Too large edit distance : A word whose edit distance from the input is larger than the threshold is not selected as a candidate.
- Compund words: Our system is effective when our dictinary and the learner's sentence use the same granulary of tokenization.