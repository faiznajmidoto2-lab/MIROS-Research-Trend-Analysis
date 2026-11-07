# MIROS Research Trend Analysis (2018–2025)
**Text Mining & Exploratory Data Analysis of Road Safety Research Projects**

## 📌 Project Background
The Malaysian Institute of Road Safety Research (MIROS) has conducted numerous research projects over the years. Without a centralized view, it is difficult to identify overlapping topics, track the evolution of research focus, and identify gaps in road user coverage. 

This project uses Natural Language Processing (NLP) to programmatically analyze 88 research project titles from 2018 to 2025. The goal is to discover **what topics have been covered**, **how frequently they appear**, and **which road user categories are underserved**.

## 🎯 Business Objectives
1. **Topic Discovery:** Identify the most frequent and statistically significant keywords in research titles.
2. **Trend Analysis:** Track how research focus has shifted year-over-year.
3. **Gap Analysis:** Categorize projects by road user type (Pedestrian, Motorcyclist, Heavy Vehicle, etc.) to see which areas need more attention.
4. **Automation:** Replace manual reading and sorting with an automated text-processing pipeline.

## 🛠️ Tools & Libraries Used
- **Language:** Python
- **Data Processing:** Pandas, Regular Expressions (Regex)
- **NLP:** NLTK (Stopwords), Scikit-learn (TF-IDF, CountVectorizer)
- **Visualization:** Matplotlib, Seaborn, WordCloud

## 🧠 Methodology
1. **Data Cleaning:** 
   - Stripped column names and handled missing values.
   - Used Regex to remove punctuation, numbers, and single-letter words.
   - Built a **custom stopword dictionary** combining English (NLTK) and Malay stopwords (*dan, di, ke, kajian, projek*) to ensure accurate topic extraction.
2. **Exploratory Analysis:** Generated Word Clouds and Bar Charts for univariate frequency analysis.
3. **Contextual Analysis:** Used **Bigrams** (2-word phrases) to find specific contexts (e.g., "road safety", "pedestrian crossing") rather than isolated words.
4. **Statistical Importance:** Applied **TF-IDF (Term Frequency-Inverse Document Frequency)** to find the most unique and important terms, filtering out common words.
5. **Categorization:** Built a custom keyword-matching function to classify projects into Road User Categories (Pedestrian, Motorcyclist, Cyclist, Heavy Vehicle, Public Transport, Speed Control).

## 📊 Key Insights
- **Core Focus:** "Road", "Malaysia", and "Safety" are the most frequent terms. TF-IDF confirms "Motorcycle" and "Safety" are statistically the most significant themes.
- **Specific Context:** Bigram analysis highlights strong research focus on "Exclusive Motorcycle" lanes and "Pedestrian Crossing".
- **Gap Analysis:** Out of 88 projects, **Motorcyclists (16 projects)** and **Pedestrians (8 projects)** received the most attention, while **Public Transport (2 projects)** and **Cyclists (4 projects)** were significantly underserved.
- **Yearly Trends:** Speed control and Heavy Vehicle research saw specific spikes in certain years (e.g., 2019 and 2024).

## 💡 Recommendations (If implemented at MIROS)
- **Increase Public Transport Research:** Given the low number of projects (2), MIROS should prioritize research on bus safety and transit accessibility.
- **Dashboard Integration:** The extracted topics could be fed into a Power BI dashboard to monitor new research titles in real-time, preventing project duplication.

## 🚀 How to Run
1. Clone this repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Open `notebooks/Text_Mining_Analysis.ipynb` and run all cells.

---
*Note: This project was conducted during my internship at MIROS (Malaysian Institute of Road Safety Research).*
