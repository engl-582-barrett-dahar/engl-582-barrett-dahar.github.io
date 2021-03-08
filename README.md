# Semantic Drift Velocity
### Change in meaning over time
Wesley Dahar and Isaac Barrett

## Abstract
### Introduction
This project will explore word embeddings to compare American and British societies from 1600 to the present. Specifically, we will use gensim to train a Word2Vec model on corpus data from different time periods, and then analyze these modes for shifts in word associations between ideologies of the times and the values placed on concepts discussed in literature. We also seek to discover which words have retained their senses and convey social bias across the centuries. In addition, we will aim to classify works of literature by the worldviews they express.

- __RQ1:__ Based on determining the k-most-similar words, how do word embedding models trained on data from different time periods capture worldview associations for a fixed set of examined vocabulary?
- __RQ2:__ How does the timespan used for training models impact the measured similarity of associations for a consistent set of words?
(Stretch goal: How well can embeddings be used to classify either time periods or authors?)
 
### Motivation
Looking back on the records of human history and culture, there are lessons to be learned and traditions to shape our identities. After so many years of advancements in both technology and science and of accumulation of diverse philosophical foundations for societies, we must critique the ideas and values of the past and present. We are fortunate to live in an age where ideas wage war across the barriers of time and space with the clarity of purpose and the power to effect change like no other time before us. As we now look with uncertainty to our future through the varying lenses of the past, moral agents can be explored through the lens of their text produced.
 
### Method
We will collect publically available works of literature in the Gutenberg Archive representative of their time periods and make sure that there is no disparity of diversity in our selections. Diverse ideologies are not so much the point of focus as are the use of the English language as the medium through which ideas are communicated.
 
### Experimental Design
Our experiment will consist of training models with their respective corpora and then measuring the relative cosine distance of embeddings for an identified set of words given different embedding models and recording the similarities and differences in word associations (e.g. their average, median, standard deviation, etc). We will look for instances in which certain categories of words exhibit bias toward factors such as gender and race.
The dependent variable is the cosine measure, while the independent variables are
- __t__: The time span used for training the model. This factor will have one of four values: 10, 25, 50, or 100 years.
- __n__:  The number of words considered for exploring proximal neighbors in embedding space. Our analysis will consider 5-10 word embeddings each for different word categories reflecting gender, race, and philosophical/political movements.
All models will be trained on corpora consisting of the same number of words and same number of authors to control for artifacts associated with the size of the training data. We will sample text from the beginning of the text to the max length of words, and discard subsequent text. Any header/footer from Gutenberg will be discarded prior to training the models. 

 


## Interim Documents
[Interim Presentation 1](./docs/semanticDriftIntro.pdf)

## References
https://nlp.stanford.edu/pubs/hamilton2016cultural.pdf
http://arxiv.org/pdf/1301.3781.pdf
http://www.eecs.harvard.edu/~htk/publication/2017-cikm-cha-gwon-kung.pdf
