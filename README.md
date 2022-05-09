# CS598 Deep Learning 4 Healthcare Final Project
## Connor Burken

### Citation to the original paper:
Citation: Burger F, Neerincx MA, Brinkman W-P (2021) Natural language processing for cognitive therapy: Extracting schemas from thought records. 
PLoS ONE 16(10): e0257832. https://doi.org/10.1371/journal.pone.0257832

### This Software is based on the following research repository. Link to the original paper’s repo:
https://data.4tu.nl/articles/dataset/Dataset_and_Analyses_for_Extracting_Schemas_from_Thought_Records_using_Natural_Language_Processing/16685347

### Python Dependencies:
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

### Data download Instruction:
The raw data for this project can be downloaded from the repository above. 
The processed data is provided as part of this repository under Data/DatasetsForH1 folder
 - H1_test_labels.csv
 - H1_test_texts.csv
 - H1_train_labels.csv
 - H1_train_texts.csv
 - H1_validate_labels.csv
 - H1_validate_texts.csv

### Preprocessing Code:
The preprocessing code is provided as two R Scripts in the project:
data_preprocessing.R
R_Script_integrated_in_paper.R

### Pretrained Models:
GLoVE Vector Embeddings:
glove.6B.100d.txt (can be downloaded from original repository)

The code uses two pretrained models for the BERT embeddings:
BERT model selected           : https://tfhub.dev/tensorflow/small_bert/bert_en_uncased_L-4_H-512_A-8/1
Preprocess model auto-selected: https://tfhub.dev/tensorflow/bert_en_uncased_preprocess/3

### Table of Results
Original Results:
| Schema            | kNN-C          | kNN-R         | SVM           | SVR           | per-Schema RNN | per-Schema RNN |
| ----------------- |:--------------:|:-------------:|:-------------:|:-------------:|:--------------:|:--------------:|
| Attach            | 0.55           |0.63           |0.65           |0.68           | 0.73           | 0.69           |
| Competence        | 0.69           |0.66           |0.68           |0.64           | 0.76           | 0.66           |
| Glob Self-Eval    | 0.40           |0.41           |0.36           |0.49           | 0.58           | 0.49           |
| Health            | 0.74           |0.53           |0.73           |0.35           | 0.75           | 0.35           |
| Power & Control   | 0.11           |0.23           |NaN            |0.31           | 0.28           | 0.31           |
| Meta-Cognition    | NaN            |0.10           |NaN            |0.11           | -0.01          | 0.11           |
| Oth. People       | 0.28           |0.24           |NaN            |0.19           | 0.22           | 0.16           |
| Hopelessness      | 0.48           |0.51           |0.49           |0.54           | 0.63           | 0.53           |
| Oth. View on Self | 0.45           |0.46           |0.48           |0.52           | 0.58           | 0.50           |

Reproduced Results:
| Schema            | kNN-C          | kNN-R         | SVM           | SVR           | per-Schema RNN | per-Schema RNN |
| ----------------- |:--------------:|:-------------:|:-------------:|:-------------:|:--------------:|:--------------:|
| Attach            | 0.55           |0.63           |0.65           |0.68           | 0.73           | 0.69           |
| Competence        | 0.69           |0.66           |0.68           |0.64           | 0.76           | 0.66           |
| Glob Self-Eval    | 0.40           |0.41           |0.36           |0.49           | 0.58           | 0.49           |
| Health            | 0.74           |0.53           |0.73           |0.35           | 0.75           | 0.35           |
| Power & Control   | 0.11           |0.23           |NaN            |0.31           | 0.28           | 0.31           |
| Meta-Cognition    | NaN            |0.10           |NaN            |0.11           | -0.01          | 0.11           |
| Oth. People       | 0.28           |0.24           |NaN            |0.19           | 0.22           | 0.16           |
| Hopelessness      | 0.48           |0.51           |0.49           |0.54           | 0.63           | 0.53           |
| Oth. View on Self | 0.45           |0.46           |0.48           |0.52           | 0.58           | 0.50           |


BERT Results:
| Schema            | kNN-C          | kNN-R         | SVM           | SVR           | per-Schema RNN | per-Schema RNN |
| ----------------- |:--------------:|:-------------:|:-------------:|:-------------:|:--------------:|:--------------:|
| Attach            | 0.53           |0.53           |0.58           |0.66           | 0.74           | NaN            |
| Competence        | 0.59           |0.60           |0.69           |0.67           | 0.77           | NaN            |
| Glob Self-Eval    | 0.38           |0.40           |0.37           |0.51           | 0.57           | NaN            |
| Health            | 0.50           |0.41           |0.56           |0.31           | 0.75           | NaN            |
| Power & Control   | 0.10           |0.20           |-0.01          |0.31           | 0.21           | NaN            |
| Meta-Cognition    | NaN            |0.04           |NaN            |0.14           | 0.18           | NaN            |
| Oth. People       | 0.18           |0.14           |NaN            |0.11           | 0.18           | NaN            |
| Hopelessness      | 0.49           |0.46           |0.52           |0.52           | 0.64           | NaN            |
| Oth. View on Self | 0.40           |0.44           |0.47           |0.49           | 0.62           | NaN            |
