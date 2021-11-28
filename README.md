# Logistic-Regression-from-scratch
*****STEPS TO RUN THE CODE*********
All of the required code blocks are included in the notebook and are generally sorted in a way to be run 
sequentially. This readme explains the flow of the code in the notebook:

1.Mount google drive
2.Import necessary libraries
3.Run both Class Definitions: Log_class and k_fold

A.Bankrupcy Dataset

	A.1 Running Logistic regression on the entire dataset:
	1.import data and split into xtrain,ytrain,xtest,ytest
	2.OPTIONAL: Add polynomial features(square,cube etc. of features)
	3.OPTIONAL: Scale the data using Z score scaling . This is Required to run if adding polynomial features in step 2.
	4.Instance the model using model=Log_Class(xtrain,xtest,ytrain,ytest,alpha) where alpha=learning rate
	5.run the fit method : model.fit(err_threshold) where err_threshold is the error threshold. Also note runtime
	6.run the model.predict(threshold=0.5) where threshold is the probability threshold
	7.run model.accu_eval() to print out the metrics

	A.2 Running K-fold cross validation:
	1.import data and split into xtrain,ytrain,xtest,ytest
	2.OPTIONAL: Add polynomial features(square,cube etc. of features)
	3.Run the k fold code block. Its located after the code for running model.accu_eval() in step 7 of A.1.it has the following parameters:
		features,target:your data  
		k : value of k(=10 for 10 fold cross validation), 
		alpha : learning rate  
		err_threshold: error threshold, 
		prob_threshold=0.5 :probability threshold,
		scaler=None : input an instance of a scikit learn scaling function like MinMaxScaler() or StandardScaler().

B.Hepatitis Dataset

	B.1 Running Logistic regression on the entire dataset:
	1.import data and split into xtrain,ytrain,xtest,ytest
	2.OPTIONAL: Add polynomial features(square,cube etc. of features)
	3.OPTIONAL: Scale either only continuous features of original dataset or scale complete dataset. scale complete dataset if adding polynomial features
	4.Instance the model using model=Log_Class(xtrain,xtest,ytrain,ytest,alpha) where alpha=learning rate
	5.run the fit method : model.fit(err_threshold) where err_threshold is the error threshold. Also note runtime
	6.run the model.predict(threshold=0.5) where threshold is the probability threshold
	7.run model.accu_eval() to print out the metrics

	A.2 Running K-fold cross validation:
	1.import data and split into xtrain,ytrain,xtest,ytest
	2.OPTIONAL: Add polynomial features(square,cube etc. of features)
	3.Run the k fold code block. Its located after the code for running model.accu_eval() in step 7 of B.1.it has the following parameters:
		features,target:your data  
		k : value of k(=10 for 10 fold cross validation), 
		alpha : learning rate  
		err_threshold: error threshold, 
		prob_threshold=0.5 :probability threshold,
		scaler=None : input an instance of a scikit learn scaling function like MinMaxScaler() or StandardScaler().



