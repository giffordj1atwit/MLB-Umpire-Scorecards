# MLB-Umpire-Scorecards

## Introduction
The goal of this project was to use the knowledge gained in class to analyze the accuracy of home plate umpires in Major League Baseball. The officiating is often under 
fire in this organization, and I wanted to see for myself whether this was warrented. In the baseball world, there seems to be a stigma that calls made by home plate
umpires, specifically those involving balls and strikes, have been getting worse in the past several years, to the point where the use of robot umpires has become a 
popularly debated idea. In this project, I wanted to test whether this was actually a reasonable conclusion, as well as analyze some other patterns in terms of umpire
accuracy.

## Data Selection
The dataset used is a Kaggle dataset which stores "umpire scorecards" from every MLB game from 2015 to 2022, both during the regular and postseason. An umpire scorecard
is a metric that allows for the "grading" of a home plate umpire during a game. Contained within the dataset were the following columns:

ID Number
Date the game occurred
Umpire Name
Home Team
Away Team
Home Team Runs
Away Team Runs
Pitches Called by Umpire
Incorrect Calls
Expected Incorrect Calls: statistic measuring how many calls we expect the umpire to miss
Correct Calls
Expected Correct Calls
Correct Calls Above Expected: difference between correct calls and expected correct calls
Accuracy: percentage of pitches that were ruled correctly
Expected Accuracy
Accuracy Above Expected
Consistency of calls (measured as percentage
Favor Home: Number of runs given in favor of home team as a result of umpire calls
Total Run Impact: Number of runs impacted by umpire calls

This dataset was stored as a csv file, then opened in a Jupyter notebook for analysis. There were two significant acts of data cleaning that were done. The first was 
to remove incomplete ("ND") rows. The second was to convert the columns we needed to use from objects to floats.

## Methods

## Results

## Discussion

## Code

## Reference
