# Columbia-Summer-Immersion-Program
In the summer of 2022, I got the chance to attend the Summer Immersion Program at Columbia University in the city of New York. We were assigned into groups of five for our capstone project. We were provided with a sample dataset containing information about loan applicants in a bank. My group decided that we would try and predict the ‘grade’ of an applicant given the other information about them (like the interest rates of their old loans, the CLI, number of times defaulted by the person, any criminal cases, the debt to income ratio among many others).

As with any ML project, we started with the data cleaning and formatting followed by Exploratory Data Analysis (EDA). Since there were seven distinct grades in the dataset, we used Multi-class Classification Algorithms. We explored several different models:

We got very good results with Random Forest Classifier 
(accuracy: 96.6% and high f1 scores for each of the grades as well). We also tried exploring Hyper Parameter Tuning though it was out of the course’s syllabus. We used RandomizedSearchCV and GridSearchCV. It is still work in progress!

Next we tried the Decision Tree Classifier (accuracy: 75%). Hyper Parameter Tuning worked really well here. When we changed the max_depth from 2 to 3, the accuracy shot up from 75% to 99.6%. 

We got a very low accuracy for K-Nearest Neighbors Classifier: 43.3%. Even when we found out the best set of Hyper Parameters for it (using GridSearchCV) the accuracy increased by a meager 1%. It would perform better if we just flipped its every decision! 

Naive Bayes Classifier gave us an accuracy of 87%. 
Gradient Boosting worked very fine for us: 96.7% accuracy while training and 95.3% while testing. Again we tried tweaking some of the hyper parameters: changed the max_depth and got a 100% accuracy for training and 98.7% while testing. 

Though it was a group project, I tried to explore more about Deep Learning and Artificial Neural Networks by myself (with a little help from my Course Facilitator). I used Keras and Tensorflow libraries. I made my best attempt at architecturing the Layers. I realized I had to keep the While compiling the model, I used “categorical_crossentropy” for the loss function and ‘adam’ as the optimizer. Next I converted all the ‘Y’ values to a binary class matrix. Alas, I got a very low accuracy of 38.33%. On the positive side, I got to learn a ton of new things!

