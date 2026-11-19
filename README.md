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

### Sub-Question 1: Demand vs. Competition
Which genres combine strong demand with relatively fewer competing games?

| Genre | Average Owners | Number of Games | Score |
|---|---:|---:|---:|
|Sports| 2,723,077 | 39 | 69,822.49 |
| Racing | 1,925,806 | 31 | 62,122.79 |
| Massively Multiplayer | 4,579,630 | 108 | 42,403.98 |
| Early Access | 2,830,435 | 69 | 41,020.79 |
| Free To Play | 5,067,725 | 189 | 26,813.36 |

**Finding:** Sports has the highest demand-to-competition score, suggesting relatvely strong player demand compared with the number of competing games.
### Sub-question 2: Positive Review Percentages

Which genres have the highest average positive review percentage?

| Genre | Average Positive Reviews |
|---|---:|
| Indie | 89.65% |
| Casual | 88.63% |
| Simulation | 86.73% |
| Adventure | 86.17% |
| Strategy | 85.07% |

**Finding:** Indie games have the highest average positive review percentage at 89.65%, followed by Casual games at 88.63%.

### Sub-question 3: Typical Selling Prices

Which genres have the highest typical selling price?

| Genre | Median Price |
|---|---:|
| Action | $19.99 |
| Adventure | $19.99 |
| Sports | $19.99 |
| RPG | $19.99 |
| Strategy | $19.99 |

**Finding:** These five genres have a median selling price of $19.99, suggesting similar typical listed prices among them.

## Final Investment Reccommendation
Based on my analysis, I recommend that a game developer consider investing in the **Sports** genre. Sports has the highest demand-to-competition score of 69,822.49, with approximately 2.72 million average estimated owners and 39 competing games in the dataset.

Sports also has a median selling price of $19.99, placing it among the highest-priced genres returned by the analysis.

However, Sports has an average positive review percentage of 76.15%, which is lower than Indie (89.65%) and Casual (88.63%).

Overall, Sports appears to offer a promising combination of player demand, competition, and pricing. However, these results do not guarantee that a new Sports game will be successful.


## AI Use Disclosure

## Author
Rachel White - MIST 4600. University of Georgia, Fall 2026
