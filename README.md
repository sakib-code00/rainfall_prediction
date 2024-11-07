<h1>Rainfall Prediction Poject</h1>
<section id="sec1">
  <h2>Project Overview</h2>
  <p>This project focuses on creating a machine-learning model to help predict and classify different weather conditions, using a dataset with weather information from Sylhet, Bangladesh. By analyzing patterns in data like temperature, humidity, pressure, and precipitation, the model aims to identify and classify weather conditions (e.g., sunny, rainy, or foggy).</p>
</section>
<h2>Table of Content</h2>
<ul>
  <li><a href="#sec1">Project Overview</a></li>
  <li><a href="#sec2">Data Description</a></li>
  <li><a href="#sec3">Data Processing</a></li>
  <li><a href="#sec4">Exploratory Data Analysis</a></li>
  <li><a href="#sec5">Handling Imbalanced Data</a></li>
  <li><a href="#sec6">Model Selection</a></li>
  <li><a href="#sec7">Training and Evaluation</a></li>
  <li><a href="#sec8">Confusion Matrix and Classification Report</a></li>
  <li><a href="#sec9">Future work</a></li>
  <li><a href="#sec10">Conclusion</a></li>
  <li><a href="#sec11">Data Source</a></li>
    
</ul>
<section id="sec2">
  <h2>Data Descriptions</h2>
  <p>The dataset is a collection of weather observations from Sylhet in 2023. Key features include:</p>
  <ul>
    <li><b>Temperature (tempmax, tempmin, temp):</b> Maximum, minimum, and current temperature.</li>
    <li><b>Humidity:</b> Measures the moisture in the air.</li>
    <li><b>Precipitation Type (preciptype)</b>: Type of precipitation recorded, which is our target variable.</li>
    <li><b>Pressure:</b> Atmospheric pressure in the region.</li>
    <li><b>Visibility:</b> Measure of the clarity of the atmosphere.</li>
    <li><b>Wind Speed:</b> Speed of wind, which can influence weather patterns.</li>
  </ul>
  <p>The target variable, preciptype, represents various weather types we aim to classify.</p>
</section>
<section id="sec3">
  <h2>Data Processing</h2>
  <p>We conducted several preprocessing steps to prepare the data for machine learning:</p>
  <ol type="a">
    <li>Checked for missing data and applied techniques to fill or drop missing entries to maintain data integrity.</li>
    <li>Removed irrelevant or highly correlated columns (e.g., tempmax and tempmin after ensuring temp was representative).</li>
    <li>Converted categorical variables into numerical values to enable machine learning algorithms to process them.</li>
    <li> Standardized the numerical features to ensure all features contributed equally to the model's performance.</li>
  </ol>
</section>
<section id="sec4">
  <h2>Exploratory Data Analysis</h2>
  <p> Visualized the data to understand trends and relationships among variables:</p>
  <ul>
    <li>Used histograms and box plots to check feature distributions and detect outliers.</li>
    <li>Generated a heatmap to explore correlations, ensuring features were independent enough to contribute unique information to the model.</li>
    <li>Visualized the target variable preciptype to address the issue of imbalanced classes, as certain weather types were more frequent.</li>
  </ul>
</section>
<section id="sec5">
  <h2>Handling Imbalanced Data</h2>
  <p>Since some weather types were underrepresented, used Random Oversampling to balance the dataset.<br/> This technique involved oversampling the minority classes to ensure the model learned from all weather conditions equally.</p>
</section>
<section id="sec6">
  <h2>Model Selection</h2>
  <p>Tested several machine learning models to determine which algorithm performed best:</p>
  <ul>
    <li><b>Logistic Regression:</b> A simple model that uses probabilities for binary and multiclass classification.</li>
    <li><b>Support Vector Machine (SVM):</b> An algorithm that finds the optimal hyperplane to separate classes, effective for high-dimensional spaces.</li>
    <li><b>Random Forest:</b> An ensemble model that builds multiple decision trees and combines their outputs to improve accuracy and reduce overfitting.</li>
    <li><b>XGBoost:</b> A highly effective gradient boosting model, optimized for performance in machine learning competitions.</li>
  </ul>
</section>

<section id="sec7">
  <h2>Training and Evaluation</h2>
  <p>Split the data into training and validation sets to evaluate the models’ effectiveness. The following metrics were used:</p>
  <li>Accuracy: Measures the overall correctness of the model.</li>
  <li>ROC-AUC Score: Evaluates model performance, especially for imbalanced datasets.</li>
  <li>Confusion Matrix: Helps visualize the classification results and identify misclassifications.</li>
  <li>Classification Report: Provides detailed metrics like precision, recall, and F1-score for each class.</li>
  <h3>Model Training Results</h3>
  <p>The performance of each model is summarized below:</p>
  <table style="border: 1px solid black;">
    <tr>
      <th>Model</th>
      <th>Training ROC-AUC</th>
      <th>Validation ROC-AUC</th>
    </tr>
    <tr>
      <td>Logistic Regression</td>
      <td>0.87</td>
      <td>0.85</td>
    </tr>
    <tr>
      <td>Support Vector Machine</td>
      <td>0.91</td>
      <td>0.89</td>
    </tr>
    <tr>
      <td>Random Forest</td>
      <td>0.93</td>
      <td>0.91</td>
    </tr>
    <tr>
      <td>XGBoost</td>
      <td>0.95</td>
      <td>0.93</td>
    </tr>
  </table>
  
</section>

<section id="sec8">
  <h2>Confusion Matrix and Classification Report</h2>
</section>

<section id="sec9">
  <h2>Future Work</h2>
</section>

<section id="sec10">
  <h2>Conslusion</h2>
</section>

<section id="sec11">
  <h2>Data Source</h2>
</section>
