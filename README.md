# Masked-Language-Modeling-on-Code-with-BERT-for-Semantic-Code-Representations
This project aims to develop a transformer-based model for automatic source code AST (abstract syntax tree) classification using the BERT architecture.

## Data
The dataset contains preprocessed AST data for source code files. It has been split into training, validation and test splits stored in JSONL format files under Dataset/ast/. Each JSON object contains the tokenized and encoded AST along with labels. The data has been preprocessed and tokenized using the BERT tokenizer.

## Model
The model uses the pretrained BERT-base-uncased model from Transformers. It is fine-tuned on the AST classification task using the masked language modeling objective.

The key steps are:

Loading and tokenizing data

Creating PyTorch tensors and datasets

Defining data loaders

Initializing BERTForMaskedLM model

Training model on dataloaders

Evaluating on validation set

## Training
To train the model, run all cells in the Jupyter notebook. Training takes 1-2 hours on a GPU. The trained model weights are saved for later use.

## Evaluation
After training, the model can be evaluated on the test set to analyze performance. Various metrics like accuracy can be computed.
