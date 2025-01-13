# **Lyric Sentiment Analysis with Fine-Tuned BERT**

In this project, I explored the emotional undertones in song lyrics using advanced natural language processing (NLP) techniques. A fine-tuned BERT model (`bert-tiny`) was employed to classify lyrics into sentiment categories. This analysis integrates preprocessing workflows, sentiment labeling, training, and validation pipelines while extracting meaningful insights like word frequencies from the lyrics.

## **Authors**
- [@jeimcg](https://www.github.com/jeimcg)

---

## **Overview**

### **Goal**
To build a comprehensive pipeline for processing song lyrics, assigning sentiment labels, and fine-tuning a pre-trained BERT model for sentiment classification. Word frequency analysis is also conducted to deepen understanding of lyrical content.

### **Workflow**
1. **Data Cleaning and Preprocessing**:
   - Remove noise (special characters, punctuation).
   - Normalize text (lowercase, tokenization).
2. **Sentiment Labeling**:
   - Assign sentiment labels using `TextBlob` and save labeled datasets.
3. **Model Training**:
   - Fine-tune a `bert-tiny` model on labeled data using training, validation, and test splits.
4. **Performance Evaluation**:
   - Validate the model with training, validation, and test metrics.
5. **Word Frequency Analysis**:
   - Analyze frequently used words to uncover linguistic trends.

---

## **Features**
- **Sentiment Analysis**: Identifies emotional tones in lyrics using a fine-tuned BERT model.
- **Data Preparation**: Automates text cleaning and sentiment labeling for large datasets.
- **Word Frequency Analysis**: Highlights common words in lyrics for further insights.
- **Training and Validation**: Includes performance metrics to evaluate the model.

---

## **Findings**
- **Training and validation losses stabilized over 3 epochs**:
  - Final Training Loss: 0.0857
  - Final Validation Loss: 0.0810
  - Test Loss: 0.1074
- **Sentiment Predictions**:
  ```python
  [{'label': 'LABEL_0', 'score': 0.6137}, {'label': 'LABEL_0', 'score': 0.5820}]
