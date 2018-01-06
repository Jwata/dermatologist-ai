# Report 2018/01/06
* Augumanted data (2,000 -> 10,000 images)
  * Vertical flip
  * horizontal flip
  * Random rotation x 2
* Customized the architecture learned in [the transfer learning lession](https://github.com/udacity/deep-learning/tree/master/transfer-learning)
  * VGG19 + pretrained weights
  * Botttle neck from the relu6 layer of the VGG19
  * 2 fully connected layers on top of the bottle neck
  * dropout layers to avoid overfitting

## Output

```
Category 1 Score: 0.744
Category 2 Score: 0.806
Category 3 Score: 0.775
```


![](./roc_curve.png)
![](./confusion_matrix.png)

## Next

* Augument only `melanoma` and `seborrheic_keratosis` to mitigate the data unbalance
* Shuffle training data
  * the order of training data matters?
* Train with more data. (the ISIC archive data)
* More data augumentation variation
  * e.g. Random Erasing
