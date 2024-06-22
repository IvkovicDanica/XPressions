# XPressions: Emotion Classification from Tweets

[Emotions Dataset](https://www.kaggle.com/datasets/nelgiriyewithana/emotions/data) – a curated collection of English Twitter messages annotated with six primary emotions: anger, fear, joy, love, sadness, and surprise. This dataset serves as a valuable resource for analyzing emotional expressions in short-form text on social media platforms.

## About the Dataset

Each entry in this dataset includes:
- **text**: A string feature representing the content of a Twitter message.
- **label**: A classification label indicating the predominant emotion, with values ranging from 0 to 5 corresponding to sadness, joy, love, anger, fear, and surprise respectively.

## Sample Data

| text                                                | label |
|-----------------------------------------------------|-------|
| that was what i felt when i was finally accept…     | 1     |
| i take every day as it comes i'm just focussin…     | 4     |
| i give you plenty of attention even when i fee…     | 0     |

## Modeling

In this project, we employed various machine learning models to classify emotions from Twitter messages. Below are the models utilized and their descriptions:

- **LSTM with PyTorch**
  - **Description**: Long Short-Term Memory (LSTM) networks implemented using PyTorch to capture long-range dependencies in text sequences.
  - **Usage**: LSTM models were trained on the Emotions dataset to understand sequential patterns and classify tweets into one of six emotion categories.

- **DeBERTa v3 with Hugging Face Transformers**
  - **Description**: State-of-the-art transformer-based model from Hugging Face Transformers library, specifically DeBERTa v3, fine-tuned on the emotions classification task.
  - **Integration**: Leveraged pre-trained DeBERTa v3 model and fine-tuned it on the Emotions dataset to utilize bidirectional contextual embeddings for accurate emotion prediction.

- **XLNet with Hugging Face Transformers**
  - **Description**: XLNet is another transformer-based model that overcomes limitations of traditional transformers by leveraging permutation language modeling.
  - **Advantages**: XLNet captures bidirectional dependencies more effectively than traditional transformers, offering enhanced understanding of context in text sequences.
  - **Implementation**: Integrated XLNet from Hugging Face Transformers library, fine-tuned on the Emotions dataset to explore its effectiveness in emotion classification tasks.

Each model was evaluated using standard metrics such as accuracy, precision, recall, and F1-score to assess its performance in predicting emotions from tweets.
