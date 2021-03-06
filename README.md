# summarizer

##Problem:
With the abundance of articles available on the internet, it is generally tedious to go through the entire article to find how relevant the article is for the user. With this, we want to implement an art of intrinsic extraction which highlights the most important sentences in a document. We want to specifically summarize articles related to a particular topic from Kannada newspapers.

Why is it interesting or challenging:
The primary reason for this project is the non-existence of working implementation of a summarizer for Kannada language and also a corpus to act as a baseline for summarization. 

Creation of corpus itself is a challenging task. Also, we want to use both supervised and unsupervised learning to improve the performance. Another reason that makes the task challenging is the requirement of a stemmer algorithm to find the root of a word. We are planning to implement a rule based stemmer algorithm1, the complexity of developing stemmer for Dravidian language like Kannada is comparatively higher than the other languages like English. Most of the words may change spelling when stems are inflected.

Existing work and Relevance to the proposed project:
The existing work involves the proposal and theoretical explanation of TF-IDF approaches. But there has neither been a corpus nor has there been a working implementation of such approaches. Also, there has been no showcase of good preprocessing techniques that aid in better summarization of the articles. But, our approach involves the creation of a corpus, implementing good preprocessing techniques  and also in implementing and evaluating multiple summarization techniques.

Method
Materials:

News articles (http://www.prajavani.net/ http://www.kannadaprabha.com/) and wikipedia. 

Also initially 400 articles will be read and summarized by all the four members with 15% articles in common. The annotation will later be used to reach a consensus on the inter-annotator agreement. Evaluation of the task is done using Rogue model or other approaches. This corpus will act as baseline for evaluation and iteratively we will add more documents.

##Procedure:
```
  1. Acquiring the Kannada articles.
  2. Building the corpus
    2.1 Collecting and preprocessing the articles.
    2.2 Distributing articles among ourselves and annotating.
    2.3 Analysing and reporting the inter-annotator agreement.
  3. Building a stemmer using a rule based stemmer algorithm1.
  4. Algorithms
    4.1 TF, IDF, GSS coefficients 5,6 and sentence scoring
      4.1.1 We use GSS coefficients and IDF methods along with TF for extracting keywords and later use these for summarization.
      4.1.2 TF and IDF are category independent, GSS coefficients which evaluate the importance of a particular term to a particular category are calculated.
    4.2 TextRank algorithm2  will also be evaluated.
  5. Using the model to summarize the preprocessed articles.
  6. Comparing and reporting the performance of the model against the established baseline
```

##Evaluation:
We will build summaries for the articles(around 400) targeted to a specific topic, use inter annotator agreement and evaluate the summaries generated by the algorithm against the manual summaries. F1 score will be used to assess the efficiency of the algorithm(sentences as features).

##References:
http://www.ijcaonline.org/volume27/number10/pxc3874583.pdf
https://web.eecs.umich.edu/~mihalcea/papers/mihalcea.emnlp04.pdf
http://nlp.cic.ipn.mx/Publications/2008/Text%20Summarization%20by%20Sentence%20Extraction%20Using.pdf
http://research.ijcaonline.org/volume75/number6/pxc3890449.pdf
http://airccj.org/CSCP/vol1/csit1311.pdf
http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6416635&tag=1
http://www.mirlabs.org/jnic/secured/Volume1-Issue1/Paper14/JNIC_Paper14.pdf
http://airccse.org/journal/ijsc/papers/2411ijsc08.pdf
https://www.youtube.com/watch?v=Vw-7XkP9H1o

