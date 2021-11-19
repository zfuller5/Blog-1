# Truth About Cats and Dogs
-By Zach Fuller

### Description
---
The debate around Cats and Dogs can be one of the most polarizing topics in the pet world. If you dig a little deeper you'll find that this is not just as simple as choosing a family pet. On the contrary, researchers and academics have spent countless hours studying the psychological correlation between choosing a cat versus a dog and the human personality type. For this study, I will be heavily referencing the study performed by Samuel D. Gosling, PhD, department of psychology, University of Texas at Austin and featured on the following 

URL (https://pets.webmd.com/ss/slideshow-truth-about-cat-people-and-dog-people).


### Why is this important?
---
You can really think about this two ways. One, use my personality type to chose which animal best suites me. Two, use the pet personality type to chose which animal best suites me. With respect to the first method, we can use a model to input human personality traits and predict which animal will best suite that human. Conversely, the second method would allow us to input desired personality traits of a pet and predict whether it is a dog or a cat to help the human with selecting which pet.


### How do we do this?
---
We will be using two methods to help the human choose their pet. One method leads more to the second method where we examine the personality trait of the pet in light of it being a positive or a negative personality type or sentiment. The other method is using a traditional model to predict whether a personality type denotes a cat or a dog.

The First Method will utilize Sentiment Analysis and specifically the VADER sentiment analyzer to give the human a way to examine pet personality traits as being positive or negative. We can think of this as a way to come up with a traditional Pros and Cons list.

The Second Method will utilize traditional predictive models or estimators used on transformed data. The table below shows which models we will examine for predicting which animal the human should chose based on personality traits.

| Method | Type |
| --- | --- |
| **Multinomail Naive Bayes** | *An estimator that uses conditional probabilities assuming all features are independent of one another.* |
| **Logistic Regression** | *An estimator that uses a logit link to fit a classification regression or simply the probability of being in each class.* |
| **Random Forest** | *An estimator that uses a modified tree learning algorithm that selects a random subset of features at each split in the learning process.* |
| **Count Vectorizer** | *A transformer that simply counts every word and creates a feature for it* |
| **Term Frequency-Inverse Document Frequency Vectorizer** | *A transformer that tells us what words are important to one document relative to all other documents.* |


### What did we find?
---
Use the VADER method to examine pet personailites as Pros and Cons. On the Pros list, we found that 34.5% of dog documents had a positive rating greater than 75%, while only 29.2% of cat documents had a positive rating greater than 75%. For the Cons list, we found that 12.9% of dog documents had a negative rating less than -75%, while only 11.2% of cat documents had a negative rating less than -75%. The human should use this tool to add positive and negative sentiments to their Pros and Cons list.

Use the Multinomial Naive Bayes transformer with the Logistic Regression estimator as a model with greatest accuracy and least amount of misclassified documents. The MNB LogReg model has an 89.5% accuracy rating to correctly predict which type of animal you should bring home as your pet based on personality types. Take each personality type that is important to the human to select which pet is right for that person or family.


### Let's make a choice!
---
Use the Streamlit app to enter personality types and watch the model chose which pet is right for you.
