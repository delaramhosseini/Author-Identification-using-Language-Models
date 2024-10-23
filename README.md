# Author Identification in Persian Literature using Language Models

## Project Overview
This project focuses on the task of identifying authors in Persian literature by using fine-tuned BERT language models. The dataset comprises texts from 10 authors in the same genre, and the models are evaluated through 5-fold cross-validation, yielding various performance metrics. The project also compares the results with traditional machine learning techniques.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Experiments](#experiments)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Conclusion](#conclusion)

## Dataset
The dataset includes texts from 10 different Persian authors writing in the same genre. Each author has 30 documents, each containing exactly 500 words. Metadata includes:
- **Author Name**: The name of the author.
- **Text Content**: The 500-word document from the author.
- **Additional Information**: Any relevant metadata.

Dataset construction steps:
1. **Web Scraping**: Used `Beautiful Soup` in Python to scrape texts from online sources.
2. **Document Selection**: Selected 30 texts per author, ensuring genre and author diversity.
3. **Text Cleaning**: Processed the text to meet the 500-word limit and cleaned unnecessary characters.

## Model Architecture
The author identification task was carried out using various pre-trained BERT models from Hugging Face, specifically fine-tuned for this problem:
- **Pre-trained Model**: BERT-based models fine-tuned on our dataset.
- **Tokenization**: Used the built-in tokenizer for Persian text.
- **Fine-Tuning**: Modified the output layer for the classification task.

## Experiments
The models were trained and evaluated using **5-fold cross-validation**. Key experiments include:
1. **Model Performance**: Measured accuracy, F1 Score, precision, and recall for each model.
2. **Parameter Tuning**: Analyzed the impact of fine-tuning parameters (e.g., learning rate, batch size) on model performance.
3. **Document Length**: Investigated the effect of varying document lengths on accuracy.
4. **Stopword Removal**: Evaluated the impact of excluding stopwords on model performance.

## Results
The performance metrics for each experiment are summarized as follows:
- **Accuracy**: [Results]
- **F1 Score**: [Results]
- **Precision & Recall**: [Results]
- **Confusion Matrix**: Included in the report for detailed analysis.

Additionally, the project compares BERT’s performance with traditional machine learning models (e.g., SVM, Random Forest), highlighting the advantages and limitations of each approach.

## Installation
To set up the environment for this project, follow these steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/author-identification-persian
   cd author-identification-persian


2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up the environment for Hugging Face models:
   ```bash
   pip install transformers
   ```

## Usage
1. **Dataset Creation**:
   - Run the `dataset_creation.py` script to create the dataset:
     ```bash
     python dataset_creation.py
     ```
   - The dataset will be saved in the `/data` folder.

2. **Fine-Tuning BERT Model**:
   - Run the `fine_tune_bert.py` script to fine-tune the BERT model:
     ```bash
     python fine_tune_bert.py
     ```

3. **Model Evaluation**:
   - After training, run the evaluation script to obtain performance metrics:
     ```bash
     python evaluate_model.py
     ```

