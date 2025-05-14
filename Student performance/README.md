# Student Habits vs Performance
This project explores the relationship between student habits and academic performance using machine learning. 
By analyzing data on behaviors such as study time, screen time, extracurricular activities and other factors. The goal is to build predictive models that estimate student exam scores. This can help identify which habits most significantly impact performance, offering practical insights for students and educators.

# Dataset
### Source: https://www.kaggle.com/datasets/jayaantanaath/student-habits-vs-academic-performance
### File: student_habits_performance.csv
### Cleaned File: Cleaned_student_habit_performance.csv

# Process
## Data Cleaning
The data was already cleaned so I didn't have to deal with missing values or any messy data

## Handling categorical data
There were several categorical columns that I handled:
- gender: This column have three variables(Male, Female, Other). These variables did not have an inherent order/ranking so I used a Label encoder to encode it.
  
- part_time_job: This column have two variables(Yes, No). These variables also did not have an order/ranking so I used a Label encoder to encode it.
  
- diet_quality: This column have three variables(Poor, Fair, Good). These variables have an order/ranking, so I used an ordinal encoder to encode it.
  
- parental_education_level: This column have four variables(None, High School, Bachelor, Master). These variables have an order/ranking, so I used an ordinal encoder to encode it.
  
- internet_quality: This column have three variables(Poor, Average, Good). These variables have an order/ranking, so I used an ordinal encoder to encode it.
  
- extracurricular_participation: part_time_job: This column have two variables(Yes, No). These variables did not have an order/ranking so I used a Label encoder to encode it.

## Multicolinearity
Multicolinearity occurs when two or more independent variables/ features in a regression model are highly corelated with each other. This can reduce model interpretability or lower the predictive performance.
I checked for multicolinearity using a heatmap and there was no instance of multicolinearity in this dataset

## Model Training and Evaluation
To predict student performance based on their habits, I trained and evaluated multiple machine learning algorithms, including:
- Linear Regression
- Decision Tree Regression
- Random Forest Regression
I trained and evaluated each model with and without feature selction to handle Overfitting and Underfitting
## Observation
### I used the R2 score and mean absolute error metrics to measure the perofrmance of the models

### Linear Regression
- The model performed well. I was able to handle overfitting using feature selection. The accuracy of the model dropped compared to when i trained and tested without feature selection

### Decision Tree Regression
- The model performed poorly compared to the Linear regression model
- Using a decision tree regressor, there was a case of overfitting. Even after using feature selection, the model was still overfitted.

### Random Forest Regression
- The model performed better than the Decision tree model but less than the Linear regression model
- Using a Random forest regressor, there was a case of overfitting. It was not as high as the decision tree model. Also the test accuracy increased after using feature selection

### After using the three different algorithms, I came to the conclusion that the Linear regression model was best suited for this.

## Tools Used
- Python
- Pandas
- Numpy
- Seaborn/Matplotlib
- Jupyter notebook
- Sklearn

## Future work
- Add dashboard visualizations

## License
- This project is for educational and portfolio purposes only.
