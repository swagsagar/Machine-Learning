

**Author:** Sagar Bhandari  
**Date:** October 09,2025  


For this project i tested two models kNN and Decision Tree Regressor on the wine quality dataset.
Both are supervised learning models. I used a dataset that tracks things like acidity, pH, and sulfur levels to see which algorithm could get the closest to the actual quality rating.

kNN Model:
The kNN model was interesting because it's all about "proximity" , it looks at the wines most similar to the one we are trying to predict.

Weighted vs. Unweighted: I tried two versions. One where every "neighbor" has the same vote (Uniform) and one where closer neighbors have more influence (Distance-based). The weighted version worked way better.

The Importance of Normalization: Since features like "Total Sulfur Dioxide" have much bigger numbers than "pH," the distance math gets weird. I used Z-score normalization to make sure every feature had a fair say in the prediction.



Decision Tree Regressor:
Next, I tried a Decision Tree, which basically asks a series of "Yes/No" questions to categorize the data.

Splitting: The tree tries to group the data so that the wines in each "leaf" are as similar as possible.

Tree Depth: I noticed that if I let the tree grow as much as it wanted, it "memorized" the training data but failed on the test data. I found that limiting the max_depth to about 5 to 8 gave me the best results on new data.