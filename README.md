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
  <li><a href="#sec11">Visualization</a></li>
  <li><a href="#sec12">Data Source</a></li>
    
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
  <p>The XGBoost model achieved the highest validation accuracy and ROC-AUC score, making it the best-performing model.</p>
</section>

<section id="sec8">
  <h2>Confusion Matrix and Classification Report</h2>
  <p>For the best-performing model (XGBoost), analyzed its confusion matrix and classification report:</p>
  <li><b>Confusion Matrix:</b> Showed strong performance across all classes, though there was some misclassification<br/> in minority classes, which could benefit from further tuning.</li>
  <li><b>Classification Report:</b> High precision and recall for majority classes, and reasonable performance on minority classes after </br>applying oversampling techniques.</li>
</section>

<section id="sec9">
  <h2>Future Work</h2>
  <p>To enhance the model’s accuracy and usability, identified several future improvements:</p>
  <ol>
    <li><b>Feature Engineering:</b> Introduce new features like the previous day’s conditions, seasonality, or air quality to improve predictive power.</li>
    <li><b>Model Tuning:</b> Further optimize hyperparameters in XGBoost and explore other boosting models like CatBoost or LightGBM for better accuracy.</li>
    <li><b>Real-Time Prediction System:</b> Deploy the model to provide real-time weather predictions through an API or web app.</li>
    <li><b>Advanced Sampling Techniques:</b> Experiment with SMOTE (Synthetic Minority Over-sampling Technique) to better handle class imbalance.</li>
    <li><b>Transfer Learning:</b> Utilize pre-trained weather models or regional weather patterns to improve accuracy for Sylhet or nearby regions.</li>
  </ol>
</section>

<section id="sec10">
  <h2>Conslusion</h2>
  <p>The project successfully developed a machine-learning model capable of classifying weather conditions based on historical data.<br/> By testing various algorithms, we found that XGBoost provided the highest accuracy, suggesting that gradient-boosting<br/> techniques are effective for weather classification.</p>
  <p>This model can be extended to provide real-time weather classification, and with additional improvements, it could become a valuable<br/> tool for industries affected by weather conditions, such as agriculture, tourism, and event planning.</p>
</section>

<section id="sec11">
  <h2>Visualization</h2>
  <h3>Columns</h3>
  <img src="https://github.com/user-attachments/assets/075e9e88-1200-490f-a29a-c36e923a8239">

  <h3>Precipitation level in Sylhet in 2023</h3>
  <img src="https://github.com/user-attachments/assets/6d0f99fe-3d4b-463c-a7e3-0fb92458e493">
  <h3> The distribution of the continuous features given in the dataset</h3>
  <img src="https://github.com/user-attachments/assets/e939ff5d-944c-4d88-9c2b-1dab9b05a97c" alt="Subplots">
  <h3> Boxplots for the continuous variable to detect the outliers present in the data.</h3>
  <img src="https://github.com/user-attachments/assets/791ce6b2-4d44-48b6-bc8e-ab4e4d30b646" alt="Boxplots">
  <h3>Correlation Heatmap</h3>
  <img src="https://github.com/user-attachments/assets/90b5da86-780a-475b-b1b4-b8342d686949" alt="Heatmap">
  <h3> confusion matrix as well for the validation data using the Logistic Regression model</h3>
  <img src="https://github.com/user-attachments/assets/106d623c-f9ea-42ab-b04e-076ae1d7588a)" alt="Logistic Regression ">
  <h3> confusion matrix as well for the validation data using the XGBoost model</h3>
  <img src="https://github.com/user-attachments/assets/beb6b4e8-c37f-4f54-b7f7-4ecbf1272c17" alt="XGBoost">
  <h3> confusion matrix as well for the validation data using the SVC (Support Vector) model</h3>
  <img src="https://github.com/user-attachments/assets/3e00ffc2-2ca4-402c-be89-b92bfcce0a18" alt="SVC">
  <h3> confusion matrix as well for the validation data using the Random Forest model</h3>
  <img src="https://github.com/user-attachments/assets/0c223560-e067-40a1-af05-8cadbb32d8a7" alt="Random Forest">
  <h3> confusion matrix as well for the validation data using the K-Nearest Neighbors model</h3>
  <img src="https://github.com/user-attachments/assets/2788b1f8-71c5-4ae3-b595-5102d4482394" alt="K-NN">
  <h3>Decision Tree</h3>
  <img src="https://github.com/user-attachments/assets/cefb1519-ccbd-4f2a-a4fb-b574df53a8bb" alt="Decision Tree">
  <h3> confusion matrix as well for the validation data using the Decision Tree model</h3>
  <img src="https://github.com/user-attachments/assets/f6342213-cb1e-47ac-890c-79a215d936b2" alt="Decision Tree">
</section>

<section id="sec12">
  <h2>Data Source</h2>
  <h3><a href="https://drive.google.com/file/d/1YrgnIn2rnJP6Skw18-VjHSXoDuVdqbFI/view?usp=sharing">Sylhet Weather Dataset 2023</a></h3>
  
</section>
