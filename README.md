# Neural Network Challenge 1
## Project Description

<p>A company that specializes in student loan refinancing wants to predict whether a borrower will repay their loan. With this information the company will determine if it can provide a more accurate interest rate for the borrower. A model was created to predict student loan repayment.</p>

<p>The team was provided a CSV file that contains information about previous student loan recipients including their credit ranking. With use of machine learning and neural networks, the features in the provided dataset were used to create a model that predicts the likelihood that an applicant will repay their student loans.</p>

## Prepare the data to be used on a neural network model

   - Step 1 - The provided CSV file was read in and reviewed, specifically reviewing the "credit_ranking" feature
   - Step 2 - From the preprocessing data, a features (X) and target (y) datasets.  "Credit_ranking" will be used as the target (y).
   - Step 3 - The features and target are split into training and testing datasets
   - Step 4 - The features dataset was then scaled using scikit-learn's StandardScaler method

## Compile and Evaluate a Model Using a Neural Network
   - Step 1: Create a deep neural network by assigning the number of input features, the number of layers, and the number of neurons on each layer using Tensorflow’s Keras.
      - First "input_nodes" was defined based on the number of columns in the features (X) dataset.
      - Then to simplify coding hidden nodes and neurons output were defined to be used in the Sequential model
      - The Sequential model was defined with two hidden layers and an output layer
   - Step 2 - The model was compiled and fit 
      - The model was compiled using the `binary_crossentropy` loss function, the `adam` optimizer, and the `accuracy` evaluation
      - The model was then fit with the X_train data with 50 epochs
   - Step 3 - Model evaluation
      - The model was evaluated using the test data and reviewing model loss and accuracy
   - Step 4 - The model was saved and exported

## Predict Loan Repayment Success by Using your Neural Network Model
   - Step 1 - The saved model was reloaded
   - Step 2 - Predictions were made using the testing data
   - Step 3 - The predictions were saved into a DataFrame
   - Step 4 - The classification report was displayed

## Discuss creating a recommendation system for student loans


1. Describe the data that you would need to collect to build a recommendation system to recommend student loan options for students. Explain why this data would be relevant and appropriate.
   - To build a recommendation system to recommend student loan options for students, I would start with gathering information about the student and school and convert into usable features for a model:
      - Major studying
      - GPA
      - STEM degree score
      - Location of school
      - Financial aid information
      - Year of study - how long to complete degree
   - I would also seek parameters about the student's previous credit such as:
      - Payment history on other loans
      - Finance workshop score


2. Based on the data you chose to use in this recommendation system, would your model be using collaborative filtering, content-based filtering, or context-based filtering? Justify why the data you selected would be suitable for your choice of filtering method.
<p>The model would be using a collaborative filtering method as the model would provide student loan choices because similar users chose that option before and were successful.</p>

3. Describe two real-world challenges that you would take into consideration while building a recommendation system for student loans. Explain why these challenges would be of concern for a student loan recommendation system.
<p>In building a student loan recommendation model, I would have to take into consideration that some information might not be available such as payment history, GPA, and STEM degree score.  A student might not have previous loan experience and payment history.  Freshman students would not yet have a GPA and not a lot of courses taken in their major of study.  Additionally, students can easily change majors which may have implications to the recommendations.</p>

