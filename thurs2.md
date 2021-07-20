#Thursday 2 Responses: 
1. Present your results and discuss the accuracy of each of model.
    - Running both models revealed that it had more success with the beans dataset than the eurosat datasets based on the validation accuracy and validation loss. The eurosat model had a higher training accuracy than validation accuracy, which tells me it's possibly an overfit model. The beans model was more accurate on the validation data than the train data, which tells me it is probably underfit
    
```
beans
loss: 0.6471
accuracy: 0.6989
val_loss: 0.6043
val_accuracy: 0.7500

eurosat
loss: 0.7583
accuracy: 0.7256
val_loss: 0.8729
val_accuracy: 0.6770
```

2. Did your model performance improve? How many epochs were you able to run and how much time did it take?
   - The beans model drastically lost accuracy when the data augmentation was applied, with both accuracy and validation accuracy fell. The model remained underfit.
   - The eurosat model saw an increase in validation accuracy. The train accuracy fell, but the increase in validation accuracy tells me the model overall became better because the model's ability to make accurate predictions with new data improved.
   - Running the models with 7 epochs added around 5/10 minutes to the runtime, but yeilded much better results. Accuracies went up, and loss went down. I suspect that there is still room to improve the model by running more epochs.

This is a spread of images to illustrate how the random contrast and flip data augmentation layers are altering the images

![img_1.png](img_1.png)

```
beans with augmentation at 3 epochs
loss: 1.0268
accuracy: 0.4680
val_loss: 0.8547
val_accuracy: 0.5769

eurosat with augmentation at 3 epochs
loss: 1.0141
accuracy: 0.6378
val_loss: 0.7895
val_accuracy: 0.7067
```

```
beans with augmentation at 7 epochs
loss: 0.7673
accuracy: 0.6687
val_loss: 0.7537
val_accuracy: 0.6827

eurosat with augmentation at 7 epochs
loss: 0.7588
accuracy: 0.7287
val_loss: 0.6312
val_accuracy: 0.7781
```