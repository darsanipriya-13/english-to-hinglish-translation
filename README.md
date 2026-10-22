# English to Hinglish Machine Translation using LSTM

## 📌 Project Overview

This project aims to develop a machine translation system that converts English sentences into Hinglish (Hindi written using English/Roman letters). It uses a Sequence-to-Sequence (Seq2Seq) architecture with LSTM (Long Short-Term Memory) networks to learn sentence patterns and generate translations.

The project demonstrates how deep learning can support multilingual communication by translating English input into Hinglish output.

## 🎯 Objectives

- Load and preprocess paired English–Hinglish sentences.
- Tokenize both languages and build vocabularies.
- Convert sentences into numerical sequences and apply padding.
- Design an LSTM-based Seq2Seq Encoder–Decoder model.
- Train the model using teacher forcing.
- Evaluate translation quality using the BLEU score.
- Translate unseen English sentences into Hinglish.
- Provide an interactive interface for user-entered English sentences.

## 📂 Dataset

The project uses an English–Hinglish parallel sentence dataset.

**Original dataset:** [English-Hinglish Machine Translation Dataset on Kaggle](https://www.kaggle.com/datasets/yash9439/eng-hinglish-machine-translation/data)

A small Romanized English–Hinglish dataset may also be used for experimentation and demonstration.

Each data sample contains:
- **English:** Source sentence.
- **Hinglish:** Target sentence written using Roman letters.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Platform:** Google Colab
- **Deep Learning Framework:** PyTorch
- **Model Architecture:** Seq2Seq LSTM Encoder–Decoder
- **Data Processing:** Pandas, NumPy
- **Evaluation Metric:** BLEU Score
- **Visualization:** Matplotlib

## 🧠 Model Architecture

The system follows a Sequence-to-Sequence Encoder–Decoder architecture.

1. **Input Processing:** English sentences are cleaned and tokenized.
2. **Embedding Layer:** Converts token IDs into dense vector representations.
3. **LSTM Encoder:** Processes the English sequence and generates hidden and cell states.
4. **LSTM Decoder:** Uses the encoder states to generate Hinglish tokens sequentially.
5. **Output Generation:** Converts predicted token IDs back into a Hinglish sentence.

### Architecture Flow

```text
English Input Sentence
          |
          v
Tokenization and Padding
          |
          v
     Embedding Layer
          |
          v
      LSTM Encoder
          |
          v
   Hidden and Cell States
          |
          v
      LSTM Decoder
          |
          v
   Hinglish Output Sentence
```

## ⚙️ Training Process

The model is trained using the following components:

- **Loss Function:** Cross-Entropy Loss
- **Optimizer:** Adam
- **Training Strategy:** Teacher Forcing
- **Evaluation:** Validation loss and BLEU score

Teacher forcing helps the decoder learn by providing the correct previous target token during training with a specified probability.

## 🚀 How to Run the Project

1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new notebook.
3. Upload the dataset CSV file.
4. Run the notebook cells in order:
   - Dataset loading and preprocessing
   - Tokenization and vocabulary creation
   - Sequence padding
   - LSTM Encoder–Decoder implementation
   - Model training
   - BLEU evaluation
   - Interactive translation
5. Enter an English sentence when prompted.
6. View the generated Hinglish translation.

## 💬 Example

**Input:**
```text
How are you?
```

**Expected Hinglish-style output:**
```text
Tum kaise ho?
```

*The example shows the intended translation format. Actual model predictions may differ depending on training data and model performance.*

## 📊 Evaluation

Translation quality is evaluated using the BLEU (Bilingual Evaluation Understudy) score, which measures n-gram overlap between generated translations and reference translations.

The model is evaluated on a held-out test dataset. The actual BLEU score should be reported after running the experiment.

## 🔮 Future Improvements

- Increase the size and diversity of the parallel dataset.
- Improve spelling consistency in Romanized Hinglish.
- Experiment with attention mechanisms.
- Tune model hyperparameters to improve translation quality.
- Compare LSTM performance with Transformer-based translation models.
- Deploy the model using a web interface.

## 📌 Conclusion

This project demonstrates an end-to-end deep learning workflow for English-to-Hinglish machine translation using an LSTM-based Seq2Seq Encoder–Decoder. It covers data preprocessing, tokenization, vocabulary construction, model training, teacher forcing, BLEU evaluation, and interactive translation.

## 👩‍💻 Author

**Darsani priya RJ**

## 📄 License

This project is intended for educational and research purposes. Refer to the original dataset's license and terms of use before redistributing the dataset or using it in other projects.
