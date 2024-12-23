# neural-network-challenge-1

In this project I use a student loan data set and a neural network to predict students' credit rankings.\
The dataset can be found here: [https://static.bc-edx.com/ai/ail-v-1-0/m18/lms/datasets/student-loans.csv]\
The notebook file and the final model, the keras file, can be found in the M18 Starter Files folder.

### Preprocessing:
First the data is split into X and y, where y is the credit ranking. Then the train test split is\
performed on the data and the standard scaler is used for the X_train and X_test.

### Creating the Model:
To make the model the following steps were taken:
- The number of nodes for each layer are set
- The sequential model is created
- Two hidden layers and the output layer are added using the specified number of nodes
- The model is compiled
  
```
nn.compile(loss = 'binary_crossentropy', optimizer = 'adam', metrics = ['accuracy'])
```
- Lastly the model is fit to the train data with 50 epochs before being evaluated and/
exported as a keras file.

### Importing and Using the Model
After exporting the model, it is imported and used to make predictions using the X_test_scaled data.
