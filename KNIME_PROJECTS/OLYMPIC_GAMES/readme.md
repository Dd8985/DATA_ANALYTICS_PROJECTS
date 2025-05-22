📊 KNIME analysis on Olympic Games

It is a comprehensive dataset of the Olympic Games, spanning from the 1896 Athens Olympics to the 2016 Rio Olympics and having records of the games. Each instance corresponds to an individual athlete competing in an individual Olympic event (athlete events).

🎯 The aim of project

This project aims to analyze (EDA and visualization) the distribution of athletes and medals by region and gender by analyzing Olympic Games data. And then , Predicting whether an athlete will win a medal based on athlete characteristics.

🧰 The methods and tools used

EDA : Data cleaning (missing data, data type conversions, duplicate data) Cleaning and analysis on categorical and numeric columns Removing some columns and replacing them with new names Identifying outliers by looking at numerical statistics Two different data sets were joined and merged based on their common columns(Joiner node) Group-based summarization and filtering Data visualization with simple charts (bar, heatmap, line chart, pie chart)

Model Preparation : 1)	Identify target column : Tagged as medal winners 1, non-medal winners 0.
                    2)	Feature selection : In order for the model to make predictions, we need to use some independent variables 
                        (characteristics) such as height, weight, age, gender, sport, country. “Considering the age, height, weight, 
                        gender and sport branch of this athlete, will he/she win a medal?” will be answered.
                    3)	String to Number (Encoding) : Machine learning algorithms work with numbers. So we need to make these columns 
                        numeric.
                    4)	Training and Test data : If we use all the data to train the model, then we cannot realistically test its 
                        performance. So we train the model with part of the data (training) and test it with the rest (testing)(%80 , %20).

Modelling : Which one predicted more accurately?
            Which model is more successful?
            Logistic Regression: First we need to do feature scaling, i.e. standardscaler. We scaled as the magnitude of the numerical 
                                 values can affect the learning of the model. The z-score method was used for normalization. 80% of the 
                                 data allocated for training was taught to the model and predictions were generated for the remaining 20%.
            Decision Tree : The decision tree model was built without normalization. 80% of the data allocated for training was taught to 
                            the model and predictions were generated for the remaining 20%.

Accuracy Score : Model performance for Logistic Regression : % 61.4
                 Model performance for Decision Tree : % 59.8



📁 Conclusion

The questions given below were answered and visualized.

Which country has sent the most athletes to the Summer Olympics?
Which countries won the most medals?
How successful are countries in winning medals according to the number of athletes they send?
How has the number of participants changed over the years?
How has the difference between the number of women and men participants changed over the years?
How many medals were won in which sport and at which level?

Logistic Regression is better in measures such as overall accuracy (61.4%) and Precision (59.8%), making it a more stable model than Decision Tree (59.8%).
