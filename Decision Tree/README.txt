Decision Tree Classifier

* This folder contains the Implementation of the Decision Tree Classifier from scratch.
* This was build using the numpy arrays in python.

* To Implement the Classifier several helper functions are written in python.
* Description of the helper functions

1.Train Test Split

Description:
		* This function takes input a 2d array and split ratio.
		* The function returns two 2d arrays the train and test 2d array.
		* Using the random module in python we split the 2d array.

2.check purity

Description:
		* This function takes a 2d array as input.
		* checking purity means if in the 2d array all the outcomes variables are same then the we don't need to classify.
		* we can stop the splitting of the data their because all the outcomes are same. And return the 2d array.
		* This function returns a boolean value if the function is pure or not.

3.classify

Description:
		* This function takes a 2d array as input.
		* returns the most dominant classifier outcomes variable.
		* Then the result for the maximum  tuple will be same in the test data also (assumption).

4.potential splits

Description:
		* This function takes a 2d array as input.
		* Returns a dictionary with column name as key and the value is a list of unique values in the column to calculate the entropy.
		* why unique values? .Their is no use to calculate the entropy for the same element twice.

5.split data

Description:
		* This function takes a 2d array ,split column,split value.
		* And splits into two dataset the value below and value above for the numerical values.
		* If for categorical values is it equal to the value or not.
		* Returns two 2d array.

6.calculate entropy

Description:
		* This function takes a 2d array as input.
		* calculate entropy and returns the value.

7.calculate overall entropy

Description:
		* This function takes two 2d array as input.
		* And calculate the overall entropy known as the information gain.
		* returns the value.

8.Best split

Description:
		* This function takes the 2d array and potential splits dictionary as input.
		* Determine which split is the best according to the highest Information gain.
		* Returns the best split column and the split value in it.

9.Determine the type of feature

Description:
		* This function takes the column names as input.
		* Returns the array of value which has values as categorical and numerical.
		* If the values in the column are less than 10 unique value numbers or string values consider as the categorical.
		* If the values are numerical and unique values in them are more than 15 consider as the numerical.

10.Decision Tree algorithm

Description:
		* This function takes a dataframe as input.
		* Returns a dictionary.
		* The dictionary is in the tree structure.Key is a question and if it is true go to left tree else go to right tree.
                                              
                                                Tree diagram

						------------
					        | question  |
						-------------
                                              /		      \
                                         yes /		       \  no
                                            /			    \	
                                     -----------           -------------
                                    | left tree |         | right tree |
                                     -----------           -------------


* dictionary form

   {"question" : [ yes_answer , no_answer ]}
   * yes_answer may be a subtree of same structure or leaf node direct output variable.
   * no_answer may be a subtree of same structure or leaf node direct output variable.

11.classify example

Description:
		* This function is used to predicted value of new input.
		* This function takes each row as input and the result dictionary returned by decision tree algorithm to predict the output.
		* Returns the predicted value found using the dictionary build by the decision tree algorithm.

12.calculate accuracy

Description:
		* This takes the dataframe as input and compare with the predicted outcomes.
		* Returns the accuracy of the model

13.bulid tree

Description:
		* This function takes the dictionary returned from the decision tree algorithm and build the tree flowchart diagram
		* This uses dot languague using the graphviz module.


This Classifier is used to build the Decision tree and the predict the accuracy of the model.                              