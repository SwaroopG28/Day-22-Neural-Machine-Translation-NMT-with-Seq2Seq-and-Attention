# Neural Machine Translation (NMT) with Seq2Seq and Attention

## **Overview**
This project demonstrates how to build a **Neural Machine Translation (NMT)** system using a **Sequence-to-Sequence (Seq2Seq)** model with an LSTM-based encoder-decoder architecture. The model is trained to translate simple sentences from **English** to **French**. 

---

## **Dataset**
This project uses a small custom dataset of English-to-French sentence pairs:

| **English**            | **French**          |
|-------------------------|---------------------|
| hello                  | bonjour             |
| how are you            | comment ça va       |
| good morning           | bonjour             |
| thank you              | merci               |
| good night             | bonne nuit          |
| see you later          | à bientôt           |
| i love you             | je t'aime           |

Feel free to expand this dataset to improve the model's performance.

---

## **Model Architecture**
1. **Encoder**:
   - Converts input English sentences into fixed-size context vectors.
   - Layers:
     - Embedding Layer: Maps input tokens to dense vector representations.
     - LSTM Layer: Processes sequences and outputs context vectors (hidden and cell states).
2. **Decoder**:
   - Uses context vectors from the encoder to generate French translations.
   - Layers:
     - Embedding Layer: Maps target tokens to dense vector representations.
     - LSTM Layer: Generates predictions one token at a time.
     - Dense Layer: Applies a softmax activation to output probabilities for each token.
3. **Training Objective**:
   - The model is trained to minimize categorical cross-entropy loss using teacher forcing.
