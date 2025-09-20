# TikTok Claim Classification Project

## 📌 Overview
This project was developed as part of **Course 2 - Get Started with Python** (Google Advanced Data Analytics Certificate).  
The scenario simulates a real-world data science task for **TikTok’s Trust & Safety team**, focusing on preparing data for a machine learning model that classifies whether statements in TikTok videos are **claims** or **opinions**.

The work follows the **PACE framework** (Plan, Analyze, Construct, Execute) to ensure a structured approach.

---

## 🎯 Objectives
- Import, inspect, and organize TikTok’s synthetic dataset (`tiktok_dataset.csv`).
- Perform exploratory data analysis (EDA) to understand data structure and quality.
- Identify variables correlated with **claim status** and **engagement levels**.
- Create meaningful variables (e.g., ratios such as likes per view, shares per view).
- Summarize insights for the TikTok data science team.

---

## 📂 Dataset
- **Rows:** 19,383 videos  
- **Columns:** 12  
- Each row represents a TikTok video containing a claim or opinion, with metadata such as:
  - `claim_status`: claim or opinion
  - `verified_status`: verified / not verified
  - `author_ban_status`: active / under review / banned
  - `video_view_count`, `video_like_count`, `video_share_count`, `video_download_count`, `video_comment_count`
  - `video_duration_sec`, `video_transcription_text`

---

## 🛠️ Methods
- Tools: **Python, Pandas, NumPy, Jupyter Notebook**
- Data inspection: `.head()`, `.info()`, `.describe()`
- Grouped aggregations: `groupby()`, `agg()`
- Feature engineering: created **likes_per_view**, **comments_per_view**, **shares_per_view**

---

## 📊 Key Findings
1. **Claims vs. Opinions**  
   - Claims: **9,608 videos (50.3%)**  
   - Opinions: **9,476 videos (49.7%)**:contentReference[oaicite:0]{index=0}

2. **Factors correlated with claim status**  
   - Claims are more common among authors with **banned or under review** status:contentReference[oaicite:1]{index=1}.  
   - Verified accounts are less likely to post claims.

3. **Factors correlated with engagement**  
   - Claims have **much higher average view counts** (~501k) compared to opinions (~4.9k):contentReference[oaicite:2]{index=2}.  
   - Engagement metrics (likes, shares, comments) are heavily skewed, with a small fraction of videos driving most activity.  
   - Content from banned authors often shows disproportionately high engagement before restrictions.

---

## 🚀 Next Steps
- Handle outliers and missing values to improve model quality.
- Use feature engineering (engagement ratios, text features from transcriptions).
- Ensure class balance between claims and opinions during model training.
- Proceed to hypothesis testing and predictive modeling (Course 3+).

---

## 🏆 Acknowledgments
This project is part of the **Google Advanced Data Analytics Professional Certificate (Course 2)** and uses synthetic data created in partnership with **TikTok**.
