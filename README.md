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
### Sub-question 1: Demand vs. Competition

Which genres combine strong demand with relatively fewer competing games?

```text
                       avg_owners  num_games         score
genres
Sports                 2.723077e+06         39  69822.485207
Racing                 1.925806e+06         31  62122.788762
Massively Multiplayer  4.579630e+06        108  42403.978052
Early Access           2.830435e+06         69  41020.793951
Free To Play           5.067725e+06        189  26813.359088
```

**Finding:** Sports ranks first with a demand-to-competition score of 69,822.49. Its average estimated ownership of 2.72 million across 39 games suggests relatively strong demand compared with the number of competitors.

### Sub-question 2: Positive Review Percentages

Which genres have the highest average positive review percentage?

```text
genres
Indie         89.648019
Casual        88.630137
Simulation    86.734375
Adventure     86.171765
Strategy      85.068293
Name: pct_pos_total, dtype: float64
```

**Finding:** Indie has the highest average positive review percentage at 89.65%, followed by Casual at 88.63%. These genres have the strongest average customer satisfaction among the genres analyzed.

### Sub-question 3: Typical Selling Prices

Which genres have the highest typical selling price?

```text
genres
Action       19.99
Adventure    19.99
Sports       19.99
RPG          19.99
Strategy     19.99
Name: price, dtype: float64
```

**Finding:** All five genres returned by the analysis have a median selling price of $19.99. This suggests that several genres have similar typical listed prices, making demand and customer satisfaction important additional considerations.


## AI Use Disclosure
- **I used AI tools:** Yes
- **Tools:** ChatGPT and Google Gemini
- **What I asked:** Help writing and explaining Python code, debugging errors, creating functions, connecting the Gemini API, and interpreting my results.
- **What I added, changed, or fixed in the AI's output:** Selected my three sub-questions, tested the code in Google Colab, fixed errors with the genre data, and reviewed the results.
- **What I designed and wrote entirely myself:** Developed game idea, identified the business problem I wanted it to solve, and formulated my final recommendation.
- **I understand every line of code I am submitting:** Yes
## Author
Rachel White - MIST 4600. University of Georgia, Fall 2026
