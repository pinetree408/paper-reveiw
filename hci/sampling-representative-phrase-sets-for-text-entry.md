# Review
## Purpose of Review

To apply the techniques used in this paper to generate well made korean corpus

## Sampling Representative Phrase Sets for Text Entry

```
@inproceedings{paek2011sampling,
  title={Sampling representative phrase sets for text entry experiments: a procedure and public resource},
  author={Paek, Tim and Hsu, Bo-June Paul},
  booktitle={Proceedings of the SIGCHI Conference on Human Factors in Computing Systems},
  pages={2477--2480},
  year={2011},
  organization={ACM}
}
```

### ABSTRACT
To demonstrate representativeness, they correlated the distridution of single letters in their phrase set to a relatively small corpus of Enlish prior to 1966, which may not reflect the style of text input today.

### INTRODUCTION
Text entry experiments evaluating the effectiveness of various input techinques often employ a procedure whereby users are promted with natural language phrases which they are instructed to enter as stimuli.

Unfortunately, the letter frequences derive from a dated corpus containing publications prior to 1966, which may not reflect the sytle of text input today.

In this paper, we propose a procedure for sampling representatvie phrase from any large corpus so that text input researchers can curate their own stimuli for tasks, domains and languages they wish to target using publicly accessible resourecs.

Three contributions
- explain the mathematical concept for relative entropy
- propose an information-theoretic procedure
- describe the characteristics of pharse sets we generated

### ENTROPY AND REPRESENTATIVENESS
#### relative entropy
$$
D(p||q) = \sum_{x \in X} p(x)log_{2}{p(x) \over q(x)}
$$
$$$p(x), q(x)$$$ are probability distributions of random variable X over the same set of English characters x.
For comparing probability distributions, relative entropy constitutes a more mathemtically principled method.

### SAMPLING PROCEDURE
Finally, like MacKenzie and Soukoreff, we sought to procure phrases of "moderate length" - about 4 words, though this can be easliy adjuseted as well. While we did not attempt to select phrases that were "easy to remember", which was manually done in [9], as a future direction, we could explore using entropy for selection as well, especially in light of prior research demonstrating a correlation between entropy for selection as well, especially in light of prior research demonstrating a correlation between entropy rate and reading comprehension.

The procedure operates as follows:
1. Obtain a large corpus of interest. Many corpora can nowadays be obtained online for a wide variety of tasks, domains and languages.
2. Clean the text to remove any undesired portions of text.
3. Collect all word 4-grams from the text, keeping around duplicates as seperate entries. To adjust the phrase length, change the n-gram order n to the desired number of words.
4. Randomly generate an index number between 1 and the total number of 4-gram entries.
5. Find the 4-gram at the generated index and store this as a phrase for sample phrase set Si.
6. Repeat steps 4-5 until M sample phrase sets of the desired size are obtained.
7. Using the source corpus C, for each sample phrase set Si, compute the relative entropy $$$D(Si||C)$$$ of the character bigram distributions.
8. Select the sample phrase set S* with the lowest relative entropy
