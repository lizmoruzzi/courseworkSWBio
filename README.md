
# Predicting breast cancer malignancy
The breast_cancer notebook contains a pipeline which can predict if a tumour is malignant or benign based on 30 different measured properties of a tumour, including cell perimeter, smoothness and area. This pipeline uses a k nearest neighbors model (knn) to classify if a tumour cell is malignant or benign, based on two paired properties. However, to find the best model, two different knn models were generated using two sets of paired properties (x variables): 'mean perimeter' vs 'worst smoothness' and 'mean area' vs 'worst smoothness'. These models were refined using GridSearchCV to find the optimal hyperparameters. Once generated, the final models can be compared, to find the most appropriate one to be used in breast cancer diagnosis. This model was trained using the scikit learn toy Breast cancer wisconsin (diagnostic) dataset.


To run:

1. Download the breast_cancer python notebook in this repository into a single directory.

2. The pipeline includes the code to import the data from sklearn directly, so there is no need to download the dataset. However, to find more information about the dataset see: https://scikit-learn.org/stable/datasets/toy_dataset.html#breast-cancer-dataset

3. Run the cells in the code under Section 1: Exploring the dataset. At the end this generates a scatterplot to visualise the separation between the two classes of tumour for each paired property. This scatterplot was used in the intitial development of the model to choose which paired x variables generate the greatest separation of the classes of tumour.

4. Run the cells under Section 2a: This will generate a knn model which will colour the graph accordingly to predict if a tumour would likely be benign or malignant. After the first model is generated, run the cells in Section 2b to refine the knn model using GridSearchCV to find the best hyperparameters, this will be visulaised in both an ordered table and a graph. This will then generate a new knn model with the improved hyperparameters. In the default code, 'mean perimeter' vs 'worst smoothness' are paired together to generate the first model, as they had good separation. **Please note the user can change which paired properties (x variables) to generate a model from.** For example, you could swap 'mean perimeter' for 'mean radius', and pair it with 'mean concavity'. Additionally, make sure to redfine 'X' in the code when generating the intial model.

5. Run the cells under Section 3a: Generating a 'mean area' vs 'worst smoothness' knn model. This also generates a second model to predict if a tumour would likely be benign or malignant based on a coloured area of the graph. Finally, after the first model is generated in this section, Section 3b will refine the knn model using GridSearchCV. This will then generate the final model with improved hyperparameters. **Again, please note the user can change the paired x variables, like in Section 2.**

Finally, the final models can be evaluated by comparing the model scores following the refinement of each model. The highest model score would be classified as the best model, however, it is worth considering the model plot itself when comparing the models to see if it is an appropriate model. The best scoring model could be chosen to be used in breast cancer diagnosis.



