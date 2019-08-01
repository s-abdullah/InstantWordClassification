# InstantWordClassification

This Project aims to do Custom word classification based on User input and minimal tagged data.

# Usage

The user inputs a sentence tagging specific word group that they need to be classified. Right now the application supports two different word groups that are distinguished by the markers "!" and " * ".

An Example Input is:
`I used to drive around with my !dogs in my *Ferrari. But then I got a !cat and bought a *Porsche for her.`

After training on this the classifier would be able to work on this test input:

`I crashed my **Mustang** but my <em>parrot</em> and snake were not in the car`


# Archecture

The application leverages the dictionary in NLTK and both Word2Vec and GloVe vector embeddings to train a perceptron. 
Speciifucally the first two are used get expand the training data using similarity metrics and synonyms. while the GloVe embeddings are used in the actuall training. Using two differnet emebeddings is what makes the classifier robust.