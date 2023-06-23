# MLB Umpire Scorecards: An Analysis

## Introduction
The goal of this project was to use the knowledge gained in class to analyze the accuracy of home plate umpires in Major League Baseball. The officiating is often under 
fire in this organization, and I wanted to see for myself whether this was warrented. In the baseball world, there seems to be a stigma that calls made by home plate
umpires, specifically those involving balls and strikes, have been getting worse in the past several years, to the point where the use of robot umpires has become a 
popularly debated idea. In this project, I wanted to test whether this was actually a reasonable conclusion, as well as analyze some other patterns in terms of umpire
accuracy.

## Data Selection
The dataset used is a Kaggle dataset which stores "umpire scorecards" from every MLB game from 2015 to 2022, both during the regular and postseason. An umpire scorecard
is a metric that allows for the "grading" of a home plate umpire during a game. Contained within the dataset were the following columns:

- ID Number
- Date the game occurred
- Umpire Name
- Home Team
- Away Team
- Home Team Runs
- Away Team Runs
- Pitches Called by Umpire
- Incorrect Calls
- Expected Incorrect Calls: statistic measuring how many calls we expect the umpire to miss
- Correct Calls
- Expected Correct Calls
- Correct Calls Above Expected: difference between correct calls and expected correct calls
- Accuracy: percentage of pitches that were ruled correctly
- Expected Accuracy
- Accuracy Above Expected: similar to correct calls above expected
- Consistency of calls (measured as percentage)
- Favor Home: Number of runs given in favor of home team as a result of umpire calls
- Total Run Impact: Number of runs impacted by umpire calls

This dataset was stored as a csv file, then opened in a Jupyter notebook for analysis. There were two significant acts of data cleaning that were done. The first was 
to remove incomplete ("ND") rows. The second was to convert the columns we needed to use from objects to floats.

## Methods
The primary tools that were used for the analysis of this data were as follows:

- pandas
- matplotlib
- Jupyter notebook

## Results
To answer the question at hand, we need to analyze several statistical categories. The most important categories for determining the quality of an umpire's game are accuracy, total run impact (additionally, we analyzed the favor home stat for similar reasons), accuracy above expected, and consistency. From the data, we discover the following.

Accuracy
Average: 92.42%

![image](https://user-images.githubusercontent.com/71138022/205470887-a603d4ea-d7a2-44ba-81c6-c3a1790a6c67.png)

Total Run Impact
Average: 1.53 runs

![image](https://user-images.githubusercontent.com/71138022/205471843-13b54d30-838b-4a63-92bd-d09e5573961c.png)

Home Favored
Average: 0.03 runs

![image](https://user-images.githubusercontent.com/71138022/205470963-a2bdadf1-2611-41ed-9279-d7231e7b3518.png)

Accuracy Above Expected
Average: 0.14%

![image](https://user-images.githubusercontent.com/71138022/205470989-222dbbde-9600-49ea-bbb9-1c108e4859ee.png)

Consistency

![image](https://user-images.githubusercontent.com/71138022/205470998-fe4fb3ce-1a2b-41aa-9461-8693e8e81139.png)


To answer the second part of our question, we need to group the data by the year the game occurred. To do this, we can separate the data into 8 different tables, take 
their averages for accuracy, accuracy above expected, and consistency, and graph the results, which are shown below.

![image](https://user-images.githubusercontent.com/71138022/205471240-0e0bd1d6-b4e4-4532-9ddf-887c0a8cf85e.png)


![image](https://user-images.githubusercontent.com/71138022/205471245-6d227e2f-6d82-46bc-aba0-da5a4e01ca34.png)


![image](https://user-images.githubusercontent.com/71138022/205471254-1bfd9ff9-7ef0-491e-a889-848c715bc10e.png)


## Discussion
From the results, we can make several observations. While the average accuracy of an umpire in the entire dataset is only 92.42%, which is lower than one would hope,
there are several other areas that show that umpires actually are better than many believe. We see that umpires overperform their expected accuracy more often than
they underperform. We also see that these two statistics have risen from 2015-2022, implying that umpires have actually gotten better over this time. A similar
observation can be made in the consistency category. It also seems to have a lower than desirable average, but has not shown any negative trend over the eight
years of data. However, there is not a notable rise in consistency above the mean of approximately 92%. In fact, any difference in consistency from 2015 to 2022 is 
negligable. Nevertheless, this data seems to refute the narrative that umpiring has gotten worse over time. Instead, it seems to imply the opposite.

The area where opponents of today's umpiring do see some results that support their ideas is in the run impact category. On average, umpire calls impact a game's
outcome by 1.53 runs, which is much higher than the ideal 0. This does seem to show some issues in officiating, but this is the only noticeable negative trend in the
data.

In terms of future research, there are two more studies I would be interested in performing. First is grouping the data by specific umpires, and finding which are
the best and worse using similar methodology to the above. I would also look into which teams receive better umpiring to determine if there are any anomalies in that 
area.

## Summary
Overall, MLB umpires have an accuracy of about 92%. They also outperform their expected accuracy by an average of 0.14% and have been improving in these statistics
from 2015 to 2022. Consistency in calls also is about 92%, but there has not been any significant change from 2015 to 2022. Umpires do affect the outcome of a game by
an average of 1.53 runs, which indicates some issues. However, while this specific statistic does not reflect well on umpires, the rest of the data seems to show a
higher quality in officiating than many claim.

## Code
https://github.com/giffordj1atwit/MLB-Umpire-Scorecards/blob/main/Individual%20Project.ipynb

## Reference
"MLB Baseball Umpire Scorecards (2015 - 2022)", _Advanced Statistics of MLB Baseball Umpire Performance (2015 - 2022)_, Kaggle, 2022, https://www.kaggle.com/datasets/mattop/mlb-baseball-umpire-scorecards-2015-2022. Accessed 3 December 2022.
