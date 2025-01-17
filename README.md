Module 21 Challenge -

Overview/Background: A company Alphabet Soup wants a machine learning neural network application that will predict whether applicants will be successful if funded by Alphabet Soup.

The CSV contains 34,000 organizations that have received funding from Alphabet Soup over the years.

1. Preprocessing the Data:
-StandardScaler() : scales the data 
-get_dummies() : encode categorical variables
-train_test_split : create feature and target arrays, splitting data into training and testing datasets
-transform : fitting the scaled training data

-target: "IS_SUCCESSFUL" : whether a company was successful or not.
-features: "Family/Parent","CompanySponsored","Independent", "Association", "Co-operative", "Trust", "Heathcare", "Preservation", "ProductDev","C1000","C1200","C2000","C2100","C3000" : variables that could determine likelihood of success.
-non-features: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE','ORGANIZATION', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS' these variables were removed because they are not interpretable by machine learning.

2. Create the TensorFlow Model 
-tf.keras.models.Sequential() : created the model
-tf.keras.layers.Dense() : creating the neural network layers
-nn_model.summary(): the structure of the model

3. Optimizing the model(Compiling, Training, and Evaluating the Model)
- chose 3 layers, each with 4 neurons, and each using the "relu" activation function(testing a few combinations, this provided the highest accuracy)
- achieved accuracy of 0.69
- tested different sized layers and neurons(2-6 layers, 2-8 neurons)

Summary: Given the features and the target variable, 0.69 accuracy is ultimately quite useful. A SVM model could be very useful in solving the classification problem. A SVM model could capture some of the complex distinctions between variable clusters.
