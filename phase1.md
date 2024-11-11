# In Phase 1, we were to analyze the data from [SCI](https://amar.org.ir)

## In the First Segment: Statistical Analysis Section

In this section, we aim to address several questions using statistical methods. Some questions are posed to help build intuition and understanding of the data, others come from a specific individual, and finally, there are hypotheses that require validation.

1. **Plot the household information distribution**  
   - Attributes: education level, age, relationship to head of household, employment status.

2. **Visualize household vehicle usage**  
   - Types: car, motorcycle, bicycle, etc.  
   - By year.

3. **Display a cumulative chart**  
   - Pension income distribution.  
   - Property rental expenses (housing, garden, etc.) by year.

4. **Plot annual household spending trends**  
   - Categories: prepared foods, hotels, and restaurants.

5. **Create a correlation matrix**  
   - Categories: expenditures on clothing and footwear, food, housing, utilities, water, sewage, and healthcare.

6. **Define income types and plot trends**  
   - **Real Income**: Adjusted income considering inflation.  
   - **Nominal Income**: Unadjusted income, without accounting for inflation.  
   - Plot both real and nominal income trends on one chart.

### Hypothesis Testing

- Is household income equal in urban and rural areas in the Chaharmahal and Bakhtiari province?

- Is there a noticeable difference in the average property value between urban and rural areas?

- Is there a significant difference in annual income between individuals who attended university and those who did not?

- Additionally, evaluate the following statement with hypothesis testing, explanations, and in-depth analysis:  
  *"An individual claims that urban income increased in 2022 compared to 2021, indicating a better standard of living for urban residents in 2022."*

## Second Segment: Clustering Problem

### Problem 1: Clustering

In the first question, assume that the current household decile system is not informative. Therefore, you want to cluster households based on total household expenses and income from the years 1398 and 1401. Note that you need to calculate each household's total expenses and income using a suitable method you propose.

#### Part 1

Run the K-means clustering algorithm on this dataset with 10 clusters. Then, plot the scatter plot and clearly indicate which points correspond to which cluster, as well as the center of each cluster. Pay special attention to the choice of colors, markers, axis labels, and overall clarity of the visualization.

#### Part 2

After that, run the K-means algorithm for different values of k (from 1 to 20). Calculate the sum of squared distances within clusters (Within-Cluster Sum of Squares) and select an appropriate value for the hyperparameter k. Note that a significant portion of the score for this section depends on the approach used to select the value of k. If the methods covered in class are insufficient, it is expected that you research and propose a suitable method to address any challenges.

#### Part 3

In the final step of this question, use the DBSCAN algorithm to cluster the data and adjust the hyperparameters to obtain a meaningful output with 10 clusters. Plot the data points in a scatter plot, showing the clusters formed. Explain how each hyperparameter affects the output.

## Third Segment: Prediction Problem

Predicting household expenditures in various domains can help guide investment decisions in those areas.

In this section, we ask you to train a model that, given household data, predicts the monthly transportation expenditure of a household.

- You may use any machine learning algorithms that have been taught in bootcamp classes for modeling.
- **Note:** Using algorithms outside of the main ones taught in class is not allowed for the main task. However, you can use additional algorithms for bonus points if you are interested and confident in their application, provided all team members have a sufficient understanding of the chosen method.
- You may add or engineer any desired features to the dataset if needed, but ensure that the model’s input features do not lead to target leakage.

To evaluate your final model, use the data from Winter 2023 as the test set.

- Compare your model’s predictions with the actual test data and plot the loss and R² charts.
- When presenting your results, provide an appropriate analysis of the outcomes.
