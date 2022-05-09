CS598 Deep Learning 4 Healthcare Final Project
Connor Burken

Citation to the original paper:
Citation: Burger F, Neerincx MA, Brinkman W-P (2021) Natural language processing for cognitive therapy: Extracting schemas from thought records. 
PLoS ONE 16(10): e0257832. https://doi.org/10.1371/journal.pone.0257832

This Software is based on the following research repository. Link to the original paper’s repo:
https://data.4tu.nl/articles/dataset/Dataset_and_Analyses_for_Extracting_Schemas_from_Thought_Records_using_Natural_Language_Processing/16685347

Python Dependencies:
numpy
pandas
scipy
gensim
sklearn
statsmodels
tensorflow
tensorflow_hub 
tensorflow_text 
talos
keras
joblib 

Data download Instruction:
The raw data for this project can be downloaded from the repository above. 
The processed data is provided as part of this repository under Data/DatasetsForH1 folder
 - H1_test_labels.csv
 - H1_test_texts.csv
 - H1_train_labels.csv
 - H1_train_texts.csv
 - H1_validate_labels.csv
 - H1_validate_texts.csv

Preprocessing Code + Command:
The preprocessing code is provided as two R Scripts in the project:
data_preprocessing.R
R_Script_integrated_in_paper.R


Pretrained Models:
The code uses two pretrained models for the BERT embeddings:
BERT model selected           : https://tfhub.dev/tensorflow/small_bert/bert_en_uncased_L-4_H-512_A-8/1
Preprocess model auto-selected: https://tfhub.dev/tensorflow/bert_en_uncased_preprocess/3

Table of Results
