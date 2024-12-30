# Sentiment Analysis Project

## Overview
This project demonstrates a machine learning approach using **Long Short-Term Memory (LSTM)** networks to predict sentiment (positive or negative) based on the `twitter_training` dataset.

The primary objective is to classify tweets into either positive or negative sentiment categories.

---

## Features
- **Dataset:** The `twitter_training.csv` file is used, which contains the following columns:
  - `seq`: Sequence ID
  - `brand`: The associated brand mentioned in the tweet
  - `sentiment`: Sentiment of the tweet (Positive/Negative)
  - `text`: Actual tweet content
- **Model:** LSTM-based sentiment analysis
- **Language:** Python
- **Libraries:** Pandas, TensorFlow/Keras, and other essential machine learning tools.

---

## Setup

### Prerequisites
Before running the project, ensure you have the following installed:
- Python 3.8+
- Required libraries (install via `requirements.txt` if available)

### Install Dependencies
```bash
pip install pandas tensorflow numpy matplotlib
```

---

## Getting Started

### Dataset
Read the dataset using the following code snippet:

```python
import pandas as pd

# Read the dataset
columns = ['seq', 'brand', 'sentiment', 'text']
df = pd.read_csv('twitter_training.csv', names=columns)

# Display the first 5 rows
df.head()
```

Sample output:

| seq  | brand       | sentiment | text                                        |
|------|-------------|-----------|---------------------------------------------|
| 2401 | Borderlands | Positive  | im getting on borderlands and i will murder yo... |
| 2401 | Borderlands | Positive  | I am coming to the borders and I will kill you... |
| 2401 | Borderlands | Positive  | im getting on borderlands and i will kill you ... |
| 2401 | Borderlands | Positive  | im coming on borderlands and i will murder you... |
| 2401 | Borderlands | Positive  | im getting on borderlands 2 and i will murder ... |

---

### Model Implementation
The LSTM model is implemented using TensorFlow/Keras. It processes the `text` column to predict the sentiment (`Positive` or `Negative`).

**Key steps:**
1. Preprocess the text data (e.g., tokenization, padding, and embedding).
2. Define the LSTM architecture.
3. Train and evaluate the model.

---

## Project Structure
```
.
├── twitter_training.csv      # Dataset
├── sentiment_analysis.py     # Main script
├── requirements.txt          # Dependencies
└── README.md                 # Project documentation
```

---

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/Aderonke25/Sentiment-Analysis-project.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Sentiment-Analysis-Project
   ```
3. Run the script:
   ```bash
   python sentiment_analysis.py
   ```

---

## Results
The LSTM model predicts whether the sentiment of a given tweet is positive or negative. The accuracy and performance metrics are evaluated and logged during training.

---

## Contributing
Contributions are welcome! Feel free to submit a pull request or open an issue if you have ideas to improve the project.

---

## License
This project is licensed under the [MIT License](LICENSE).

---

## Acknowledgments
Special thanks to the creators of the `twitter_training` dataset and the open-source community for providing amazing tools and resources!
