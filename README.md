# A Text Mining Study of Argonaut Hotel Guest Reviews (2024–2025)

This project analyzes 1,120 guest reviews of the Argonaut Hotel (San Francisco) collected from **TripAdvisor, Google, Yelp, Reddit, and Facebook (2024–2025)**. Using text mining **(EDA, topic modeling, sentiment analysis, and clustering)** to uncover what guests talk about most and turn unstructured feedback into actionable insights for hotel service and reputation management. This project focuses on cross-platform review analysis.

# Cleaning
- Removed spam / meaningless / AI-generated reviews
- Removed nulls + duplicates
- Fixed encoding issues, removed URLs, stripped HTML (BeautifulSoup)
- Lowercased text, normalized whitespace
- Additional preprocessing depending on model (stopwords, lemmatization, etc.)

# Methods
### 1) Exploratory Data Analysis (EDA)
- Text length distributions
- Lexical frequency + word clouds
- N-gram analysis
- POS tagging + NER (spaCy)

### 2) Topic Modeling
Compared multiple topic models:
- **LDA**
- **NMF**
- **BERTopic**

**LDA was selected as the most practical** due to clearer, more interpretable topics.

**LDA topics (4):**
1. Excellent Location & Nearby Attractions  
2. Friendly Staff & Exceptional Service  
3. Parking & Service Concerns  
4. Scenic Views & Hotel Aesthetic  

### 3) Sentiment Analysis
Models used:
- **TextBlob**
- **VADER**
- **BERT**

Overall sentiment trends showed **positive sentiment dominating**, and TextBlob was the most balanced performer.

### 4) Clustering
- Vectorization: **TF-IDF**
- Model: **K-Means**
- Best K chosen by elbow method (**K = 5**)
- PCA visualization for cluster interpretation


## Key Findings
- Guests most consistently praise **location** and **staff/service**
- Positive sentiment dominates across topics, with issues most commonly appearing around **parking/pricing transparency** and occasional **guest/security concerns**
- Clustering results align with topic modeling themes, increasing confidence in patterns

## Recommendation:
- Be transparent about parking/extra fees (show total cost upfront).
- Improve valet/parking flow (reduce waits, clearer communication).
- Keep investing in staff service quality (biggest strength).
- Promote location/views more and add easy guest guides (maps/QR tips).
- Tighten security + incident response for occasional safety concerns.


## Limitations
- Sentiment/clustering may miss subtle emotions or cultural nuance
- No time-series trend tracking ( seasonality, renovations)
- Cross-platform differences (formats, rating systems, user behavior)
