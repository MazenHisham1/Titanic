<!DOCTYPE html>
<html>
<head>
</head>
<body>

  <h1>🚢 Titanic Dataset Analysis</h1>

  <h2>📌 Overview</h2>
  <p>
    This project contains an <b>Exploratory Data Analysis (EDA)</b> and optional <b>Machine Learning models</b> 
    built on the Titanic dataset from Kaggle’s 
    <a href="https://www.kaggle.com/c/titanic">Titanic: Machine Learning from Disaster</a>.
  </p>
  <p>The aim is to understand the factors that influenced passenger survival and visualize meaningful patterns.</p>

  <h2>📂 Dataset</h2>
  <p>The dataset includes details about <b>891 passengers</b> aboard the Titanic.</p>

  <table border="1" cellpadding="5" cellspacing="0">
    <tr><th>Column</th><th>Description</th></tr>
    <tr><td>PassengerId</td><td>Unique ID for each passenger</td></tr>
    <tr><td>Survived</td><td>Survival (0 = No, 1 = Yes)</td></tr>
    <tr><td>Pclass</td><td>Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)</td></tr>
    <tr><td>Name</td><td>Passenger name</td></tr>
    <tr><td>Sex</td><td>Gender</td></tr>
    <tr><td>Age</td><td>Age in years</td></tr>
    <tr><td>SibSp</td><td>Number of siblings/spouses aboard</td></tr>
    <tr><td>Parch</td><td>Number of parents/children aboard</td></tr>
    <tr><td>Ticket</td><td>Ticket number</td></tr>
    <tr><td>Fare</td><td>Ticket fare</td></tr>
    <tr><td>Cabin</td><td>Cabin number</td></tr>
    <tr><td>Embarked</td><td>Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)</td></tr>
  </table>

  <h2>🛠️ Tech Stack</h2>
  <ul>
    <li>Python 🐍</li>
    <li>Pandas – Data manipulation</li>
    <li>NumPy – Numerical operations</li>
    <li>Matplotlib & Seaborn – Visualizations</li>
  </ul>

  <h2>🔍 Project Workflow</h2>
  <ol>
    <li><b>Data Cleaning</b> – Handle missing values and encode categorical features</li>
    <li><b>Exploratory Data Analysis</b> – Study distributions and survival rates</li>
    <li><b>Data Visualization</b> – Create plots and charts</li>
  </ol>

  <h2>📊 Example Insights</h2>
  <ul>
    <li>Women had a higher survival rate than men.</li>
    <li>First-class passengers were more likely to survive than those in second/third class.</li>
    <li>Children had better survival chances compared to older groups.</li>
  </ul>

  <h2>🚀 Getting Started</h2>
  <p><b>1️⃣ Clone the repository</b></p>
  <pre><code>git clone https://github.com/MazenHisham1/titanic-analysis.git
cd titanic-analysis</code></pre>

  <p><b>2️⃣ Install dependencies</b></p>
  <pre><code>pip install -r requirements.txt</code></pre>

  <p><b>3️⃣ Run the notebook</b></p>
  <pre><code>jupyter notebook Titanic_Analysis.ipynb</code></pre>

  <h2>📌 Future Improvements</h2>
  <ul>
    <li>Feature engineering (extract titles from names)</li>
  </ul>

  <h2>🤝 Contributing</h2>
  <p>Contributions are welcome! Please fork this repo, create a new branch, and submit a pull request.</p>

  <h2>📜 License</h2>
  <p>This project is licensed under the <b>MIT License</b>. Dataset courtesy of 
    <a href="https://www.kaggle.com/c/titanic">Kaggle Titanic Competition</a>.
  </p>

</body>
</html>
