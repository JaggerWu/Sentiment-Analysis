# FastSent
###### A project for Language Processing 2 - Group 3

---

#### Credits

- [fastText](https://github.com/facebookresearch/fastText) by facebook
- the [keras tutorial](https://github.com/fchollet/keras/blob/master/examples/imdb_fasttext.py) on the subject

#### Example output of current model


*A cinematic achievement of amazing depth. Marvellous acting, captivating score,
a journey in a time when directors produced masterpieces. one of a kind, my favorite film,
I LOVE IT!*

gives 0.75

*I went with my girlfriend to the cinema. She's into american comedies and I
really like her, so I just saw the worst most terrible movie in my life.
boring, untalented acting, dull and uninspired cast, absolutely terrible score.
the worst movie ever.*

gives 0.14

*with Robert De Niro and Al Pacino*

gives 0.45

*with Adam Sandler and Jennifer Aniston*

gives  0.38



#### Architecture

- Assign a unique integer to the 20000 most common words and bigrams
- Take the dot product of the one-hot representation to create a N dimensions embedding
- Drop a dense layer
- Put a softmax on top to get the so-called rating

#### Training

We trained first for an epoch on some IMDB [data](http://ai.stanford.edu/~amaas/data/sentiment/)
and then for two epochs on our dataset.


#### Comments

The nature and number of the data lead to overfitting on many occasions,
so our model's accuracy cannot estimated without too much variance. We expect,
however, to score better than chance.
