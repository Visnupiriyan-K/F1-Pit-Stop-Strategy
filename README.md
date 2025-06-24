# 🏁 Formula 1 Pit Stop Strategy Analysis

This project explores pit stop strategies and performance metrics in Formula 1 using structured data analysis, visualization, and machine learning. It evaluates how pit stop efficiency affects race outcomes, constructor performance, and driver success, aiming to offer actionable insights for teams and future constructors.

---

## 📊 Abstract

This project presents a comprehensive data analysis pipeline emphasizing data preprocessing, EDA, and visualization. Datasets such as `circuits` and `drivers` are cleaned, duplicated for safe processing, and explored using custom summary functions and visual aids like waterfall charts. The goal is to uncover key patterns, ensure data readiness for modeling, and enable high-impact insights for motorsport analytics.

---

## 🏎 Background

With the explosion of data in motorsports, especially Formula 1, preprocessing and structured workflows are critical. This project adopts automation, cloud storage (Google Drive), and reproducible tools to summarize and visualize high-volume telemetry and historical performance data. The result is a framework that enables reliable decision-making and insights into race dynamics.

---

## ❗ Problem Statement

Pit stop inefficiencies and suboptimal race strategies can cause teams to lose precious time, directly impacting their race position. This project aims to:
- Analyze historical race and pit stop data.
- Correlate circuit conditions, driver stats, and strategy outcomes.
- Recommend data-driven solutions to optimize pit times.

---

## 💼 Impact on Business

Effective pit strategies improve race performance and team standings, boosting brand value, sponsorships, and merchandise revenue. This project provides:
- Benchmarks for top-performing teams.
- Historical patterns of pit stop optimization.
- Insights into operational inefficiencies and competitive gaps.

---

## 🗂 Dataset and Domain

This project utilizes Formula 1 datasets:
- `circuits.csv`: Includes track layout, name, and environment.
- `drivers.csv`: Driver history, wins, retirements, and qualifying data.

The domain is **Motorsport Analytics**, especially focused on strategy and operational efficiency.

---

## 🧩 Data Selection Criteria

1. **Relevance** – Pit stop times, race results, and circuit data.
2. **Completeness** – Coverage across years and teams.
3. **Accuracy** – Verified from official F1 sources or telemetry.
4. **Timeliness** – Spanning from 2010 to 2023 with updated data.

---

## 🔍 Exploratory Data Analysis (EDA)

### Lewis Hamilton's Championship Standings (2007–2023)
![Figure 12](./assets/figure12_hamilton_standings.png)

### Mercedes Constructor Standings Over Time
![Figure 13](./assets/figure13_mercedes_standings.png)

### Top 5 Constructors – Finish Position Distribution
![Figure 14](./assets/figure14_boxplot_constructors.png)

### Monaco Circuit Driver Finish Positions
![Figure 15](./assets/figure15_monaco_distribution.png)

### Top 10 Drivers by Wins
![Figure 16](./assets/figure16_driver_wins.png)

### Top 10 Drivers by Points
![Figure 17](./assets/figure17_driver_points.png)

### Average Qualifying Position (Top Drivers)
![Figure 18](./assets/figure18_avg_qualifying.png)

---

## 🛠 Pit Stop Insights

### Pit Stop Time Distribution
![Figure 19](./assets/figure19_pitstop_dist.png)

### Constructors vs. Avg Pit Stop Time
![Figure 20](./assets/figure20_const_avg_time.png)

### Race Tracks vs. Avg Pit Stop Time
![Figure 21](./assets/figure21_tracks_avg_time.png)

### Pit Stop Duration by Constructor (Scatter)
![Figure 22](./assets/figure22_const_pitstop_scatter.png)
![Figure 23](./assets/figure23_const_pitstop_scatter2.png)

### Avg Pit Stop Time by Race Circuit
![Figure 24](./assets/figure24_avg_pitstop_circuit.png)
![Figure 25](./assets/figure25_avg_pitstop_simple.png)

### Boxplots by Circuit & Constructor
![Figure 26](./assets/figure26_boxplot_circuits.png)
![Figure 27](./assets/figure27_boxplot_2021.png)
![Figure 28](./assets/figure28_boxplot_2011_onward.png)

### Line Chart – Avg Pit Stop by Constructor
![Figure 29](./assets/figure29_line_avg_const.png)

### Total Pit Lane Time by Circuit
![Figure 30](./assets/figure30_pitlane_total1.png)
![Figure 31](./assets/figure31_pitlane_total2.png)
![Figure 32](./assets/figure32_pitlane_total_revised.png)

### Pit Lane % vs Final Race Position
![Figure 33](./assets/figure33_pitlane_percent_vs_position.png)

### Pit Stop Duration Distribution (Histogram)
![Figure 34](./assets/figure34_pitstop_hist.png)

### Avg Pit Stop Time by Constructor (Gradient Bar)
![Figure 35](./assets/figure35_avg_pitstop_gradient.png)
![Figure 36](./assets/figure36_avg_pitstop_gradient2.png)

### Avg Pit Stop Time vs Wins (Bubble)
![Figure 37](./assets/figure37_bubble_wins_vs_pit.png)

---

## 🤖 Models Implemented

### RandomForestClassifier  
**Figure 38**  
- Predicts incidents & race wins  
- Accuracy: ~91.77%  
- Strength: High precision in multi-feature classification

### Support Vector Regressor (SVR)  
**Figure 39**  
- Used for lap time prediction  
- Result: High MSE, underfitting  
- Insight: Required better preprocessing or feature scaling

### Ridge Regression  
**Figure 40**  
- Predicts race outcomes from pit data  
- Result: Low R²  
- Limitation: Weak feature correlation

### DecisionTreeRegressor  
**Figure 41**  
- Used for qualifying position  
- Strength: Interpretability, no need for scaling

### Race Strategy Simulations  
- Compared time gains from varying pit strategies  
- Result: Average time saved per optimized pit stop strategy

---

## ✅ Key Takeaways

- Hamilton and Mercedes consistently outperform others in both standings and pit efficiency.
- Pit stop durations heavily influence team standings and final race positions.
- RandomForestClassifier yields the best model accuracy.
- Custom strategy simulations add valuable race outcome insights.

---

## 📌 Conclusion

This project bridges motorsport and machine learning, using data science to drive race-day decisions. It demonstrates the value of structured preprocessing, automated EDA, and model validation in optimizing pit stop performance. Teams can use this blueprint to refine pit strategies, reduce downtime, and gain competitive advantages.

---

## 📚 References

- Formula 1 Official Data Archive – [formula1.com](https://www.formula1.com)  
- Rohan Rao, Kaggle – [F1 Dataset](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020)  
- Scikit-learn, PyTorch Documentation  
- "Pattern Recognition & Machine Learning" – Bishop  
- "The Elements of Statistical Learning" – Hastie, Tibshirani, Friedman  
- Few, Tufte – Visualization Best Practices  

---

## 📁 Folder Structure

