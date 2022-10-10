# tenserflow

## Image Classification - Food CLassification & Sport Identification:

* models use Functional API
* Fine tuned top layers for better fitting
* food classification uses EfficientNEtB0 with top 5 layers trainable
* Sport identification uses EfficientNetB3 with top 8 layers trainable

## NLP 

### Sentiment Analysis

* Objective: Model should classify a sentence into one of 6 'sentiments': 'sadness', 'joy', 'fear', 'anger', 'love', 'surprise'
* 6 models using Naive Bayes, Deep Learning, and pre trained models ( `Bert` and `Universal Sentence Encoder`) to analyze emotion in sentences from a kaggle dataset. 
* Used `Conv1D`, and  `RNN`s like `GRU`, `LSTM` and `Bi-RNN` 
* Plotted accuracy-loss curves to find out overfitting and added Dropout layer for overfit prevention
* Evaluate the best model using a confusion matrix to find out where majority of the errors are.
* Used mixed-precision training for accelerating analysis

### PubMed RCT

* Objective:  build an NLP model to make reading medical abstracts easier. It basically takes a large block of text, like a research paper from https://pubmed.ncbi.nlm.nih.gov/ and makes the text easier to read by splitting the text into managable chuncks- Backgrounds, Methods, Results, and Conclusions. Therefore, it is essentially a multiclass classfication model.
* The final model should take in `Total Sentences`, `Sentence Number` (order of the sentence in the text), and the `Text` to output the classes.
* Started with baseline model `Model_0` using SKLearn Naive Bayes's `ComplementNB`, which reached 73% score.
* Built 7 models, each with their own versions, to find out which works best. These models concentrated on different ascpects of the input, for example a model would take in only `Total Sentences` and `Sentence Number` to predict the classes. Another model would only take in character and text embeddings to predict the classes.
* Used `Concatonate` layer to build final model `Model_7`, utilizing the best performing models from the above step, resulting in `Model_7` reaching 86% accuracy on 10% of the dataset and trained on 10% of each batch.
* Layers used in various models: `Embedding` using universal-sentence-encoder from tf_hub, `Conv1D`, `GlobalMaxPool1D`, `Dense`, and `Bi-LSTMs`.
* Utilized `tf.data` API, enabling faster data loading.
