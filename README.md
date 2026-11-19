# Game Investment analyzer

My app helps smaller game developers decide what game genre to invest in by analyzing genre popularity, player satisfaction and market pricing found in the Steam data.

> A course project for **MIST 4600: Computer Programming in Business** at the University of Georgia's Terry College of Business (Fall 2026).

## Problem
Small video game development studios face uncertainty when deciding which genre to invest in for their next game. With limited resources and many copeting genres, developers need a way to identify which genres offer the strongerst market opportunities. My app addresses this problem by analyzing Steam games data to compare player demand, customer satisfaction, and pricing across different genres.

## What it does
My app Game Investment Analyzer answers three questions:
1. **Sub-question 1:** Which genres combine strong demand with relatively fewer competing games?
2. **Sub-question 2:** Which genres have the highest average positive review percentage?
3. **Sub-question 3:** Which genres have the highest typical selling price?
The app also uses the Google Gemini API to interpret the results and explain potential investment opportunities.

## Data
The [Steam Games Dataset](https://www.kaggle.com/datasets/artermiloff/steam-games-dataset) on Kaggle, collected in March 2025. The dataset is shared under the MIT License by its creator, artermiloff. This repo uses `steam_games.csv`, a smaller file made for the course: the 1,000 games with the most reviews.

## Built with
- Python and pandas, in Google Colab
- Coming soon: Gemini API

## How to run it
1. Open the project's .ipynb notebook in Google Colab.
2. Upload steam_games.csv to Google Drive.
3. Obtain a Gemini API key from Google AI Studio.
4. In Colab, open Secrets and save the key as GOOGLE_API_KEY. Enable notebook access.
5. Select Runtime -> Run all to execute the notebook.
6. View the results for all three sub-questions and Gemini's results.
Never put your API key directly into the notebook or GitHub repository.

## Example output
```text
genres
Indie         89.648019
Casual        88.630137
Simulation    86.734375
Adventure     86.171765
Strategy      85.068293
```
### Sub-question 1: 
Sports has the highest demand-to-competition
score, with an average of 2.72 million owners across 39 games.

### Sub-question 2: 
Indie games have the highest average positive
review percentage at 89.65%, followed by Casual at 88.63%.

### Sub-question 3: 
Action, Adventure, Sports, RPG, and Strategy
all have a median selling price of $19.99.


## AI Use Disclosure

## Author
Rachel White - MIST 4600. University of Georgia, Fall 2026
