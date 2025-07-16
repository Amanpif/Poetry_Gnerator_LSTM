
# 📝 Poetry Generator using Deep Learning

A deep learning-based poetry generation model trained on a custom dataset of poems using LSTM/GRU networks. It learns the structure and patterns of poetic text and generates coherent verses based on input prompts.

---

## 📌 Features

- Text preprocessing and tokenization using `Tokenizer`
- Sequence generation for next-word prediction
- LSTM-based sequential model built using TensorFlow/Keras
- Generates original poetic stanzas
- Easily extendable for GRU or Transformer models

---

## 📁 Dataset

- Collected poems from a curated text file or corpus
- Preprocessing steps:
  - Lowercasing
  - Removing punctuations/special characters
  - Splitting into sequences of N words
  - Padding sequences for uniform input size

---

## 🧠 Model Architecture

```python
model = Sequential()
model.add(Embedding(vocab_size, 100, input_length=max_len-1))
model.add(LSTM(150, return_sequences=True))
model.add(Dropout(0.2))
model.add(LSTM(100))
model.add(Dense(vocab_size, activation='softmax'))
```

- **Loss**: Categorical crossentropy  
- **Optimizer**: Adam  
- **Evaluation**: Perplexity, manual review of generated outputs

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/poetry-generator.git
   cd poetry-generator
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter notebook:
   ```bash
   jupyter notebook Poetry_Generator.ipynb
   ```

4. Type a starting phrase and let the model complete the poem.


## 🛠 Requirements

- Python 3.7+
- TensorFlow / Keras
- NumPy
- Matplotlib
- Jupyter Notebook

---

## 📌 Future Work

- Use GRU and Transformer architectures
- Train on larger poetic corpora (e.g., Gutenberg, HaikuDB)
- Add rhyme schemes and syllable constraints
- Deploy via Gradio/Streamlit
