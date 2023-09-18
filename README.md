# Predicting Facial Expression/Emotion from Images
_________

## Problem Statement

The goal of my project is to build 1-3 Convolutional Neural Network (CNN) models that can take in images of individuals with different facial expressions and classify them into the correct emotion classes with a 70% accuracy on both the training and testing set. The emotion classes that were identified in the source data were: Angry, Fear, Happy, Sad, Surprised, and Neutral. 

The purpose of investigating this topic is to see how well a model can interpret facial expressions as simply as possible, with as little resources as possible. If a model can predict facial expressions with an accuracy of 70% on both the training and testing set without needing to purchase extra resources from services like Google Colab, it may elude to the possibility of smaller companies and individuals being able to implement these models for their own uses and products, without needing the resources of large tech companies. 

Additionally, if these models can easily and relatively accurately predict facial expression from images, it may improve certain technologies such as VR, AR, facial recognition technologies, etc., as well as aid in studies in psychology and related fields.
__________________

## Evaluation, Conclusions, Recommendations, and Future Steps

### Evaluation:

In consideration of my measure of success being the creation of a model that scored 70% accuracy on both the training and testing set, I did not meet the success criteria in either of my models. My first model, a "basic" CNN ran for 5 epochs, having no early stopping clause or data augmentation, concluded with a training accuracy of 0.61 and testing accuracy of 0.51. On a positive note, both the training and testing accuracy scores improved from epoch 1(training: 0.33; testing: 0.42) to epoch 5(training: 0.61; testing: 0.51), although the model became increasingly overfit as the epochs increased. 

My second model, a CNN ran for 10 epochs, with early stopping (no data augmentation), showed that adding in more epochs to the model improved the training accuracy(~0.70 after 7 epochs, vs ~0.61 after 5 epochs in my previous model), although the testing accuracy began to stagnate around 0.5. Additionally, the model becomes increasingly overfit as it moved higher in the number of epochs. It ended up stopping at epoch 7 due to the early stopping clause specifying to stop running the model if the validation loss increased for three epochs straight(which it did, from epoch 5 to 7). 

### Conclusion and Recommendations:

After evaluating my models, I do not think that one can conclude with certainty that an individual or small company with relatively little resources cannot build a model that can take in images of individuals with different facial expressions and classify them into the correct emotion classes with a 70% accuracy on both the training and testing set. I attempted to build a CNN model that ran for 10 epochs with early stopping and included significant data augmentation to combat overfitting/high variance, although I continued to reproduce a "FileNotFoundError" in the model even after many attempts to resolve the issue. I predict that if one is able to produce the aforementioned model and have it run for 10 epochs (due to the data augmentation helping reduce variance, and therefore delay the early stopping), the model could produce 70%+ accuracy scores on both the training and testing set. 

I recommend that when attempting to build a CNN model that can take in images of individuals with different facial expressions and classify them into the correct emotion classes with a 70% accuracy on both the training and testing set, one should include significant data augmentation to combat overfitting/high variance. I believe that if an individual or small company with relatively little resources does the above, they can indeed build a model that satisfies their goals, using free resources like google colab, and not need to purchase additional resources. 

### Future Steps:

A future step I plan to take in the project is to install TensorFlow/Keras onto my local machine so I can try to run the CNN model with 10 epochs, early stopping, and significant data augmentation using a different resource, such as VS Code or Jupyter Lab. I believe that hosting the data for this project on Google Drive may have been the source of the "FileNotFoundError" that I continued to produce - running the models on VS Code or Jupyter Lab may prove to resolve that issue, making running my models a much smoother process.