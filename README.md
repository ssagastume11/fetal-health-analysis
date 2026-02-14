![GitHub Repo Size](https://img.shields.io/github/repo-size/ssagastume11/fetal-health-analysis)
![Last Commit](https://img.shields.io/github/last-commit/ssagastume11/fetal-health-analysis)

# 🩺 Fetal Health Classification Analysis

This project analyzes cardiotocogram (CTG) exam data to identify patterns that distinguish between **Normal**, **Suspect**, and **Pathological** fetal health classifications.  

The goal is to uncover measurable differences in fetal heart rate variability and related indicators that can help healthcare professionals prioritize monitoring and intervention for higher-risk pregnancies.

This project follows the **Google Data Analytics 6-Step Framework**:
Ask → Prepare → Process → Analyze → Share → Act

---

## 📦 Dataset

**Source**: Fetal Health Classification Dataset (CTG Data)  
**Original Context**: Cardiotocogram recordings analyzed for fetal health risk classification  

**Filename**: `fetal_health.csv`  
**Location**: Stored in the `data/` folder  

**Target Variable**:
- `fetal_health`
  - 1 = Normal
  - 2 = Suspect
  - 3 = Pathological

**Features Include**:
- Baseline fetal heart rate
- Accelerations
- Fetal movement
- Uterine contractions
- Light, severe, and prolonged decelerations
- Short-term and long-term variability metrics
- Histogram-based statistical measures

---

## 🔍 Business Task

The objective of this analysis is to identify measurable characteristics that differentiate fetal health classifications in order to:

- Detect patterns associated with high-risk (Pathological) cases
- Compare variability metrics across classifications
- Support data-driven prioritization of medical monitoring
- Translate clinical metrics into actionable insights

---

## 📊 Tools & Technology

- **Google BigQuery** for cloud-based SQL processing
- **SQL (SAFE_CAST, aggregation, views)** for cleaning and transformation
- **Tableau Public** for interactive dashboard visualization
- **Google Slides** for executive presentation
- **Git & GitHub** for version control and documentation

---

## 📁 Project Structure

```plaintext
gaming-hours-performance-analysis/
├── data/
├── sql/
├── visuals/
├── tableau/
├── presentation/
└── README.md
```

---

## 🧮 Sample SQL Query (Classification Comparison)
```SQL
SELECT
  fetal_health_class,
  COUNT(*) AS total_records,
  ROUND(AVG(baseline_value),2) AS avg_baseline_value,
  ROUND(AVG(accelerations),4) AS avg_accelerations,
  ROUND(AVG(mean_short_term_variability),2) AS avg_mean_stv,
  ROUND(AVG(mean_long_term_variability),2) AS avg_mean_ltv
FROM
  `plenary-ability-463920-b3.fetal_health_analysis.cleaned_fetal_health`
GROUP BY
  fetal_health_class
ORDER BY
  fetal_health_class;
```

---

## 📈 Analysis Output

Key visual outputs stored in the visuals/ folder include:

- Pathological cases show higher abnormal short-term variability
- Suspect cases often fall between Normal and Pathological metrics
- Variability and deceleration patterns are strong differentiators
- Certain histogram statistics reflect measurable distribution differences across classifications

---

## 📊 Interactive Tableau Dashboard

Explore the interactive dashboard analyzing how gaming habits impact academic and workplace performance:

🔗 **Tableau Public Dashboard:**  
[Fetal Health Analysis](https://public.tableau.com/views/FetalHealthAnalysis/FetalHealthClassification?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

The dashboard allows interactive exploration of:

- Average clinical metrics by classification
- Distribution differences between health groups
- Variability trends across risk levels

---

## 🧾 Presentation

The Google Slides presentation includes:

- Problem definition and business task
- Data preparation methodology
- SQL transformation logic
- Analytical findings
- Recommendations for healthcare prioritization

---

## 📌 Recommendations
- Prioritize monitoring for cases with elevated abnormal variability
- Develop threshold alerts for high-risk variability patterns
- Integrate data dashboards into clinical review workflows
- Expand analysis with predictive modeling in R

---

## 🛠 Skills Demonstrated
- Data cleaning and type validation using SQL
- Clinical metric aggregation and comparison
- Analytical storytelling
- Dashboard design and stakeholder communication
- End-to-end analytics workflow documentation

## 🙌 Acknowledgments
- Dataset courtesy of [Larxel on Kaggle](https://www.kaggle.com/datasets/andrewmvd/fetal-health-classification) 
- Tools powered by Google Cloud BigQuery, SQL, Tableau and Google Slides

---

👨‍💻 Author

**Sergio E. Sagastume**
Data Analyst | SQL | Tableau | R


