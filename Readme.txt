README: 
Topic: Midterm Project
Names: Ben Fraser and Riley Thomas
Student ID: 2390802 and 2398529
Sources: Chat GPT 3.5, Vanguard Pub Dataset: LotwiZe, CA Census Data, GreatSchools.org, and Feedback from Professor Frenzel. 
Errors: No known errors
        


Project Overview
Our project is designed to help LotwiZe find actionable insights in a dynamic real estate market by accurately predicting housing prices. Acting as Data Scientists, we developed two advanced valuation models using a combination of provided features and additional ones created through external data sources. This project aims to provide a high-quality property valuation model that gives LotwiZe a competitive edge in the real estate industry.
In this project, we used XGBoost and other advanced analytics models to create the most accurate models possible. The models utilized a variety of features, including property-specific attributes and broader market indicators. To make our analysis better, we used external data sources like census data to improve price prediction capabilities. Additionally, we employed AI sentiment analysis to further refine the price estimation process by classifying housing descriptions into price ranges before estimating final values.
Instructions for reproducing our analysis
1. Data Preparation:
   * Feature Engineering: Add the following additional features to reproduce the dataset. To recreate our dataset utilize census data and other reliable sources to ensure accuracy and appropriate geographic mappings. Alongside the vanguard data set provided, create the following variables and add them to your dataset:  Population, Distance to coast, Average Income City, the house, School Rating of the city, home type (Apartment, Condo etc). 
   * Binary Encoding: Convert categorical variables or boolean features, for example the True/False variables for hasHeating into binary form (0/1) to allow the models to interpret the data. Reference the dataset provided to find examples of creation of these variables.
   * Handling Missing Data: Drop any missing values (NA) to clean up the dataset and ensure completeness before modeling.
   * Dataset Split: Use a train/test split of 80/20 instead of K Fold because of the complexity of the dataset. K Fold took too long to run and wasn’t a viable option for us moving through this project with limited time. 
   * Regularization: Utilize different regularization techniques such as LASSO or RIDGE to ensure that only the most relevant variables are being applied to your model. 
2. Modeling:
   * XGBoost Model: Fit an XGBoost model using the cleaned dataset. XGBoost is ideal for handling large datasets with complex relationships between variables. Utilize the tuning parameters such as nrounds, max_depth, and eta to optimize the models performance. 
   * Random Forest Model: As a comparison, also fit a Random Forest model to the data. Optimize the parameters of number of trees and node size to create the most accurate results. Both models can be optimized by cross-validation and hyperparameter tuning.
3. Sentiment Analysis for Price Classification: We integrated sentiment AI integration analysis to enhance our models. Initially, we struggled to create a rubric for ChatGPT to classify home descriptions accurately into cheap, mid-price, and expensive categories. However, after simplifying the prompt engineering and including the city name in descriptions, the model's performance improved significantly. By classifying homes into price ranges before estimating their value, we enhanced the accuracy of our predictions. Inside the integration code be sure to provide the AI user and assistant roles to give the model examples of cheap descriptions, mid-level descriptions, and expensive descriptions. Utilize the most expensive GPT that you are comfortable paying for. 
4. Evaluation and Comparison:
   * Use metrics such as Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) and R Squared to measure prediction accuracy.
   * Compare the performance of the XGBoost and Random Forest models to determine the most effective approach for LotwiZe’s valuation tool.
5. Visualization & Reporting:
   * Visualize feature importance from the XGBoost and Random Forest models to highlight key variables driving price predictions.
   * Use visualization techniques such as bar plots, box and whisker plots and scatter plots to gain an understanding of your dataset and plot the results of your model.
   * For deeper understanding of your dataset utilize the Leaflet package in RStudio to display city prices on a map. Ensure that you have both longitude and latitude for each of your variables and the city. To do this bin the average home price in each city and use the leaflet packages to plot the cities onto the California map. Color each of the cities by the average price with the range you feel is right and color the differences. 
   * Generate a final report summarizing the methodology, results, and actionable insights.
After following these steps you will be able to recreate the project and analysis that we made to produce high quality actionable valuation models for LotWize. Utilizing complex XGBoost, Random Forest Regressions, advanced AI sentiment analysis and more to boost LotwiZe into a leader in the real estate valuation market.