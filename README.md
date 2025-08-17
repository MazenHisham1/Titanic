<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>🚢 Titanic Dataset Analysis – README (HTML)</title>
  <style>
    :root {
      --bg: #0b0c10;
      --panel: #111217;
      --text: #e8e8ea;
      --muted: #b9bbc6;
      --accent: #58a6ff;
      --border: #23262f;
      --code-bg: #0f1116;
    }
    @media (prefers-color-scheme: light) {
      :root {
        --bg: #f7f7fb;
        --panel: #ffffff;
        --text: #0f172a;
        --muted: #475569;
        --accent: #2563eb;
        --border: #e5e7eb;
        --code-bg: #0f172a0d;
      }
    }
    html, body { height: 100%; }
    body {
      margin: 0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Noto Sans, Ubuntu, Cantarell, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji";
      background: linear-gradient(180deg, var(--bg), var(--panel));
      color: var(--text);
      line-height: 1.6;
    }
    .wrap {
      max-width: 950px;
      margin: 0 auto;
      padding: 2.5rem 1.2rem 4rem;
    }
    header {
      background: linear-gradient(180deg, rgba(88,166,255,0.08), transparent);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      backdrop-filter: blur(6px);
      z-index: 10;
    }
    .title { font-size: clamp(1.8rem, 3vw, 2.3rem); margin: 0 0 0.25rem; }
    .subtitle { color: var(--muted); margin: 0 0 1rem; }
    .badges img { height: 22px; margin-right: 8px; vertical-align: middle; }
    .panel {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 1.25rem 1.25rem;
      box-shadow: 0 1px 0 rgba(0,0,0,0.05), 0 10px 25px -20px rgba(0,0,0,0.4);
    }
    nav {
      margin: 1rem 0 1.5rem;
      display: flex;
      flex-wrap: wrap;
      gap: .5rem .75rem;
    }
    nav a {
      text-decoration: none;
      padding: .45rem .7rem;
      border: 1px solid var(--border);
      border-radius: 999px;
      color: var(--text);
      background: linear-gradient(180deg, transparent, rgba(255,255,255,0.03));
      font-size: .9rem;
    }
    nav a:hover { border-color: var(--accent); color: var(--accent); }

    h2 { margin-top: 2rem; font-size: clamp(1.35rem, 2.4vw, 1.6rem); }
    h3 { margin-top: 1.2rem; font-size: 1.05rem; color: var(--muted); }

    code, pre { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace; }
    pre {
      background: var(--code-bg);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 1rem;
      overflow: auto;
    }
    .kbd {
      font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
      background: var(--code-bg);
      border: 1px solid var(--border);
      border-bottom-width: 3px;
      padding: .1rem .4rem;
      border-radius: 6px;
      font-size: .9em;
    }
    table { width: 100%; border-collapse: collapse; }
    th, td { border: 1px solid var(--border); padding: .6rem .7rem; text-align: left; }
    th { background: linear-gradient(180deg, rgba(88,166,255,0.08), transparent); }
    .list-check li { margin-bottom: .4rem; }
    .muted { color: var(--muted); }
    footer { color: var(--muted); font-size: .95rem; margin-top: 2.5rem; }
    .hr { height: 1px; background: var(--border); border: 0; margin: 1.5rem 0; }
    a { color: var(--accent); }
  </style>
