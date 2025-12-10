# Amazon-Feedback-Analysis
Objective: Uncover the drivers of customer sentiment and engagement in Amazon product reviews to inform product development and marketing strategies.
Data Cleaning: Standardized column names, parsed review dates, handled missing values in text and recommendation flags, and engineered features such as review length and sentiment polarity.
Data Analysis: Explored distributions of ratings and recommendation flags, identified top brands and categories by sentiment, examined the relationship between review length, helpfulness votes, and ratings.
Data Visualization: Employed bar charts for rating counts, word clouds for positive vs. negative reviews, scatter plots of helpful votes vs. review length, and heatmaps of sentiment across brands.
Insights: High ratings (4–5 stars) dominate but negative reviews contain recurring product-specific complaints; longer reviews tend to garner more helpful votes; certain brands/categories show consistently higher sentiment.
Deliverable: A thoroughly documented Jupyter Notebook with all code and outputs, plus a concise slide deck summarizing actionable findings and recommendations.
Extended Overview
Data Collection & Cleaning
Source & Scope: Loaded ~3,077 Amazon product reviews covering 13 fields—including review text, rating (1–5), recommendation flag, helpfulness votes, brand, and categories.
Preprocessing Steps:
Column normalization: Renamed fields to snake_case (e.g. reviews_date_added).
Date parsing: Converted reviews_date_added to datetime; noted only ~276 entries had dates, so time-based trend analysis was limited.
Missing data: Imputed missing reviews_do_recommend as “Unknown”; dropped any rows without review text.
Feature engineering:
Review length: Counted words in reviews_text.
Sentiment polarity: Computed using a lexicon-based approach to score each review from –1 (negative) to +1 (positive).
Helpfulness ratio: reviews_num_helpful divided by review length to normalize engagement.
Data Analysis
Rating & Recommendation Distribution:

Ratings: Approximately 70% of reviews are 4–5 stars; 1–2 star reviews represent ~15%.
Recommendation Flag: “doRecommend = True” aligns strongly with 4–5 star ratings; ~10% of high-rated reviews did not explicitly recommend.
Brand & Category Sentiment:
Brands A and B show average sentiment scores above 0.6, while Brand C averages 0.2 with frequent 1–2 star reviews.
Certain categories (e.g., Electronics) have wider sentiment variability versus more uniform categories like Books.
Textual Insights:
Word Cloud Analysis: Positive reviews frequently mention “quality,” “easy,” and “recommend,” while negative reviews highlight “defective,” “return,” and “battery.”
Length vs. Helpfulness: Longer reviews (200+ words) receive on average 2× more helpful votes than short reviews (<50 words).
Data Visualization
Bar Charts: Rating counts and recommendation rates by category.
Heatmap: Average sentiment polarity across top 10 brands and categories.
Word Clouds: Side-by-side for 5-star vs. 1-star reviews to contrast key terms.
Scatter Plot: Review length vs. number of helpful votes with a LOESS smoothing line.
Box Plots: Distribution of helpfulness ratio across rating levels
Trend Analysis
Sentiment Extremes: While most reviews are positive, negative reviews are more textually rich—offering deeper insights into pain points (e.g., durability, customer service).
Engagement Patterns: Reviews that include product comparisons or detailed pros/cons lists see the highest helpfulness ratios, indicating value in structured feedback.
Summary
This analysis distills the volumetric and semantic dimensions of Amazon product feedback. Key recommendations include prioritizing improvements on common defect areas, encouraging longer “pros and cons” style reviews to boost helpfulness and trust, and tailoring product messaging around features that drive the highest sentiment in your strongest-performing brands and categories.
