# Sentiment Analysis - Product Reviews

## Project Overview
A Bidirectional LSTM neural network that classifies product
reviews as positive or negative sentiment.

## Dataset
- 30 product reviews (balanced: 15 positive, 15 negative)
- Train/test split: 80/20 with proper data leakage prevention

## Model Architecture
- Embedding layer (32 dimensions)
- Bidirectional LSTM (32 units) with return_sequences
- Bidirectional LSTM (16 units)
- Dense layer with Dropout regularization
- Sigmoid output for binary classification

## Results
- Training Accuracy: 100.00%
- Testing Accuracy: 83.33%
- Train-Test Gap: 16.67%

## Key Learnings
1. Data leakage prevention - tokenizer fit only on training data
2. Bidirectional LSTM captures context from both directions
3. Small datasets limit generalization (30 samples is minimal)
4. Proper train/test evaluation reveals true model performance

## Limitations
- Small dataset size limits real-world accuracy
- Production systems need thousands of labeled examples
- Model may struggle with sarcasm, complex negation

- Model achieved 100% training accuracy but 
failed to generalize on completely new sentences,
demonstrating overfitting despite reasonable 
test accuracy (83%). 
- Root cause: insufficient 
training data (24 samples) for LSTM model 
complexity. This highlights the importance of 
train-test gap monitoring beyond single metrics."

## Tools Used
- Python, TensorFlow/Keras
- LSTM, Bidirectional layers
- Tokenizer, text preprocessing

## Author
Kaviya V | github.com/kaviyavijayan11