</head>
<body>
  <header>
    <div class="wrap">
      <h1 class="title">🚢 Titanic Dataset Analysis</h1>
      <p class="subtitle">GitHub-style README rendered as a beautiful single-file HTML page.</p>
      <div class="badges">
        <img alt="Python" src="https://img.shields.io/badge/Python-3.8%2B-blue.svg" />
        <img alt="Pandas" src="https://img.shields.io/badge/Pandas-Data%20Analysis-orange" />
        <img alt="Seaborn" src="https://img.shields.io/badge/Seaborn-Visualization-green" />
        <img alt="License" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
      </div>
      <nav>
        <a href="#overview">Overview</a>
        <a href="#dataset">Dataset</a>
        <a href="#stack">Tech Stack</a>
        <a href="#workflow">Project Workflow</a>
        <a href="#insights">Example Insights</a>
        <a href="#getting-started">Getting Started</a>
        <a href="#future">Future Improvements</a>
        <a href="#contributing">Contributing</a>
        <a href="#license">License</a>
      </nav>
    </div>
  </header>

  <main class="wrap">
    <section id="overview" class="panel">
      <h2>📌 Overview</h2>
      <p>This repository contains an <strong>Exploratory Data Analysis (EDA)</strong> and optional <strong>Machine Learning</strong> models built on the <em>Titanic dataset</em> from Kaggle’s <a href="https://www.kaggle.com/c/titanic" target="_blank" rel="noopener">Titanic: Machine Learning from Disaster</a>. The aim is to understand the factors that influenced passenger survival and visualize meaningful patterns.</p>
    </section>

    <section id="dataset" class="panel">
      <h2>📂 Dataset</h2>
      <p>The classic training set includes details about <strong>891 passengers</strong> aboard the Titanic.</p>
      <div class="hr"></div>
      <table>
        <thead>
          <tr>
            <th>Column</th>
            <th>Description</th>
          </tr>
        </thead>
        <tbody>
          <tr><td><code>PassengerId</code></td><td>Unique ID for each passenger</td></tr>
          <tr><td><code>Survived</code></td><td>Survival (0 = No, 1 = Yes)</td></tr>
          <tr><td><code>Pclass</code></td><td>Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)</td></tr>
          <tr><td><code>Name</code></td><td>Passenger name</td></tr>
          <tr><td><code>Sex</code></td><td>Gender</td></tr>
          <tr><td><code>Age</code></td><td>Age in years</td></tr>
          <tr><td><code>SibSp</code></td><td>Number of siblings/spouses aboard</td></tr>
          <tr><td><code>Parch</code></td><td>Number of parents/children aboard</td></tr>
          <tr><td><code>Ticket</code></td><td>Ticket number</td></tr>
          <tr><td><code>Fare</code></td><td>Ticket fare</td></tr>
          <tr><td><code>Cabin</code></td><td>Cabin number</td></tr>
          <tr><td><code>Embarked</code></td><td>Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)</td></tr>
        </tbody>
      </table>
      <p class="muted">Dataset courtesy of Kaggle’s Titanic competition.</p>
    </section>

    <section id="stack" class="panel">
      <h2>🛠️ Tech Stack</h2>
      <ul>
        <li><strong>Python</strong> – core language</li>
        <li><strong>Pandas</strong> – data manipulation</li>
        <li><strong>NumPy</strong> – numerical operations</li>
        <li><strong>Matplotlib &amp; Seaborn</strong> – visualizations</li>
        <li><strong>Scikit-learn</strong> – ML models (optional)</li>
      </ul>
    </section>

    <section id="workflow" class="panel">
      <h2>🔍 Project Workflow</h2>
      <h3>1) Data Cleaning 🧹</h3>
      <ul class="list-check">
        <li>Handle missing values (e.g., <code>Age</code>, <code>Cabin</code>, <code>Embarked</code>).</li>
        <li>Encode categorical features.</li>
      </ul>
      <h3>2) Exploratory Data Analysis (EDA) 📊</h3>
      <ul class="list-check">
        <li>Distribution of age, gender, and ticket class.</li>
        <li>Survival rate across passenger groups.</li>
      </ul>
      <h3>3) Data Visualization 🎨</h3>
      <ul class="list-check">
        <li>Heatmaps, bar plots, and histograms.</li>
      </ul>
      <h3>4) Machine Learning (Optional) 🤖</h3>
      <ul class="list-check">
        <li>Logistic Regression, Random Forest, etc.</li>
        <li>Evaluate with accuracy and confusion matrix.</li>
      </ul>
    </section>

    <section id="insights" class="panel">
      <h2>📊 Example Insights</h2>
      <ul>
        <li>Women had a higher survival rate than men.</li>
        <li>First-class passengers were more likely to survive than those in second/third class.</li>
        <li>Younger passengers (children) had better survival chances compared to older groups.</li>
      </ul>
    </section>

    <section id="getting-started" class="panel">
      <h2>🚀 Getting Started</h2>
      <h3>1️⃣ Clone the repository</h3>
      <pre><code>git clone https://github.com/yourusername/titanic-analysis.git
cd titanic-analysis</code></pre>
      <h3>2️⃣ Install dependencies</h3>
      <pre><code>pip install -r requirements.txt</code></pre>
      <h3>3️⃣ Run the notebook</h3>
      <pre><code>jupyter notebook Titanic_Analysis.ipynb</code></pre>
    </section>

    <section id="future" class="panel">
      <h2>📌 Future Improvements</h2>
      <ul>
        <li>Feature engineering (e.g., extracting titles from names).</li>
        <li>Hyperparameter tuning for ML models.</li>
        <li>Try advanced models (XGBoost, LightGBM).</li>
      </ul>
    </section>

    <section id="contributing" class="panel">
      <h2>🤝 Contributing</h2>
      <p>Contributions are welcome! Please fork this repo, create a new branch, and submit a pull request.</p>
    </section>

    <section id="license" class="panel">
      <h2>📜 License</h2>
      <p>This project is licensed under the <strong>MIT License</strong>. Dataset courtesy of Kaggle’s Titanic competition.</p>
    </section>

    <footer>
      <p>Made with ❤️ &nbsp;—&nbsp; Single-file HTML &amp; CSS. Optimize images &amp; minify CSS if publishing.</p>
    </footer>
  </main>
</body>
</html>
