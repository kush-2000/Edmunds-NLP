# Edmunds Forum Analysis: Entry-Level Luxury Performance Sedans

This project analyzes 5,284 user-generated posts from Edmunds’ discussion forum on entry-level luxury performance sedans using Selenium-based web scraping and advanced NLP techniques. It evaluates word frequency distributions, brand mentions, customer aspirations, and brand associations using metrics like lift values and multidimensional scaling (MDS).

---

## 🛠️ Technologies Used

- **Python Libraries:**  
  - `selenium` – for automated web scraping  
  - `nltk`, `re`, `collections` – for text processing  
  - `pandas`, `numpy`, `matplotlib`, `seaborn` – for data handling and visualization  
  - `statsmodels`, `scipy` – for regression and statistical analysis  
  - `sklearn.manifold.MDS` – for multi-dimensional scaling analysis  

---

## 📌 Project Breakdown

### 1. **Web Scraping**
Scraped discussions from 106 pages of the Edmunds forum thread using Selenium, collecting the author, date, and comment of each post.

### 2. **Data Preprocessing**
- Replaced car models with their corresponding brands using a CSV mapping.
- Cleaned text by removing punctuation and converting to lowercase.
- Tokenized words for frequency and co-occurrence analysis.

### 3. **NLP Analysis**
- Generated word frequency tables and performed Zipf’s law validation.
- Identified top 10 most mentioned car brands and top 6 most discussed attributes.
- Highlighted aspirational phrases (e.g., "wish to", "plan to") and unified them into a single label “Aspiration”.

### 4. **Statistical Testing**
Performed OLS regression to evaluate whether Zipf’s law holds. Found that the estimated β = -1.14 is statistically different from -1 (p < 0.05), rejecting Zipf’s law for this dataset.

### 5. **Association Rule Mining**
- Computed **lift values** for:
  - Brand–Brand co-mentions
  - Brand–Attribute relationships
  - Brand–Aspiration co-mentions
- Visualized findings using heatmaps and MDS plots to explore brand positioning and user sentiment clusters.

---

## 📈 Key Findings

- **Top Brands:** BMW, Audi, Acura, Honda, Subaru.
- **Notable Observations:**
  - Acura was often mentioned alongside Subaru—unexpected due to market segment difference.
  - Audi and Volkswagen had strong co-mentions despite different brand positioning.
  - Hyundai had the strongest co-mention with aspirational terms.
  - Surprisingly, BMW had a below-average lift for “performance”.

---

## 📌 Recommendation

As BMW is assumed to be the client, we recommend:

1. **Explore Competitor Overlap:** Focus on value-driven segments where non-luxury brands like Subaru and Hyundai are gaining traction.
2. **Monitor Customer Sentiment:** Systematic sentiment tracking from online forums can help prevent customer churn and improve messaging strategies.

---
