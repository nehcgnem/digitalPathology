## a classfier for digital pathology images.
#### Link to dataset
https://www.kaggle.com/c/digitalpathology/overview
#### Sample pathology image
![alt text](https://github.com/nehcgnem/digitalPathology/blob/master/sample.png)

#### Method
1. Using Local Binary Pattern to extract features from the training images. 

2. Train SVC model from the sklearn library to determine the decision boundary, with C parameter to determine how wide the margin is (penalty), too wide gives under-fitting, too narrow results over-fitting.

 3. Using 10-fold cross-validation. In each fold, a model was trained with 90% of the training data and evaluated with loss and accuracy score based on the rest 10% of the training data. 10 very similar model was created after K-fold validation, and each gives one prediction on the testing data. 

4. Ensemble 10 predictions together by majority vote (averaging the probabilities), and took the most likely result as the final prediction.

#### Result 
Achieved 93% test accuracy.
