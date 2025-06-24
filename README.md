# 🏎️ Formula 1 Pit Stop Analysis and Optimization

This project explores the role of **data analysis, visualization, and machine learning** in optimizing pit stop strategies in Formula 1. By examining key performance indicators, constructor data, and pit stop metrics, the goal is to derive actionable insights to improve competitive performance on the racetrack.

---

## 📘 Abstract

This project presents a comprehensive data analysis pipeline, emphasizing **preprocessing**, **EDA**, and **visualizations** to derive insights from motorsport data. Key stages include:
- Integration with Google Drive (for dataset access).
- Use of Python libraries for summarization and plotting.
- Structured data duplication to ensure raw integrity.
- Automated insights via reusable functions (`get_desired_summary`).
- Use of waterfall charts and custom visuals to highlight performance shifts.

This systemized approach ensures clean datasets ready for ML or advanced analytics, with a focus on reproducibility and future adaptability.

---

## 🧠 Background

With data at the heart of modern motorsport strategy, teams rely on telemetry, weather data, driver stats, and race history to inform decisions. This project mirrors such real-world practices:
- Accesses circuits and drivers datasets.
- Leverages `summarytools`, visual analytics, and structured scripting.
- Recreates real-world analysis techniques using automation and reproducible patterns.

---

## ❓ Problem Statement

In F1, a **single-second delay** in pit stops can cost a podium finish. Teams require data-driven pit stop strategies that:
- Minimize downtime.
- Adapt to circuit and driver conditions.
- Reduce operational inefficiencies.

Our goal: Analyze historical F1 data to build **pit stop benchmarks**, **constructor comparisons**, and **strategic recommendations**.

---

## 💼 Business Impact

- ⬆️ Better race outcomes → more points, wins, and prize money.
- 📈 Improved standings → more sponsorship & brand recognition.
- 💰 Efficient strategy planning → reduced trial-and-error costs.
- 🔧 Strategic planning for new constructors entering the grid.

---

## 🧾 Dataset and Domain

- **Domain**: Motorsport analytics (Formula 1 focus)
- **Datasets**:
  - `circuits`: Names, locations, layout info.
  - `drivers`: Performance stats, team affiliations.
- **Source**: [Formula1.com](https://www.formula1.com) and [Kaggle F1 datasets](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020/data)

---

## 🧠 Data Selection Criteria

| Criterion       | Description |
|----------------|-------------|
| **Relevance**  | Circuits and drivers are directly tied to pit stop success. |
| **Completeness** | Ensures minimal missing values in race outcomes, timings, and strategy metadata. |
| **Accuracy**   | Data from reliable F1 archives and telemetry sources. |
| **Timeliness** | Covers multiple seasons, capturing both historic and current trends. |

---

## 📊 Exploratory Data Analysis (Key Visuals)

### Lewis Hamilton's Championship Standings Over Time  
![Figure 12](./assets/figure12_hamilton_standings.png)

### Mercedes Constructors' Standings  
![Figure 13](./assets/figure13_mercedes_standings.png)

### Race Finish Position Distribution (Top 5 Constructors)  
![Figure 14](./assets/figure14_boxplot_constructors.png)

### Monaco Circuit Finish Positions  
![Figure 15](./assets/figure15_monaco_distribution.png)

### Top 10 Drivers by Wins  
![Figure 16](./assets/figure16_driver_wins.png)

### Top 10 Drivers by Points  
![Figure 17](./assets/figure17_driver_points.png)

### Average Qualifying Position  
![Figure 18](./assets/figure18_avg_qualifying.png)

---

## ⛽ Pit Stop Performance Visualizations

| Metric | Visualization |
|--------|---------------|
| Pit Stop Distribution | ![Figure 19](./assets/figure19_pitstop_dist.png) |
| Constructors vs Avg Pit Stop Time | ![Figure 20](./assets/figure20_const_avg_time.png) |
| Tracks vs Avg Pit Stop Time | ![Figure 21](./assets/figure21_tracks_avg_time.png) |
| Pit Stop Duration by Constructor | ![Figure 22](./assets/figure22_const_pitstop_scatter.png) |
| Pit Stop Duration by Circuit | ![Figure 24](./assets/figure24_avg_pitstop_circuit.png) |

📈 Figures 25 to 36 explore:
- Circuit variability
- Total pit lane time
- Pit stop time vs performance
- Average performance by constructor

Each chart is included in the `/assets/` folder and referenced in this README for traceability.

---

## 🤖 Models Implemented

### 🎯 RandomForestClassifier  
**Purpose**: Predict incident occurrence and race winners  
![Figure 38](./assets/figure38_rf_accuracy.png)  
**Results**:  
- Incident prediction: 91.77% accuracy  
- Winner prediction: 80% accuracy (imbalanced classes)  

---

### 📉 Support Vector Regressor (SVR)  
**Purpose**: Predict lap times  
![Figure 39](./assets/figure39_svr_results.png)  
**Results**:  
- High MSE  
- Underfitting likely due to poor feature selection  

---

### 🔢 Ridge Regression  
**Purpose**: Predict race outcomes using pit stop metrics  
![Figure 40](./assets/figure40_ridge_results.png)  
**Results**:  
- High MSE, low R²  
- Limited predictive capability  

---

### 🌳 DecisionTreeRegressor  
**Purpose**: Predict qualifying positions  
![Figure 41](./assets/figure41_dtr_results.png)  
**Results**:  
- Model interpretable  
- Useful for basic strategy forecasting  

---

## 🎯 Simulation of Pit Stop Strategies

Statistical simulations show:
- Mean & std dev of different strategies
- Estimated time savings by optimized sequences
- Use of Monte Carlo-style sampling to evaluate randomness

---

## ✅ Key Takeaways

| ✅ Insight | Description |
|-----------|-------------|
| Hamilton Dominance | Most wins, best average start position |
| Mercedes Era | 2014–2021 dominance confirmed |
| Pit Stop Ranges | ~20–30s is optimal, <20s is elite |
| Outliers | Circuits like Baku and Korea cause delays |
| Top Constructors | Mercedes, Red Bull excel in consistency |

---

## 📌 Conclusion

This project demonstrates the power of **data-driven pit stop strategy** in F1:
- EDA reveals consistent vs outlier performances.
- Visuals highlight critical decision points (driver, track, timing).
- RandomForest was most reliable ML model.
- Simulations quantify race outcome variances due to pit stops.

The approach combines **motorsport domain knowledge** and **statistical rigor**, showing how teams can gain an edge through smarter data use.

---

## 📚 References

- Formula 1 Data Archives: [formula1.com](https://www.formula1.com)
- Kaggle F1 Dataset: [rohanrao/F1 Championship](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020)
- McKinney, Hunter (Matplotlib), Scikit-learn Docs, PyTorch Docs
- Statistical Learning: Hastie, Tibshirani, Breiman
- Motorsport Strategy Journal (2023)

---

> **Note**: All visualizations are stored in the `/assets/` directory. Ensure all figures from 12 to 41 are included in that path.

---

Let me know if you’d like help auto-generating the directory or assets structure with Python or bash commands!
