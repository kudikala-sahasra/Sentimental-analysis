# Sentimental-analysis
This project demonstrates how to train a sentiment analysis model using BERT and deploy it with Gradio in Google Colab. The project includes the following steps:

1. Data Preprocessing: The project uses the SMILE Twitter dataset to train a sentiment analysis model. The data is preprocessed to filter relevant categories and split into training and validation sets.

2. Model Training: The BERT model for sequence classification is fine-tuned on the training data. The model is trained for several epochs and performance metrics are evaluated.

3. Model Saving: The trained model and tokenizer are saved to a specified directory using the Hugging Face Transformers library.

4. Gradio Deployment: The saved model and tokenizer are loaded and used to deploy the sentiment analysis model with Gradio in Google Colab. This allows user input to be analyzed and sentiment labels to be predicted.
## Usage

1. Open the notebook `Sentiment_Analysis_with_BERT_and_Gradio.ipynb` in Google Colab.
2.  upload the dataset to google collab notebook

3. Run the notebook cells to preprocess the data, train the model, save the model, and deploy it with Gradio.

4. Follow the instructions in the notebook to interact with the deployed model using the Gradio interface.

## Requirements
- google collab
- Familiarity with BERT and sentiment analysis
- Hugging Face Transformers library
- Gradio library
