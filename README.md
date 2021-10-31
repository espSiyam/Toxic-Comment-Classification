# Jigsaw Unintended Bias in Toxicity Classification

This is a kaggle competetion hosted by Jigsaw and google to identify toxic comments in online conversations. This is a addition to the previous Toxic Comment Classification Challenge which is to be more unbiased and diverse.

## Methodology: 
1. Data Cleaning: 
   * For the training “comment_text” and “target” features were relevant. 
    So, other columns are dropped.
    
    * For the training “comment_text” and “target” features were relevant. 
  So, other columns are dropped. 

2. Tokenizing and Embedding: 
    * The training and testing data is tokenized and padded to have same 
length. 
    * FastText and QuoraText embedding are combined, and fitted on 
tokenized dataset to create the embedding of the words.

3. Splitting the dataset: 
    * The tokenized input variable and target variable is splitted for training 
and testing.

4. Model Building: 
    * The model is built using Embedding layer, Bidirectional LSTM layer and 
Dense layer. 

5. Model training: 
    * The model is trained for 20 epoch with batch size of 248. 
    * Early stopping and Reduce Learning rate is used to stop overfitting. 
    * Model Checkpoint is used to save the best model.

## Result Analysis: 
* The training accuracy is: 0.9638 and loss is 0.0955 
* The validation accuracy is: 0.96380 and loss is 0.095541 
* The model seems converged well on the first epoch, the started 
overfitting. Reducing learning rate haven’t helped much.

**Accuracy Plot:**

![Accuracy](https://github.com/espSiyam/Toxic-Comment-Classification/blob/main/attachmet/accuracy.png)

**Loss Plot:**

![Loss](https://raw.githubusercontent.com/espSiyam/Toxic-Comment-Classification/main/attachmet/loss.png)

### Dependencies

* numpy
* pandas
* sklearn
* tensorflow
* matplotlib
* gensim
* tqdm
* operator
* gc

## Acknowledgments

* [Kaggle Competetion](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification)
