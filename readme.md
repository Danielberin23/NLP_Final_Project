# NLP Final Project: Analyzing Twitter Posts from Major News Websites

## Project Overview

This project is the final assignment for my Natural Language Processing (NLP) course. The project involves scraping, processing, and analyzing Twitter posts from four major news organizations: Reuters, The New York Times, The Washington Post, and CNN. The main objectives of this project are to process the collected tweets, identify trends, and generate text using both RNN and GPT models.

## Data Sources

The data for this project was scraped from the official Twitter accounts of the following news organizations:
- **Reuters** (@Reuters)
- **The New York Times** (@nytimes)
- **The Washington Post** (@washingtonpost)
- **CNN** (@CNN)

## Project Structure

### 1. Data Preprocessing
- **Text Cleaning**: The raw tweets were processed to remove noise such as URLs, mentions, hashtags, and special characters.
- **Tokenization**: The cleaned text was tokenized to break down the tweets into individual words or tokens.
- **Padding**: Sequences were padded to ensure uniform input lengths for the models.
- **Data Truncation**: The sequences were truncated to reduce memory usage and optimize model performance.

### 2. Summarization of Tweets
- **User-specific Summarization**: A custom summarization algorithm was implemented to generate summaries of tweets for each of the four news organizations.
- **Selected Users**: The summarization was specifically applied to tweets from Reuters, The New York Times, The Washington Post, and CNN.

### 3. Text Generation Models
- **Recurrent Neural Network (RNN) Model**:
  - Built using PyTorch.
  - A simple RNN architecture with embedding and dense layers was implemented.
  - The model was trained to predict the next word in a sequence based on the input text.
  - Example text generation was performed using the trained RNN model.

- **Generative Pre-trained Transformer (GPT) Model**:
  - Built using PyTorch.
  - A GPT architecture was employed for text generation.
  - The model was trained on the same processed tweets to generate contextually relevant text.
  - The text generation results were compared between the RNN and GPT models.

### 4. Memory Optimization
- **Data Generator**: A custom `DataGenerator` was implemented to manage memory usage during training, allowing the models to be trained on GPU without exceeding memory limits.
- **GPU Memory Management**: Techniques to flush GPU memory were utilized to prevent memory overflow and ensure efficient model training.

## Project Dependencies

- Python 3.x
- PyTorch
- Numpy
- NLTK
- TensorFlow (optional, if running TensorFlow-based code)
- Additional libraries as listed in `requirements.txt`

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Special thanks to the instructors and mentors of the NLP course for their guidance.
- The datasets used in this project were scraped from Twitter and are subject to Twitter's terms and conditions.
