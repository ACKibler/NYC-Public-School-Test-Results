Every year, American high school students take SATs, which are standardized tests intended to measure literacy, numeracy, and writing skills. There are three sections - reading, math, and writing, each with a maximum score of 800 points. These tests are extremely important for students and colleges, as they play a pivotal role in the admissions process.

Analyzing the performance of schools is important for a variety of stakeholders, including policy and education professionals, researchers, government, and even parents considering which school their children should attend.

You have been provided with a dataset called schools.csv, which is previewed below.

You have been tasked with answering three key questions about New York City (NYC) public school SAT performance.

## Import pandas as pd
#import pandas as pd

## Read in the data
#schools = pd.read_csv("schools.csv")

## Preview the data
#schools.head()

## Create a pandas DataFrame called best_math_schools containing the "school_name" and "average_math" score for all schools where the results are at least 80% of the maximum possible score, sorted by "average_math" in descending order.

#best_math_schools = schools[schools["average_math"] >= 640][["school_name","average_math"]]
#best_math_schools = best_math_schools.sort_values(by="average_math", ascending=False)
#print(best_math_schools)

## Identify the top 10 performing schools based on scores across the three SAT sections, storing as a pandas DataFrame called top_10_schools containing the school name and a column named "total_SAT", with results sorted by total_SAT in descending order.
#schools["total_SAT"] = schools[["average_math", "average_reading", "average_writing"]].sum(axis=1)
#top_10_schools = schools[["school_name", "total_SAT"]].sort_values(by="total_SAT", ascending=False).head(10)
#print(top_10_schools)

## Locate the NYC borough with the largest standard deviation for "total_SAT", storing as a DataFrame called largest_std_dev with "borough" as the index and three columns: "num_schools" for the number of schools in the borough, "average_SAT" for the mean of "total_SAT", ##and "std_SAT" for the standard deviation of "total_SAT". Round all numeric values to two decimal places.

#borough_stats = schools.groupby('borough')["total_SAT"].agg(['count','mean','std']).round(2)
#borough_stats.columns = ['num_schools','average_SAT','std_SAT']
#largest_std_dev = borough_stats[borough_stats['std_SAT'] == borough_stats['std_SAT'].max()]
#print(largest_std_dev)
