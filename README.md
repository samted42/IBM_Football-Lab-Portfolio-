# ⚽ Soccer 2026 Match Predictor

> **AI-powered football match outcome predictor built with IBM Bob and scikit-learn**

![Python](https://img.shields.io/badge/Python-3.13-blue) ![Streamlit](https://img.shields.io/badge/Streamlit-1.x-red) ![scikit-learn](https://img.shields.io/badge/scikit--learn-RandomForest-orange) ![IBM Bob](https://img.shields.io/badge/IBM-Bob-0062ff)

---

## 🧩 The Problem We Are Solving

Predicting the outcome of a football match has always been a challenge — even for experts. With the FIFA World Cup 2026 approaching, fans, analysts, and teams want data-driven insights into which teams are most likely to win.

This project answers the question:

> **Given two national teams, what is the probability that Team A wins, it ends in a draw, or Team B wins?**

---

## 🤖 Our AI / Technical Approach

This solution was built entirely using **IBM Bob** as the AI coding assistant — from raw data to a live interactive web app.

### Technology Stack

| Component | Technology |
|-----------|-----------|
| AI Coding Assistant | **IBM Bob** |
| Language | Python 3.13 |
| Machine Learning | scikit-learn (Random Forest Classifier) |
| Data Processing | pandas |
| Web App | Streamlit |
| Model Persistence | joblib |

### How It Works

1. **Dataset** — 49,000+ international football results from 1872 to 2026 (Kaggle)
2. **Feature Engineering** — 8 features computed with zero data leakage:
   - Historical win rate (home & away)
   - Average goals scored
   - Recent form (last 10 matches)
   - Neutral venue flag
   - Major tournament flag
3. **Model** — Random Forest Classifier (200 trees, max depth 12) trained on matches before 2018, tested on 2018–2026
4. **Filtering** — Only FIFA World Cup-eligible teams (215 nations) are included in the predictor
5. **UI** — Interactive Streamlit app with team dropdowns, probability metrics, and progress bars

### Model Performance

- **Test accuracy: ~52%** vs baseline of ~45% (always predict home win)
- Time-based train/test split ensures no future data leakage

---

## 🌍 Why This Matters — Soccer & the World Cup

The FIFA World Cup 2026 will be hosted across the USA, Canada, and Mexico — the largest World Cup in history with 48 teams. Billions of fans worldwide will be following every match.

Our predictor:
- **Democratises sports analytics** — anyone can explore match predictions without needing a data science background
- **Uses 150+ years of football history** to surface patterns that go beyond intuition
- **Showcases IBM Bob** as an AI coding assistant that enables non-coders to build real ML applications
- **Bridges AI and sport** — making machine learning tangible and fun through the universal language of football

---

## 🚀 Running the App

### Prerequisites

```bash
pip install pandas scikit-learn streamlit joblib requests
```

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/samted42/football-lab-portfolio.git
cd football-lab-portfolio

# 2. Run the Streamlit app
streamlit run app.py
```

Open your browser at **http://localhost:8501**

---

## 📁 Repository Structure

```
football-lab-portfolio/
├── app.py                          # Streamlit web app
├── bob_generated_code.ipynb        # Complete ML pipeline (Tasks 1–10)
├── models/
│   ├── match_predictor.pkl         # Trained Random Forest model
│   └── team_data.pkl               # Stats for 215 World Cup-eligible teams
├── data/
│   └── results.csv                 # 49,000+ international match results
└── README.md
```

---

## 📸 App Preview

The app lets you:
- Select any two World Cup-eligible national teams
- Choose venue type (neutral or home) and tournament type
- Click **Predict** to see win probabilities, draw chance, and team statistics

---

## 🏆 Built With IBM Bob

Every line of code in this project was generated using **IBM Bob**, IBM's AI coding assistant. This lab demonstrates how AI tools can empower anyone — regardless of coding background — to build real, functional machine learning applications.

---

## 📊 Dataset

[Kaggle: International football results from 1872 to 2026](https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017)

---

## 👤 Author

**samted42** — IBM SkillsBuild AI Builders Challenge 2025
"# Football-Lab-Portfolio-" 
"# Football-Lab-Portfolio-" 
