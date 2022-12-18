# Medical-Data-Visualizer
This project is part of FreeCodeCamp's 'Data Analysis with Python' course completion exercise. In this project, matplotlib, seaborn, and pandas are used to make visualization and calculations from the medical examination data. 
The rows in the dataset represent patients and the columns represent information like body measurements, results from various blood tests, and lifestyle choices. The dataset is used to explore the relationship between cardiac disease, body measurements, blood markers, and lifestyle choices. 

## Tasks:
Create a chart similar to examples/figure_1.png, where the counts of good and bad outcomes for the cholesterol, gluc, alco, active, and smoke variables for patients with cardio=1 and cardio=0 in different panels.

Use the data to complete the following tasks:
- Add an overweight column to the data. To determine if a person is overweight, first calculate their BMI by dividing their weight in kilograms by the square of their height in meters. If the value is > 25, then the person is overweight. Use the value 0 for NOT overweight and the value 1 for overweight.
- Normalize the data by making 0 always good and 1 always bad. If the value of cholesterol or gulc is 1, make the value 0. If the value is more than 1, make the value 1.
- Convert the data into long format and create a chart that shows the value counts of the cathegorical features using seaborn's catplot(). The dataset should be split by 'Cardio' so there is one chart for each cardio value. The chart should look like examples/figure_1.png. 
- Clean the data. Filter out the following patient segments that represent incorrect data:
  - diastolic pressure is higher than systolic (Keep the correct data with (df['ap_lo'] <= df['ap_hi'])).
  - height is less than the 2.5th percentile (Keep the correct data with (df['height'] >= df['height'].quantile(0.025))).
  - height is more than the 97.5th percentile.
  - weight is less than the 2.5th percentile.
  - weight is more than the 97.5th percentile.
- Create a correlation matrix using the dataset. Plot the correlation matrix using seaborn's heatmap(). Mask the upper triangle. The chart should look like examples/figure_2.png.

Any time a variable is set to None, make sure to set it to the correct code. 
