<h1 align="center"> 🌟 Customer Rating Prediction 🌟 </h1>
<p align="center">using <b>SAS Enterprise Miner 🖥⛏</b><br><br>
.: 📄 Dataset taken from <b><a href="https://www.kaggle.com/mrmorj/big-mart-sales"> Kaggle </a></b> :.
</p><br>
<p align="center">
  <img src="https://img.shields.io/static/v1?label=%F0%9F%8C%9F&message=If%20Useful&style=style=flat&color=BC4E99" alt="Star Badge"/>
  <a href="https://www.github.com/caesarmario">
    <img src="https://img.shields.io/github/followers/caesarmario?style=social&link=https://www.github.com/caesarmario" alt"GitHub"/>
  </a>
  <a href="https://linktr.ee/caesarmario_">
    <img src="https://img.shields.io/badge/Follow%20My%20Other%20Works-019875?style=flat&labelColor=019875&link=https:/linktr.ee/caesarmario_" alt"Linktree"/>
  </a>
</p>
<br>

## 📃 Table of Contents:
  - [About Project](#-about-project)
  - [Objectives](#-objectives)
  - [Data Set Description](#-data-set-description)
  - [Process Flow](#-process-flow)
  - [Initial Data Exploration](#-initial-data-exploration)
  - [Data Pre-processing](#-data-pre-processing)
  - [EDA](#-eda)
  - [Model Implementation](#-model-implementation)
      - [Data Preparation](#-data-preparation)
      - [Experiment Preparation](#-experiment-preparation)
      - [Linear Regression](#-linear-regression)
      - [Neural Network](#-neural-network)

## 🖋 About Project:
*   This project is to predict customer rating using SAS Enterprise Miner.
*   This repository also contain initial data exploration, data transformation, and EDA of dataset.
*   The models used in SAS EM are:
    - Linear regression
    - Neural network
<br><br>

## 📌 Objectives:
*   Perform intial data exploration, data transformation, EDA, and implement linear regression and neural network with SAS EM.
<br><br>

## 🧾 Data Set Description:
* The dataset description can be seen [here](https://www.kaggle.com/aungpyaeap/supermarket-sales)
<br><br>

## ⚙ Process Flow
![EM Flow](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/01%20-%20EM%20Process%20Flow.png)

[![](https://img.shields.io/badge/back%20to%20top-%E2%86%A9-blue)](#-table-of-contents)
<br><br>

## 📊 Initial Data Exploration
![IDA](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/02%20-%20Initial%20Data%20Exploration.png)
   - There are no missing values detected for character and numerical columns.
   - However, the skewness for Tax_5%, Total, cogs, and gross_income have right-skewed distribution. <br>

![Pearson Corr](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/03%20-%20Pearson%20Correlation%20Statistics.png)
   - All continuous variables in the dataset do not correlate with the rating because the correlation value is close to 0 even though the correlation value is negative. <br>

![Statistical Exploration](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/04%20-%20Statistical%20Exploration.png)
   - This node will explore variables that can not entered StatExplore node.
   - It can be seen that the four variables do not have missing values in the dataset.
   - The minimum, maximum, and mean values in gross margin percentage have the same value, namely 4.761905 (it happens since it has same values for all observations). <br>

![Pearson Corr](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/03%20-%20Pearson%20Correlation%20Statistics.png)
   - All continuous variables in the dataset do not correlate with the rating because the correlation value is close to 0 even though the correlation value is negative. <br>

[![](https://img.shields.io/badge/back%20to%20top-%E2%86%A9-blue)](#-table-of-contents)
<br><br>

## 🛠 Data Pre-processing
### ▶ Data Transformation
![DT Config](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/05%20-%20Data%20Transformation%20Config.png)
   - Configuration of dtata transformation node.<br>

![DT Output](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/06%20-%20Data%20Transformation%20Output.png)
   - Data transformation output.
   - The skewness value of the new variables has a skewness value of < 0.5, means that the distribution of these variables is normal.<br>

### ▶ Dropping Variables
![Dropping Variables](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/07%20-%20Dropping%20Variables%20Config.png)
   - Dropping some variables in the dataset.<br>

[![](https://img.shields.io/badge/back%20to%20top-%E2%86%A9-blue)](#-table-of-contents)
<br><br>

## 📈 EDA
### 1️⃣ Payment Type based on Branch
![EDA 1](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/08%20-%20EDA%201.png)

### 2️⃣ Customer Type based on Gender
![EDA 2](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/09%20-%20EDA%202.png)

### 3️⃣ Average Rating based on Branch
![EDA 3](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/10%20-%20EDA%203.png)

### 4️⃣ Average Transformed Total based on Product Line
![EDA 4](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/11%20-%20EDA%204.png)

### 5️⃣ Average Transformed Gross Income based on Branch
![EDA 5](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/12%20-%20EDA%205.png)

[![](https://img.shields.io/badge/back%20to%20top-%E2%86%A9-blue)](#-table-of-contents)
<br><br>

## 🔨 Model Implementation
### 🪓 Data Preparation
![Data Preparation Config](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/13%20-%20Data%20Partition%20Node%20Conifguration.png)
   - The dataset split into 70% train, 15% validation, and 15% test.<br>

![Data Preparation Output](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/14%20-%20Output%20of%20Data%20Partition%20Node.png)

### 🧪 Experiment Preparation
*   Table below shows the experiment that will be implemented for each model:
<table>
<thead>
  <tr>
    <th>No.</th>
    <th>Experiment</th>
    <th>Details</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td colspan="3">Linear Regression</td>
  </tr>
  <tr>
    <td>1.</td>
    <td>None</td>
    <td>-</td>
  </tr>
  <tr>
    <td>2.</td>
    <td>Forward Model</td>
    <td>-</td>
  </tr>
  <tr>
    <td>3.</td>
    <td>Stepwise Model</td>
    <td>-</td>
  </tr>
  <tr>
    <td>4.</td>
    <td>Backward Model</td>
    <td>-</td>
  </tr>
  <tr>
    <td colspan="3">Neural Network</td>
  </tr>
  <tr>
    <td>5.</td>
    <td>Generalized Linear Model</td>
    <td>Number of hidden units: -<br>Max Iterations: 100</td>
  </tr>
  <tr>
    <td>6.</td>
    <td>Multilayer Perceptron 1</td>
    <td>Number of hidden units: 2<br>Max Iterations: 100</td>
  </tr>
  <tr>
    <td>7.</td>
    <td>Multilayer Perceptron 2</td>
    <td>Number of hidden units: 4<br>Max Iterations: 200</td>
  </tr>
  <tr>
    <td>8.</td>
    <td>Multilayer Perceptron 3</td>
    <td>Number of hidden units: 8<br>Max Iterations: 300</td>
  </tr>
</tbody>
</table>

[![](https://img.shields.io/badge/back%20to%20top-%E2%86%A9-blue)](#-table-of-contents)
<br><br>

### 📏 Linear Regression
#### 1️⃣📏 Standard Linear Regression
![Standard LR](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/15%20-%20Standard%20LR.png)<br>
![ANOVA Standard LR](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/16%20-%20ANOVA%20Standard%20LR.png)
   - RMSE value for training is 1.73, for validation is 1.712, whereas the RMSE value for testing is 1.746.
   - The p-value from ANOVA table is 0.9250 (> 0.05), which can be concluded that the independent variables do not exhibit a statistically significant connection with the dependent variable, or the independent variables do not predict the dependent variable dependably.
   - The value of R-square is 0.0180, which means this result shows that the independent variable can be used to predict just 1.8% of the variation in ratings (dependent variable).<br>

#### 2️⃣📏 Forward Linear Regression
![Forward LR](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/18%20-%20Forward%20LR.png)<br>
![ANOVA Forward LR](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/17%20-%20ANOVA%20Forward%20LR.png)
   - The RMSE value for training is 1.71, for validation is 1.733, whereas the RMSE value for testing is 1.723.
   - The p-value and r-square obtained error or did not appear.<br>

#### 3️⃣📏 Stepwise Linear Regression
![Stepwise LR](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/19%20-%20Stepwise%20LR.png)<br>
![ANOVA Stepwise LR](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/20%20-%20ANOVA%20Stepwise%20LR.png)
   - RMSE value for training is 1.71, for validation is 1.733, whereas the RMSE value for testing is 1.723.
   - The p-value and r-square obtained error or did not appear.<br>

#### 4️⃣📏 Backward Linear Regression
![Backward LR](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/21%20-%20Backward%20LR.png)<br>
![ANOVA Backward LR](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/22%20-%20ANOVA%20Backward%20LR.png)
   - RMSE value for training is 1.71, for validation is 1.733, whereas the RMSE value for testing is 1.723.
   - There are 15 steps performed in this model, and based on the resulting p-value, there are no independent variables that affect the rating value (dependent variable) since the p-value is more than 0.05.
   - The p-value and r-square obtained error or did not appear.<br>

#### 👀📏 Linear Regression Summary
![Summary LR](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/23%20-%20Comparison%20LR.png)

[![](https://img.shields.io/badge/back%20to%20top-%E2%86%A9-blue)](#-table-of-contents)
<br><br>

### 🕸 Neural Network
#### 1️⃣🕸 Generalized Linear Model
![GLM](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/24%20-%20Generalized%20Linear%20Model_NN.png)<br>
![Iteration Plot - GLM](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/25%20-%20Iteration%20Plot_Generalized%20Linear%20Model_NN.png)<br>
![Opt Result - GLM](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/26%20-%20Optimization%20Results_Generalized%20Linear%20Model_NN.png)
   - RMSE value for training is 1.73, for validation is 1.731, whereas the RMSE value for testing is 1.743.
   - There is only one iteration with the initial RMSE train 1.739708 and ending at 1.729611
   - The initial RMSE validation is 1.732672 and ends at 1.731434. <br>

#### 2️⃣🕸 Multilayer Perceptron 1 (2 Hidden Units, Iterations 100)
![MLP1](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/27%20-%20Multilayer%20Perceptron_NN.png)<br>
![Iteration Plot - MLP1](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/28%20-%20Iteration%20Plot_Multilayer%20Perceptron_NN.png)<br>
![Opt Result - MLP1](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/29%20-%20Optimization%20Results_Multilayer%20Perceptron_NN.png)
   - RMSE value for training is 1.77, for validation is 1.730, whereas the RMSE value for testing is 1.721.
   - There were 96 iterations in this model with the initial RMSE train of 1.771294 and continued to decrease to 1.65361
   - The initial RMSE validation value is 1.732672 and continues to increase to 1.893184 (overfitting). 
   - The best iteration is the first iteration with RMSE training, which is 1.768396, and RMSE validation is 1.730018. <br>

#### 3️⃣🕸 Multilayer Perceptron 3 (8 Hidden Units, Iterations 300)
![MLP2](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/30%20-%20Multilayer%20Perceptron_NN2.png)<br>
![Iteration Plot - MLP2](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/31%20-%20Iteration%20Plot_Multilayer%20Perceptron_NN2.png)<br>
![Opt Result - MLP2](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/32%20-%20Optimization%20Results_Multilayer%20Perceptron_NN2.png)
   - RMSE value for training is 1.83, for validation is 1.731, whereas the RMSE value for testing is 1.723.
   - There were 146 iterations in this model with the initial RMSE train of 1.833963 and continued to decrease to 1.614349.
   - The initial RMSE validation value is 1.732672 and continues to increase to 1.877191 (overfitting).
   - The best iteration is the first iteration with RMSE training is 1.828181, and for RMSE validation is 1.730597. <br>

#### 4️⃣🕸 Multilayer Perceptron 2 (4 Hidden Units, Iterations 200)
![MLP3](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/33%20-%20Multilayer%20Perceptron_NN3.png)<br>
![Iteration Plot - MLP3](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/34%20-%20Iteration%20Plot_Multilayer%20Perceptron_NN3.png)<br>
![Opt Result - MLP3](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/35%20-%20Optimization%20Results_Multilayer%20Perceptron_NN3.png)
   - RMSE value for training is 1.98, for validation is 1.724, whereas the RMSE value for testing is 1.725.
   - There were 189 iterations in this model with the initial RMSE train of 1.982259 and continued to decrease to 1.464764.
   - The initial RMSE validation value is 1.732672 and continues to increase to 2.169641.
   - The best iteration is the first iteration with RMSE training, which is 1.976888 and RMSE validation, which is 1.72416. <br>

#### 👀🕸 Neural Network Summary
![Summary NN](https://github.com/caesarmario/customer-rating-prediction-using-SAS-Enterprise-Miner/blob/main/Screenshot/36%20-%20Comparison%20NN.png)

[![](https://img.shields.io/badge/back%20to%20top-%E2%86%A9-blue)](#-table-of-contents)
<br><br>

## 🙌 Support me!

👉 If you find this project useful, **please ⭐ this repository 😆**!
---

👉 _More about myself: <a href="https://linktr.ee/caesarmario_"> here </a>_
