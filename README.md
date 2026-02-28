# VADER Sentiment Analyzer

A simple, interactive Python script that utilizes the **NLTK (Natural Language Toolkit)** library to analyze the sentiment of a given text. It classifies text into five categories based on the **VADER (Valence Aware Dictionary and sEntiment Reasoner)** algorithm.

## Features

* Takes user input directly from the console.
* Uses NLTK's `SentimentIntensityAnalyzer` for analysis.
* Provides a numerical compound score and a descriptive sentiment label with emojis.

## How it Works

The script follows these steps:

1.  **Download Lexicon:** Downloads the necessary VADER lexicon data using `nltk.download('vader_lexicon')`.
2.  **Analyze Text:** Breaks down the input text and calculates a compound score ranging from **-1** (Extremely Negative) to **+1** (Extremely Positive).
3.  **Classify Sentiment:** Maps the compound score to a human-readable label based on specific thresholds.

## Thresholds Mapping

| Compound Score ($s$) | Sentiment Label |
| :--- | :--- |
| $s > 0.5$ | Very Positive! 🌟 |
| $0 < s \le 0.5$ | Slightly Positive 🙂 |
| $s = 0$ | Neutral 😐 |
| $-0.5 \le s < 0$ | Slightly Negative 🙁 |
| $s < -0.5$ | Very Negative 💢 |

## Requirements

To run this script, you will need the following:

* Python
* NLTK
