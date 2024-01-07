# Sentiment Analysis and Drug Recommendation System

## Overview
This repository contains code for sentiment analysis on drug reviews and a drug recommendation system based on user sentiments. Reviews play a crucial role in determining a drug's useful count and rating, influencing the user's trust in the medication. The polarity of these reviews aids users in assessing the efficacy and usefulness of the medicine.

## Setup
Before running the code, ensure that you have the necessary dependencies installed. Use the following command to install them:

```bash
pip install -r requirements.txt
```

Additionally, make sure to include NLTK's stopwords for efficient text processing.

```python
import nltk
nltk.download('stopwords')
```

## Sentiment Analysis
The sentiment analysis is conducted using the VADER lexicon from NLTK. Lexical techniques are applied to determine sentiments based on the reviews. Sentiments are categorized as negative, neutral, or positive, providing valuable insights into user opinions.

### Lexicon Mapping
- "awful" is mapped to -2.5
- "okay" is mapped to 0.9
- Emoticons "/-:" is translated to -1.3, and "0:-3" is translated to 1.5.

## Stopwords Removal
Stopwords, such as common words like "the," "a," and "in," can be ignored to save storage space and processing time. NLTK provides a list of stopwords in various languages, which can be utilized for this purpose.

```python
from nltk.corpus import stopwords
stop_words = set(stopwords.words('english'))
```

## Drug Recommendation System
The drug recommendation system utilizes sentiments derived from reviews to suggest the top 5 and bottom 5 drugs for various medical conditions. Duplicate data is removed to ensure data accuracy.

### Functionality
1. **Data Cleaning**: Remove duplicate values for accurate recommendations.
2. **Stopwords Removal**: Exclude common stopwords for efficient text processing.
3. **Recommendation Generation**: Generate recommendations based on sentiment analysis.

## How to Use
1. Clone this repository to your local machine.
2. Install the required dependencies `nltk==3.6.3`.
3. Download NLTK stopwords using `nltk.download('stopwords')`.
4. Run the code to perform sentiment analysis and generate drug recommendations.

Feel free to customize the code to suit your specific requirements. If you encounter any issues or have questions, refer to the documentation or contact me.

Happy analyzing and recommending!

