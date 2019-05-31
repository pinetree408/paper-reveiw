# Review
## Purpose of Review
To apply the techniques used in this paper to predict korean word
## Class-Based n-gram models of Natural Language
### Language Models
#### Definition of Language Models
- given a signal y, we seek to determine the string of English words, w, which gave rise to it.
- we blithely assume that the production of English text can be characterized by a set of conditional probabilities, Pr(wk|w1^k-1), in terms of which the probability for a string of words, w1^k, can be expressed as a product:
- Pr(w1^k) = Pr(w1)Pr(w2|w1) …Pr(wk|w1^k-1)
- Here, w1^k-1 represents the string w1w2…wk-1. In the conditional probability Pr(wk|w1^k-1), we call w1^k-1 the history and wk the prediction. We refer to a computational mechanism for obtaining these conditional probabilities as a language model.
##### Evaluation
- The perplextity of a language model with respect to a sample of text, S, is the reciprocal of the geometric average of the probabilities of the predictions in S. If S has |S| words, then the perplexity is Pr(S)^-1/|S|.
- Thus, the language model with the smaller perplexity will be the one that assigns the larger probability to S. Because the perplexity depends not only on the language model but also on text with respect to which it is measured, ti is important that the text be representative of that for which the linage model is intended. Because perplexity is subject to sampling error, making fine distinctions between language models may require that the perplexity be measured with respect to a large sample.
##### ETC
- We estimate the parameters of an n-gram model by examining a sample of text, t1^T, which we call the traning text, in a process called training. 
- We say that an n-gram language model is consistent if, for each string w1^n-1, the probability that the model assigns to w1^n-1 is S(w1^n-1). 
- We can illustrate the problems attendant to parameter estimation for a 3-gram language model with the data in Table 1.
- As n increases, the accuracy of an n-gram model increaes, but the reliability of our parameter estimates, drawn as they must be from a limited training text, decrease.
##### Interpolated estimation
Jelinek and Mercer describe a techinque called interpolated estimated that combines the estimates of several language models so as to use the estimates of the more accurate models where they are reliable and where they are unreliable, to fall back on the more reliable estimates for less accurate modes.