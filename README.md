<h1 align="center">IEEE-CIS Fraud Detection</h1>
</br>
<h3>Abstract: </h3>
<p>This project is inspired from IEEE-CIS Fraud Detection Kaggle competition, where we have to solve a binary classification to predict fraudulent transaction. The dataset is cleaned, feature engineered, modeling and ensembling is done.</p>
<h3>Methodology: </h3>
<ol>
  <li>Data Cleaning: </li>
    <ul>
      <li>The training and testing dataset is separated in transaction and identity. So the dataset is merged on TransactionID for training and testing.</li>
      <li>There are some mismatch in training and testing features. So, the columns of test dataset is renamed to match the columns of the training data.</li>
      <li>There are a lots of null value. The feature containing more the 100000 null value is removed.</li>
      <li>The null values of the feature containing less null values will be filled with mode values.</li>
      <li>Memory size is reduced by changing datatype to manage this large volume of data.</li>
    </ul>
  <li>Exploratory Data Analysis:</li>
    <ul>
      <li>Some EDA is done to make sense of the data.</li>
    </ul>
  <li>Feature Selection:</li>
    <ul>
      <li>Correlation is measured related to Fraud to find out the best feature.</li>
      <li>Features with less correlation is dropped from the dataset.</li>
      <li>Find out the best features from Kaggle public notebook and dropped the rest.</li>
    </ul>
  <li>Handling Class Imbalance:</li>
    <ul>
      <li>The dataset contains huge class imbalance issue. To tackle this issue, I’ve tried using Up-Sampling and Down-Sampling.</li>
    </ul>
  <li>Modeling:</li>
    <ul>
      <li>XGBoost and LightGBM seems gave the state of the art accuracy. So, finetuned hyper-parameter is used to train the dataset.</li>
    </ul>
  <li>Ensemble:</li>
    <ul>
      <li>Weighted Average ensemble is apply on two models prediction</li>
    </ul>
</ol>
<h3>Result Analysis: </h3>     
<ul>
  <li>Up-Sampling and Down-sampling cased the worst result. They were both 0.50 on public leaderboard.</li>
  <li>XGBoost model gave the best score which is 0.915064 but took too much time, around 25 mins 31 sec.</li>
  <li>LightGBM too way less time but score was also a bit less. Score on public leaderboard is 0.896678.</li>
  <li>Weighted average ensemble was applied on the models (XGBoost, LightGBM) but the score was still 0. 915064</li>
  <li>Important features selection + LightGBM score is: 0.939961</li>
</ul>
<h3>Conclusion: </h3>
<p>The 0.915064 score is satisfactory but definitely there is more room to improve. Better selection of feature, feature engineering, hyper parameter tuning and model ensemble methods will help to push the result.</p>
<br>
Dataset Link: https://drive.google.com/drive/folders/1T_EoinJML_VHEX55pujEz-Ld3-ytMo5T?usp=sharing <br>
Competetion link: https://www.kaggle.com/c/ieee-fraud-detection
