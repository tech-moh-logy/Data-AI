<div align="center">
  <h1>Data Science, Database Management, AI & Machine Learning Researches</h1>
</div>

## Contents
1. [Driver's Choice: $1.1M+ and Counting](#drivers-choice-11m-and-counting-ai-powered-fuel-optimization-for-nyc-taxi-drivers): Machine Learning, Predictive Analytics, Python, SQL, Streamlit, XGBoost, Data Engineering, Statistical Analysis
2. [End-to-End Machine Learning Project in Python](#end-to-end-machine-learning-project-in-python-real-estate-price-prediction-with-data-pipelines-correlation-analysis-and-cross-validation): Real Estate Price Prediction with Data Pipelines, Correlation Analysis, and Cross-Validation
3. [Database Design: Social Media Application Relational Database Schema Design and Implementation](#database-design-social-media-application-relational-database-schema-design-and-implementation)
4. [Savatar - Interactive AI Chatbot](#)
5. [MotionWise Fitness](#)

---

## Driver's Choice: $1.1M+ and Counting (AI-Powered Fuel Optimization for NYC Taxi Drivers)
**Machine Learning | Data Science | Predictive Analytics | Python | SQL | Streamlit | XGBoost | Data Engineering | Statistical Analysis**

> ***Testomonial #1:** Thank you, Mohammed! I can't believe this, yaar! I was little scared for hybrid, you know, new technology and all. But the money I save every month, oh my god, it's too much, man!*
> 
> ***Testomonial #2:** Tumhe pata nahi yaar, hybrid lene se gas kitna save ho raha hai! Pehle jo paisa har mahine gas par jaata tha, ab wo bacha ke rakhta hoon!*
>
> ***Testomonial #3:** $400 bach gaya har mahina aur koi shor nahi! Best decision, bhai! Pichhe socha, yeh karte to achha hota. 15 saal se NYC mein chala raha hoon! Nahi jaana tha ki itna paisa bachaya jaa sakta hai.*

*[_View the Full Project_](https://github.com/tech-moh-logy/Data-AI/tree/main/Driver's%20Choice)*

This AI-driven, end-to-end data science solution is built to transform how NYC's high-mileage taxi drivers select vehicles, maximizing fuel efficiency, boosting profitability, and reducing environmental impact. By merging rigorous statistical validation with advanced machine learning, we aim to deliver real-world results tailored to the unique demands of drivers who work long hours.

Our system develops an XGBoost model to forecast long-term fuel cost savings across hybrid and non-hybrid vehicles, leveraging firsthand, high-frequency data collected from drivers with similar work patterns. This ground-truth approach allows for more accurate feature engineering and nuanced training, avoiding reliance on generalized assumptions.

The initial phase has demonstrated the potential to save **up to $15K per driver over 20 months** in verified fuel savings for early adopters. We have influenced over 10 NYC taxi drivers, empowering more informed decision-making. A dynamic Streamlit dashboard delivers real-time, personalized recommendations. Initial statistical testing shows promising differences in fuel efficiency, with ongoing data collection to further strengthen our validation.

**Looking ahead, we project a potential economic value exceeding $1.1M** as the benefits of this solution spread through the driver community via word-of-mouth and wider adoption. This projection is based on the anticipated "rippling effect" of successful early adoption and the continued savings for a larger user base.

We are building a full ML pipeline from data collection to deployment, utilizing Python, SQL, Excel, Streamlit, XGBoost, and scikit-learn. Our vision is to empower more informed decision-making within this vital community, encouraging sustainable practices and realizing this significant potential economic value.

**Project Scope and Intent:** This is a localized, personal data science project undertaken to explore the fuel efficiency and cost savings of different vehicle types (specifically EVs and Hybrids) for a niche group of NYC taxi drivers I know personally – those with demanding schedules. The findings and models developed are primarily intended to inform decision-making within my immediate circle of family and friends in the taxi industry. **There are no plans to develop this into a public website, application, or widely distributed tool.**

<sub>[⬅ Back to Contents](#contents)</sub>


---

## End-to-End Machine Learning Project in Python: Real Estate Price Prediction with Data Pipelines, Correlation Analysis, and Cross-Validation
**scikit-learn | Machine Learning | Predictive Analytics | Python | Data Engineering | Statistical Analysis | Data Visualization | Jupyter Notebook | Model Evaluation**

This project showcases a comprehensive machine learning pipeline designed to predict housing prices using real-world data. With a focus on real-world applicability, it integrates key data science principles to solve a business problem faced by real estate companies: accurately forecasting property prices based on a variety of features.

The solution involves a structured end-to-end workflow, from data ingestion and cleaning to model training, evaluation, and deployment. The model takes into account various attributes such as location, size, and other critical factors, ensuring that predictions reflect actual market trends. 

### Workflow Highlights:
- **Data Loading & Cleaning:** Reading CSV data using `pandas`, inspecting distributions, identifying missing values
- **Exploratory Data Analysis:** Summary statistics (`describe()`), data visualization with `matplotlib`, correlation analysis
- **Data Splitting Techniques:**
  - Manual train-test split
  - scikit-learn’s `train_test_split`
  - `StratifiedShuffleSplit` for preserving data distribution
- **Feature Engineering:** Attribute combination testing, correlation-based feature selection
- **Handling Missing Values:** Using `SimpleImputer` for imputation
- **Pipeline Creation:** Building reusable data preprocessing and modeling pipelines
- **Model Selection & Training:** Training multiple models to compare performance
- **Model Evaluation:** Using metrics and **cross-validation** for robust evaluation
- **Model Serialization:** Exporting the trained model using `joblib`
- **Deployment Simulation:** Loading the saved model and testing on unseen data

*[_View the Full Project_](#)*

<sub>[⬅ Back to Contents](#contents)</sub>

---

## Savatar - Interactive AI Chatbot: Dynamic Responses and Personalized Engagement  
**Artificial Intelligence | Natural Language Processing | Google Gemini API | JavaScript | HTML | CSS**

An interactive chatbot powered by the **Google Gemini API**, designed to deliver dynamic, context-aware responses. By integrating NLP capabilities, this chatbot offers personalized conversations tailored to user inquiries. With features like **image uploads** and an **emoji picker**, it provides an engaging user experience. 

### Key Highlights:
- **Dynamic Conversations**: Leverages Google Gemini API for real-time, contextual responses.
- **Personalization**: Easily customizable to reflect company-specific information, enhancing user engagement.
- **Interactive Features**: Image uploads and emoji picker for enriched user interactions.
- **Simple Integration**: API key configuration allows for seamless setup and easy updates.

This project demonstrates the potential of combining AI and NLP to create adaptable, user-centric solutions for various use cases, from customer support to interactive content.

*[_View the Full Project_](#)*

<sub>[⬅ Back to Contents](#contents)</sub>

--

## Database Design: Social Media Application Relational Database Schema Design and Implementation

This project involved designing and implementing a relational database schema to support the core features of a social media application. The goal was a well-structured, efficient, and maintainable database for managing users, their posts (tweets), social connections, and content organization.

The schema includes the following key tables:

* **Users**: Stores user information, using `user_id` as the primary key and ensuring unique usernames and emails. It includes fields for profile details, privacy settings, and user roles, along with creation and update timestamps. Password security is handled using hashing and salting.
* **Tweet**: Stores user posts, with `tweet_id` as the primary key. It links back to the user who posted it (`user_id`) and includes the tweet content, timestamp, and audit fields. Deleting a user will also remove their tweets.
* **Hashtags**: Stores unique hashtags, with `hashtag_id` as the primary key and a unique constraint on the hashtag text.
* **Follow**: Manages the following relationships between users, using a combination of `follower_id` and `followee_id` as the primary key to prevent duplicates. Deleting a user will also remove their follow relationships.
* **LikeTweet**: Records which users liked which tweets, using `like_id` as the primary key and linking to both the user and the tweet. Deleting a user or a tweet will also remove the corresponding likes.
* **TweetHashtag**: Connects tweets to hashtags, using a combination of `tweet_id` and `hashtag_id` as the primary key. Deleting a tweet or a hashtag will also remove the corresponding entries here.

The design prioritizes data integrity through the use of primary and foreign keys, unique constraints, and the `ON DELETE CASCADE` rule where appropriate. Sample data insertions and basic analytics queries were also developed to demonstrate data population and retrieval capabilities, such as finding top users by follower count and listing tweets by hashtag.

*[_View the Full Project_](https://github.com/tech-moh-logy/Data-AI/blob/main/social_media_db_design.sql)*

<sub>[⬅ Back to Contents](#contents)</sub>

---

## MotionWise Fitness: 

[Project Not Uploaded Yet]

Tired of miscounting push-ups and wondering if you're getting the most out of your workout? This AI project automatically counts your repetitions by tracking your movements, ensuring accuracy for effective exercise. By eliminating manual counting, it helps prevent overexertion, promotes healthy blood flow, and encourages proper form for better results. Imagine exercising with confidence, knowing every up and down is precisely recorded thanks to intelligent IoT tracking.

*[_View the Full Project_](#)*

<sub>[⬅ Back to Contents](#contents)</sub>

---

<sub>
  
  ### Credits
  
  Research conducted by MOHAMMED, unless otherwise specified in the respective document.
  
  ### License
  
  This project is licensed under the [MOHAMMED LICENSE](https://github.com/tech-moh-logy/MOHAMMED-License/blob/main/README.md). For more details, see the [MOHAMMED LICENSE](https://github.com/tech-moh-logy/MOHAMMED-License/blob/main/README.md) file.

  <br>

  More available on request. Contact me via [LinkedIn](https://www.linkedin.com/in/mohtech/).
   
</sub>
