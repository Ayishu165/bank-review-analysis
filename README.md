# bank-review-analysis
Task 1: Setup & Data Collection
Create GitHub repository for the project.
Add .gitignore to exclude unnecessary files.
Add requirements.txt listing required Python libraries (e.g., google-play-scraper, pandas, cx_Oracle, spacy).
Create and switch to branch task-1.
Use google-play-scraper to collect at least 400 reviews per bank (total 1200 reviews) including:
Review text
Rating
Review date
Bank name
Source
Preprocess reviews:
Remove duplicates
Handle missing data
Normalize dates to YYYY-MM-DD
Save cleaned data to CSV with columns:
review, rating, date, bank, source
            Commit preprocessing scripts and update README.md with methodology.

Task 2: Sentiment & Thematic Analysis
Switch to branch task-2.
     Use libraries (TF-IDF) to:
     Calculate sentiment scores (positive, neutral, negative)
     Aggregate sentiment by bank and rating
     Extract keywords and n-grams
     Group related keywords into 3–5 themes per bank and document the grouping logic.
     Save analysis results to CSV with columns:
     eview_id, review_text, sentiment_label, sentiment_score, identified_theme(s)
     Commit analysis scripts and merge task-2 branch via pull request.
Task 3: Store Cleaned Data in Oracle

Set up Oracle XE database (or fallback to PostgreSQL if needed).
create branch task-3 and switch into task-3
   Create database/schema bank_reviews.
   Define schema with two tables:
   BANKS1 (bank_id, bank_name)
   REVIEWS1 (review_id, review, rating, review_date, bank, source, translated_review, lang_detected, sentiment_label, sentiment_score, bank_id)
   Use Python with cx_Oracle to connect and insert cleaned review data.
   Commit insert scripts and confirm tables are populated with over 1,000 entries.
   Export SQL dump of database schema and data to GitHub.
