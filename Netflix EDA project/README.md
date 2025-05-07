# Netflix Titles Data Analysis
This project explores and analyzes the netflix titles dataset to uncover insights about the platorm's content library. My goal is to clean the dataset,perform exploratory data analysis and prepare it for possible machine learning tasks.

# Dataset
### Source: https://www.kaggle.com/datasets/shivamb/netflix-shows
### File: netflix_titles.csv
### Cleaned File: cleaned_netflix.csv

# Process
## Data Cleaning

Dropped Columns
. I dropped the "ID" column because it was just a unique identifier and had no meaningful relationship with the data
. I dropped the "director" column because it had a lot of missing values and also a high cardinality which made it messy to work with
. I dropped the "cast" column too because it was not really important for my analysis
. I dropped the "description" column bacause it was just an unstructured summary of a movie/tv show

Missing values
. I replaced the missing values in the "country" column with "Unknown"
. I dropped the rows with missing values in the "Date added" column
. I dropped the rows with missing values in the "rating" column
. I dropped the rows with missing values in the "duration" column

.I sorted the data accordingly from newest down to the oldest and reset the index.
. I extracted date-related features(year_added, month_added)

## Exploratory Data Analysis(EDA)
. I visualized:
   . Top countries by content
   . Content rating distribution
   . Content type breakdown
   . Titles released by year
   . Duration categories for both Movies and TV shows
. Used both standard and visually enhanced charts (Seaborn and Plotly)


## Observations
. The country with the highest content on netflix was the US and Mexico the lowest
. TV-MA is the most common rating, followed by TV-14
. There are more Movies than Tv shows on netflix
. The number of titles released grew rapidly from 2010 and peaked in 2018

## Tools Used
. Python
. Pandas
. Numpy
. Seaborn/Matplotlib/Plotly
. Jupyter notebook

## Future work
. Build a machine learning model to predict content duration or type
. Add dashboard visualizations

## License
This project is for educational and portfolio purposes only.
