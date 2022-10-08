# tenserflow

## Food CLassification & Sport Identification:

* models use Functional API
* Fine tuned top layers for better fitting
* food classification uses EfficientNEtB0 with top 5 layers trainable
* Sport identification uses EfficientNetB3 with top 8 layers trainable

## NLP - Sentiment Analysis

* Objective: Model should classify a sentence into one of 6 'sentiments': 'sadness', 'joy', 'fear', 'anger', 'love', 'surprise'
* 6 models using Naive Bayes, Deep Learning, and pre trained models ( `Bert` and `Universal Sentence Encoder`) to analyze emotion in sentences from a kaggle dataset. 
* Used `Conv1D`, and  `RNN`s like `GRU`, `LSTM` and `Bi-RNN` 
* Plotted accuracy-loss curves to find out overfitting and added Dropout layer for overfit prevention
* Evaluate the best model using a confusion matrix to find out where majority of the errors are.
* Used mixed-precision training for accelerating analysis
