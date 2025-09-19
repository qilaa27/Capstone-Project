# 💤 Sleep Health Analysis with AI Support

## 📌 Project Overview

This capstone project aims to analyze a public dataset on sleep health and lifestyle. By combining Exploratory Data Analysis (EDA) with a Large Language Model (LLM), we extract meaningful insights and actionable recommendations to improve sleep quality.

I use **IBM Granite 3.3-8B** through **LangChain + Replicate API** for AI-assisted analysis.

---

## 📂 Dataset

- **Name:** Sleep Health and Lifestyle Dataset  
- **Source:** [Kaggle Link](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset)  
- **Shape:** 374 rows × 13 columns  
- **Target Variable:** `Sleep Disorder` (`Normal`, `Insomnia`, `Sleep Apnea`)  

---

## 🧼 Data Preprocessing & Cleaning

- Imputed missing values in `Sleep Disorder` column as `'Normal'`:
  ```python
  df['Sleep Disorder'] = df['Sleep Disorder'].fillna(value='Normal')
- Selected numeric subset (select_dtypes) for statistical and correlation analysis.
- Used describe() to generate descriptive statistics.
- Checked correlation with df.corr().

--- 

## 📊 Exploratory Data Analysis (EDA)

1. Sleep Disorder Distribution
Used countplot to visualize distribution of sleep disorder types.

2. Correlation Heatmap
Identified relationships among Sleep Duration, Stress Level, Quality of Sleep, and Physical Activity Level.

3. Scatter Plot
Found a negative trend between Stress Level and Quality of Sleep.

## 🤖 AI-Assisted Analysis using IBM Granite

#### Prompt 1: Ringkasan Statistik & Insight

Ringkas data numerik berikut:
{summary}

Berdasarkan data di atas:
- Sebutkan 3 insight penting.
- Sebutkan 3 rekomendasi praktis untuk meningkatkan kualitas tidur.

a. Output from AI:
- High stress is associated with lower sleep quality.
- Short sleep duration frequently appears in individuals with insomnia.
- Higher physical activity is observed in people without sleep disorders.

b. Recommendations:
- Sleep at least 7–8 hours every night.
- Exercise regularly with light activities like walking or yoga.
- Reduce stress through relaxation techniques.

#### Prompt 2: Korelasi dengan Sleep Disorder

Pertanyaan:
Variabel apa yang paling berkorelasi dengan Sleep Disorder?

a. Output from AI:
The most influential factors are Stress Level, Quality of Sleep, and Sleep Duration.

#### Prompt 3: Interpretasi Grafik Scatter

Terdapat scatter plot antara Stress Level dan Quality of Sleep.
Apa interpretasinya?

a. AI Response:
- There is a negative relationship: the higher the stress level, the lower the sleep quality.
- This highlights the importance of stress management for healthy sleep.

## 💡 AI Support Explanation
We integrated a powerful LLM (IBM Granite) to:
- Summarize statistics and extract correlations.
- Generate expert-level insights and health recommendations.
- Assist with interpreting visualizations.

This showcases how AI can accelerate data-driven health decisions.

## ✅ Final Recommendations
- Prioritize stress reduction to improve sleep quality.
- Maintain regular sleep duration (7+ hours).
- Monitor physical activity and avoid sedentary lifestyles.
- Use AI tools for faster and deeper health data interpretation.
