# Predicting Hit Songs with Machine Learning

## Project Overview

This project focuses on developing a predictive model that can accurately predict whether a song will be a hit. Leveraging data from the leading music analytics company Chartmetric and utilizes a range of metrics from various sources, including Spotify Popularity Scores, Editorially Created Music Top Charts data, and YouTube view performance., the model aims to democratize the music industry's decision-making process by using objective, data-driven insights.  

This initiative that we've embarked on could significantly impact marketing strategies, improve lesser known artist exposure, and promote better financial planning in the music industry which would better reward human creativity at a global scale.

## Features
- **Data Sources**: Utilizes comprehensive data from Chartmetric, including Spotify and YouTube metrics.
- **Machine Learning Model**: Employs a RandomForestClassifier to predict song success based on various musical features and audience engagement metrics.
- **Evaluation Metrics**: Precision, Recall, F1 Score, and Accuracy are used to measure the model's performance.

## Built With
- **Python**: The scripting language used.
- **scikit-learn**: Machine learning library used.
- **Pandas**: Used for data manipulation and analysis.
- **Chartmetric API**: Primary data source.

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
What things you need to install the software and how to install them:
```bash
python >= 3.6
numpy
pandas
scikit-learn
matplotlib  # Optional for plotting

### Installing
A step-by-step series of examples that tell you how to get a development environment running:

Clone the repository:
git clone https://yourrepository.com/hit-song-predictor.git

## Creating & Understanding the Data Sets

To create the data sets to achieve the objective of this project, we analyzed tracks from top artists, who have historically produced hit tracks, to train our predictive model. Once trained, the model is then used to analyze newer, lesser-known releases that have potential to become hits. We aim to apply our model to predict the hit potential of the last year's newer, lesser-known releases, and then compare those predictions with actual outcomes to validate the accuracy and effectiveness of our model.

### Step 1 - The X DataSet

The X DataSet comprises tracks from top artists provided by ChartMetrics. This dataset includes tracks that have achieved hit status and others that have not, providing a robust basis for training our predictive model.

**Run File:**
Final - Alisha - Nico - Consolidate And CleanUp Data For ML.ipynb

Note: This takes a very long time to run because we are processing a large data set & joining Artists, Tracks & Charts data to create all of the base CSV data files we will later combine.

### Step 2 - The Y DataSet

The Y DataSet includes new releases sourced from ChartMetrics that were less known at the time of discovery. This dataset consists of new artists and obscure artists, making it ideal for testing the model's ability to predict potential hits.

**Run File:**
Final - Alisha - Danny Group 9 - New Releases To Predict If It Is Hit From Spotify.ipynb

Note: This contains some of our initial EDA to analyze newer tracks to determine what being a Hit means by looking at a variance of High Hit probablity vs Low Hit Probability based on editorial inclusion, chart & playlist mentions.

### Step 3 - Data Consolidation and Standardization

After thorough data analysis, we standardized the dataset to include fields that consistently provided reliable indicators of a song's potential to be a hit. These fields were selected based on their reliability across all tracks and their contribution to the model's accuracy as we optimized the model try out different data sources.

**Fields used:**
- `cm_track_id`
- `isrc`
- `name`
- `IsHit`
- `cm_artist`
- `artist_names`
- `spotify_popularity`
- `score`
- `track_genre`
- `image_url`
- `artist_images`
- `spotify_artist_ids`
- `explicit`
- `region_codes`

**Run File:**
Final - Alisha - ML Model Train And Optimization.ipynb

## Model Development and Evaluation
* Model: Utilized RandomForestClassifier due to its effectiveness in managing overfitting and its robustness with large datasets.
* Training Process: Data was split into training and test sets with a 70:30 ratio, ensuring a random distribution.
* Performance Metrics: Precision, Recall, F1 Score, and overall Accuracy to evaluate the model
- **Precision:** 0.9397715472481828
- **Recall:** 0.8792098445595855
- **F1 Score:** 0.9084825163125314
- **Accuracy:** 0.8989283074648928

These results indicate a high level of accuracy in predicting hits, reinforcing the effectiveness of the chosen features and model architecture.

## Conclusion

The predictions from our model are saved in 'Final_PredictedNewHits.csv', providing insights into which new tracks might become future hits. This project not only highlights the potential of machine learning in the music industry but also offers a valuable tool for artists, producers, and labels to forecast track success.

## Visualizations & Presentations

See our presentation overview deck presented on July 9 2024 online at https://docs.google.com/presentation/d/1MqyydFH2bMGaiJKFjRCEsg0WE7KQXcR6fZeFPb2IWEQ/edit?usp=sharing

![image](https://github.com/Project2andTeam9/Team_9/assets/154397635/0b513399-c450-4218-98ec-d1b8c914b57b)

![image (1)](https://github.com/Project2andTeam9/Team_9/assets/154397635/7ef3d716-748d-4dce-a76a-a9bace2babd3)

![image (2)](https://github.com/Project2andTeam9/Team_9/assets/154397635/153c0a0f-2aae-4bcb-9c54-b955afbe0047)

![image (3)](https://github.com/Project2andTeam9/Team_9/assets/154397635/4c93fa92-1537-4ea9-b741-f525c1cde4cb)

![image (4)](https://github.com/Project2andTeam9/Team_9/assets/154397635/11f00ab7-6969-4f3e-81b0-453283da31f0)

![image (5)](https://github.com/Project2andTeam9/Team_9/assets/154397635/c3f8d3e5-4d2c-4804-92ea-560df132dbc4)

![image (6)](https://github.com/Project2andTeam9/Team_9/assets/154397635/7166ab9d-8417-4a1d-a455-c9fc538d4eb6)

![NumberOfBigHitsandLowHits](https://github.com/Project2andTeam9/Team_9/assets/154397635/7e17fe2f-e1e7-4b36-a6dd-374b6a1fddcc)

![TrackAppearanceFrequencies](https://github.com/Project2andTeam9/Team_9/assets/154397635/b19d93ab-bdbf-4b95-9b52-1d09352cbd15)

