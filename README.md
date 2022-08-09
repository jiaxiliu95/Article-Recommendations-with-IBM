## Table of Contents

- [Installation](#Installation)

- [Project Motivation](#ProjectMotivation)

- [File Descriptions](#FileDescriptions)

- [Results](#Results)

- [Acknowledgments](#Acknowledgments)

## Installation

The Jupyter Notebook should be able to work without any issue using Python version 3.. with the libraries in the [requirements.txt](requirements.txt) installed. 

## Project Motivation

The dashboard on the IBM Watson Studio is showing the newest articles to the users. However, a better recommendation strategy is to show articles that are most pertinent to a specific user.

The target of this project is to make recommendations based on the interactions that users have with articles on the platform. 

## File Descriptions

Here is a description of the files in this repository:

- [data](data)
  - [articles_community.csv](/data/articles_community.csv) : portfolio data of the articles, including the article id, article name, article description and article body.
  - [user_item_interactions.csv](user_item_interactions.csv): the user-item interactions, including the article id, the article name, and the email of the user who reads the article.
  - [user_item_matrix.p](user_item_matrix.p) : a user-item interaction matrix that is ready to use for analysis.
- [requirements.txt](requirements.txt) : one can use this file to set up the environment required for this project.
- [Recommendations_with_IBM.ipynb](Recommendations_with_IBM.ipynb) : analysis and results for the project (one can run the code in Jupyter Notebook with required libraries installed).
- [project_tests.py](project_tests.py) : include the tests used in the analysis
- [top_5.p](top_5.p), [top_10.p](top_10.p), [top_20.p](top_20.p): correct solutions for the tests in project_test.py.

## Results

The project makes rank-based recommendations, user-user-based collaborative filtering and recommendations made by matrix factorization.

The accuracy of the matrix factorization on the test set decreases with the number of latent features, but still achieves 96%.

However, this result cannot tell whether there would be an improvement to how users currently find articles. To determine that, further experiment, i.e., an A/B test, will need to be conducted.

## Acknowledgments

The project is originated from [Udacity Data Scientist Nanodegree](https://www.udacity.com/course/data-scientist-nanodegree--nd025). The data used in this project is credited to the IBM Watson Studio platform. 