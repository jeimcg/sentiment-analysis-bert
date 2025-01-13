Lyric Sentiment Analysis with Fine-Tuned BERT
In this project, I explored the emotional undertones in song lyrics using advanced natural language processing (NLP) techniques. A fine-tuned BERT model (bert-tiny) was employed to classify lyrics into sentiment categories. This analysis integrates preprocessing workflows, sentiment labeling, training, and validation pipelines while extracting meaningful insights like word frequencies from the lyrics.

Authors
@jeimcg
Overview
Goal
To build a comprehensive pipeline for processing song lyrics, assigning sentiment labels, and fine-tuning a pre-trained BERT model for sentiment classification. Word frequency analysis is also conducted to deepen understanding of lyrical content.

Workflow
Data Cleaning and Preprocessing:
Remove noise (special characters, punctuation).
Normalize text (lowercase, tokenization).
Sentiment Labeling:
Assign sentiment labels using TextBlob and save labeled datasets.
Model Training:
Fine-tune a bert-tiny model on labeled data using training, validation, and test splits.
Performance Evaluation:
Validate the model with training, validation, and test metrics.
Word Frequency Analysis:
Analyze frequently used words to uncover linguistic trends.
Features
Sentiment Analysis: Identifies emotional tones in lyrics using a fine-tuned BERT model.
Data Preparation: Automates text cleaning and sentiment labeling for large datasets.
Word Frequency Analysis: Highlights common words in lyrics for further insights.
Training and Validation: Includes performance metrics to evaluate the model.
Findings
Training and validation losses stabilized over 3 epochs:
Final Training Loss: 0.0857
Final Validation Loss: 0.0810
Test Loss: 0.1074
Sentiment Predictions:
css
Copy code
[{'label': 'LABEL_0', 'score': 0.6137}, {'label': 'LABEL_0', 'score': 0.5820}]
Word frequency analysis reveals linguistic patterns and key terms.
Project Structure
plaintext
Copy code
lyric-sentiment-analysis/
│
├── notebooks/
│   ├── lyric_sentiment_analysis_pipeline.ipynb  # Main Colab workflow
│   ├── python_word_frequency_combined.ipynb    # Local word frequency analysis
│   └── txt_dataset_generation.ipynb            # Dataset creation for training
│
├── data/
│   ├── lyrics_with_labels.xlsx                 # Labeled dataset for training
│   ├── lyrics_dataset.txt                      # Preprocessed lyrics for tokenization
│   └── filtered_word_frequencies_pt2.xlsx      # Filtered word frequency results
│
├── models/
│   └── fine_tuned_tinybert/                    # Saved model and tokenizer
│
├── results/
│   ├── sentiment_analysis_results.xlsx         # Predicted sentiment labels
│   └── word_frequencies.xlsx                   # Word frequency results
│
├── requirements.txt                            # Python dependencies
├── .gitignore                                  # Ignored files and directories
└── README.md                                   # Project documentation
Setup Instructions
Clone the Repository
bash
Copy code
git clone https://github.com/<your-username>/lyric-sentiment-analysis.git
cd lyric-sentiment-analysis
Install Dependencies
bash
Copy code
pip install -r requirements.txt
Run the Colab Notebook
Open lyric_sentiment_analysis_pipeline.ipynb in Google Colab.
Upload the lyrics_with_labels.xlsx dataset.
Follow the notebook to:
Clean and preprocess the dataset.
Train and validate the fine-tuned BERT model.
Analyze results.
Acknowledgements
Thanks to:

Hugging Face Transformers for pre-trained models.
TextBlob for sentiment labeling.
Open-source communities for their tools and documentation.
Special appreciation for self-learning, persistence, and curiosity in data science and machine learning at age 24! 😊

Future Improvements
Expand dataset diversity for improved generalization.
Use a larger pre-trained BERT model for enhanced accuracy.
Add data augmentation for better handling of rare labels.
Deploy the model as an API or integrate into a web application.
