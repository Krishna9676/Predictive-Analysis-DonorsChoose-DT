Your write‑up is already strong — it just needs clean Markdown formatting so it drops directly into a GitHub README and renders beautifully. Below is a polished, GitHub‑ready version of your entire section, including a properly formatted performance table.
You can paste this directly into your README.md file.

# DonorsChoose Funding Prediction using Decision Trees and NLP

##  Project Overview
This project predicts the approval status of classroom funding requests submitted to **DonorsChoose**, a non-profit platform that connects donors with public school teachers.  
By combining structured categorical data with unstructured project essays, this machine learning pipeline identifies which projects are most likely to be approved.  
The goal is to help organizations prioritize resources and provide teachers with insights into what makes a proposal successful.

---

##  Technical Stack
- **Language:** Python  
- **Libraries:** Scikit‑Learn, NLTK, Pandas, NumPy, Matplotlib, Seaborn  
- **Techniques:** Decision Tree Classification, NLP, Sentiment Analysis, GridSearchCV  

---

## 🏗️ Data Pipeline

### 1. Data Cleaning & Preprocessing
- Standardized categorical features such as `school_state`, `project_grade_category`, and `teacher_prefix`.
- Cleaned project essays by removing special characters, stopwords, and applying text decontraction.

### 2. Feature Engineering
- **Sentiment Analysis:** Used VADER to extract Positive, Negative, Neutral, and Compound sentiment scores.
- **Vectorization (NLP):**
  - **TF‑IDF:** Captures statistical importance of words.
  - **TF‑IDF Weighted Word2Vec:** Uses GloVe embeddings to capture semantic meaning.

### 3. Model Building & Optimization
- Implemented a **Decision Tree Classifier** with `class_weight='balanced'`.
- Tuned hyperparameters (`max_depth`, `min_samples_split`) using **GridSearchCV**.

---

##  Results & Performance

The model was evaluated using the **ROC‑AUC score**.

| Vectorizer              | Max Depth | Min Sample Split | Test AUC |
|-------------------------|-----------|-------------------|----------|
| TF‑IDF                  | 10        | 500               | 0.6140   |
| TF‑IDF Weighted W2V     | 5         | 100               | 0.6215   |
| Feature Importance      | 10        | 500               | 0.6028   |

---

##  Key Takeaways
- **Semantic Intelligence:** TF‑IDF Weighted Word2Vec performed the best, showing that contextual meaning is more predictive than raw word frequency.
- **Explainability:** Decision Trees provide interpretable feature importance, highlighting which variables (e.g., essay sentiment, project cost) influence approval decisions.

---

##  Real‑World Applications
- **Risk & Approval Systems:** Adaptable for credit scoring, loan approvals, or insurance underwriting.  
- **Content Moderation:** Useful for platforms that need to prioritize or flag text submissions.  
- **EdTech Insights:** Helps optimize resource allocation and teacher support systems.  

---

## How to Run

### Clone the repository
```bash
git clone https://github.com/Krishna9676/donorschoose-dt-prediction.git


Install dependencies
pip install scikit-learn nltk pandas vaderSentiment prettytable


Run the notebook
jupyter notebook donors_Assignment_DT_ass_2022.ipynb



👤 Author
Murali krishna kaye
Connect with me on LinkedIn:www.linkedin.com/in/murali-krishna-k-9628a399


