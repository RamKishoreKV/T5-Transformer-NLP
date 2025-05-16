# Text Summarization Using T5 Transformer

This project demonstrates the process of summarizing text using a pre-trained T5 Transformer model. It includes steps for model training, evaluation, and visualization of the results. The notebook also computes various metrics to evaluate the performance of the summarization model.

## Introduction

This project utilizes the T5 Transformer model to generate summaries of input texts. T5 (Text-To-Text Transfer Transformer) is a transformer model that converts every NLP problem into a text-to-text format. 

## Dataset

The dataset used for this project includes news articles with their respective summaries. 
After modifying the dataset we can get the - 
Each entry in the dataset contains:
- `text`: The original article text.
- `ctext`: The reference summary for the article.

## Model Training

The T5 Transformer model is fine-tuned on the pre-processed dataset. The `summarize` function takes an input text and generates a summary using the following steps:
1. Tokenizing the input text.
2. Generating the summary using the T5 model with beam search and other generation parameters.
3. Decoding the generated tokens into a readable summary.

## Evaluation Metrics

The performance of the summarization model is evaluated using the following metrics:
- BLEU: Measures the overlap of n-grams between the generated summary and the reference summary.
- ROUGE: Measures the overlap of words and sequences of words between the generated summary and the reference summary. Includes ROUGE-1, ROUGE-2, and ROUGE-L scores.

## Results

The results are presented as a dictionary containing the computed BLEU, ROUGE scores.

## Conclusion

The T5 Transformer model performs well in summarizing text, with high ROUGE and BLEU scores indicating good overlap between the generated and reference summaries. 


## How to Run

To run the notebook:
1. Ensure you have the necessary dependencies installed (`transformers`, `nltk`, `rouge`, `sklearn`, `lightning`).
2. Load the dataset into a pandas DataFrame.
3. Follow the steps in the notebook to preprocess the data, fine-tune the model, and evaluate its performance.
