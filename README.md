# Neural Machine Translation (NMT) with Seq2Seq and Attention

## **Overview**
This project implements a **Neural Machine Translation (NMT)** system to translate simple sentences from **English** to **French** using a **Sequence-to-Sequence (Seq2Seq)** architecture with an **LSTM-based encoder-decoder model**. While this example uses a small custom dataset, the architecture can be extended to larger and more complex datasets like **European Parliamentary Proceedings Parallel Corpus** or **OpenSubtitles**.

---

## **How It Works**
1. **Encoder**:
   - Converts input English sentences into fixed-size context vectors using an LSTM network.
2. **Decoder**:
   - Uses the context vectors from the encoder to generate French translations word by word.
3. **Dataset**:
   - A small, custom English-to-French dataset with simple sentences.
4. **Training**:
   - The model is trained using teacher forcing with padded input sequences.
5. **Inference**:
   - During inference, the decoder generates the translation one token at a time using the context vector from the encoder.

