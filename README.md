# TED Talk NLP Temporal Analysis

This repository contains a comprehensive Natural Language Processing (NLP) analysis of TED Talk transcripts, examining linguistic patterns and topics over time. The project uses multiple approaches including Latent Dirichlet Allocation (LDA), BERTopic, and rhetorical analysis to understand how TED Talks have evolved from 2008 onwards.

## Overview

This project analyzes the TED Ultimate Dataset containing thousands of TED Talk transcripts. The analysis explores:

- **Topic Evolution**: How topics discussed in TED Talks have changed over time using both LDA and BERTopic approaches
- **Rhetorical Features**: Linguistic patterns including pronoun usage, sentence structure, laughter, and punctuation
- **Temporal Trends**: Year-over-year changes in speaking style and content focus

## Dataset

The project uses the **TED Ultimate Dataset** from Kaggle, containing:
- Complete transcripts of TED Talks
- Metadata including recording dates, speaker information, and talk details
- Covers TED Talks from 2008 to 2019/2020

The dataset is automatically downloaded using the Kaggle Hub Python library during notebook execution.

## Project Structure

```
TedTalkNLP/
├── Code/
│   ├── TedTalkNLP_EDA_LDA.ipynb          # Exploratory Data Analysis and LDA topic modeling
│   ├── TedTalkNLP_BERTopic.ipynb         # Advanced topic modeling using BERTopic
│   ├── TedTalkNLP_Rhetoric.ipynb         # Rhetorical and linguistic analysis
│   └── TedTalkNLP_EDA_LDA.html           # Rendered HTML output of EDA/LDA analysis
├── Write-ups/
│   ├── NLP Final Project Progress Report.pdf   # Project progress documentation
│   └── NLP Project Proposal.docx                # Initial project proposal
└── README.md                              # This file
```

## Notebooks

### 1. TedTalkNLP_EDA_LDA.ipynb
**Exploratory Data Analysis & Latent Dirichlet Allocation (LDA)**

This notebook performs:
- Initial data exploration and visualization of talk distribution by year
- Text preprocessing (lowercasing, punctuation removal, stopword filtering)
- LDA topic modeling to identify themes in TED Talks
- Coherence analysis to evaluate model quality
- Temporal visualization of topic emergence and dominance
- Interactive pyLDAvis visualizations for topic exploration

**Key Outputs:**
- Topic distributions across talks and years
- Coherence scores for LDA model validation
- Temporal trends in topic prevalence

### 2. TedTalkNLP_BERTopic.ipynb
**Advanced Topic Modeling with BERTopic**

This notebook implements:
- BERTopic (BERT-based topic modeling) for more semantic understanding
- Sentence transformers for embedding generation
- Custom vectorizer configuration with n-grams
- Comparison with traditional LDA approaches
- Dynamic topic modeling across time periods
- Topic representation refinement

**Key Features:**
- Leverages transformer-based embeddings for better semantic understanding
- Automatic topic identification and labeling
- Reduced dependency on manual stopword tuning compared to LDA
- Enhanced topic coherence and interpretability

### 3. TedTalkNLP_Rhetoric.ipynb
**Rhetorical & Linguistic Analysis**

This notebook analyzes speaking patterns including:

**Pronoun Usage:**
- First-person singular (I, me, my, mine, myself)
- First-person plural (we, us, our, ours, ourselves)
- Second-person (you, your, yours, yourself, yourselves)
- Pronoun rates calculated per 1,000 words for normalization

**Linguistic Features:**
- Sentence length and complexity metrics
- Punctuation patterns (questions, exclamations)
- Laughter occurrences and frequency
- Number-to-word ratios
- Word choice patterns

**Temporal Analysis:**
- Year-by-year trends in rhetorical devices
- Speaker engagement indicators
- Changes in presentation style over time
- Correlation between linguistic features and talk characteristics

## Technical Stack

### Core Libraries
- **pandas** - Data manipulation and analysis
- **scikit-learn** - Machine learning and feature extraction
- **nltk** - Natural language processing toolkit
- **gensim** - Topic modeling (LDA)
- **bertopic** - Transformer-based topic modeling
- **sentence-transformers** - Semantic embeddings
- **spacy** - Advanced NLP processing

### Visualization
- **matplotlib** - Basic plotting
- **pyLDAvis** - Interactive topic model visualization

### Data Access
- **kagglehub** - Automated dataset download from Kaggle

## Getting Started

### Prerequisites

- Python 3.8+
- pip or conda package manager
- Kaggle API credentials (for dataset download)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/emilyedono/TEDTalkNLP.git
cd TedTalkNLP
```

2. Install required packages:
```bash
pip install pandas scikit-learn nltk gensim bertopic sentence-transformers spacy pyLDAvis kagglehub matplotlib jupyter
```

3. Download required spacy model:
```bash
python -m spacy download en_core_web_sm
```

4. Set up Kaggle credentials for dataset download (see Kaggle documentation)

### Running the Analysis

Navigate to the `Code/` directory and open notebooks in Jupyter:

```bash
cd Code
jupyter notebook
```

Then open and run the notebooks in this order:
1. `TedTalkNLP_EDA_LDA.ipynb` - Start with data exploration
2. `TedTalkNLP_BERTopic.ipynb` - Explore semantic topic modeling
3. `TedTalkNLP_Rhetoric.ipynb` - Analyze rhetorical patterns

## Key Findings

### Topic Evolution (LDA)
- Consistent presence of technology and innovation themes
- Emergence of social and personal development topics over time
- Evolution of business and leadership discussions
- Growth in discussions of global challenges and sustainability

### Topic Insights (BERTopic)
- More nuanced and semantically meaningful clusters than traditional LDA
- Better identification of cross-cutting themes
- Clearer temporal patterns in topic emergence

### Rhetorical Patterns
- Variations in pronoun usage reflecting speaker approach (personal vs. collective narratives)
- Trends in sentence structure and complexity
- Changes in engagement techniques (questions, laughter) over years
- Linguistic adaptation of speakers to audience expectations

## Methodology

### Text Preprocessing
- Conversion to lowercase
- Removal of non-alphanumeric characters
- Custom stopword removal for improved topic coherence
- Tokenization and vectorization

### Topic Modeling Approaches
1. **LDA (Latent Dirichlet Allocation)**
   - Probabilistic generative model
   - Interpretable topic distributions
   - Good baseline for comparison

2. **BERTopic**
   - Neural embedding-based approach
   - Semantic understanding via transformers
   - Better capture of contextual relationships

### Rhetorical Analysis
- Quantitative measurement of linguistic features
- Normalization to handle variable talk lengths
- Temporal aggregation for trend analysis
- Statistical comparison across time periods

## Future Enhancements


- Sentiment analysis across topics and time
- Rhetorical analysis across topics
- Audience engagement metrics integration


## Author

Emily Donofrio


