<div align="center">
  <h1>Data Science, Database Management, AI & Machine Learning Researches</h1>
</div>

## Contents
1. [Driver's Choice: $1.1M+ and Counting](#drivers-choice-11m-and-counting-ai-powered-fuel-optimization-for-nyc-taxi-drivers): Machine Learning, Predictive Analytics, Python, SQL, Streamlit, XGBoost, Data Engineering, Statistical Analysis
2. [End-to-End Machine Learning Project in Python](#): Real Estate Price Prediction with XGBoost, Data Engineering, and Model Optimization
3. [Project Not Uploaded Yet](#)
4. [Project Not Uploaded Yet](#)

---

## Driver's Choice: $1.1M+ and Counting (AI-Powered Fuel Optimization for NYC Taxi Drivers)
**Machine Learning | Data Science | Predictive Analytics | Python | SQL | Streamlit | XGBoost | Data Engineering | Statistical Analysis**

> ***Testomonial #1:** Thank you, Mohammed! I can't believe this, yaar! I was little scared for hybrid, you know, new technology and all. But the money I save every month, oh my god, it's too much, man!*
> 
> ***Testomonial #2:** Tumhe pata nahi yaar, hybrid lene se gas kitna save ho raha hai! Pehle jo paisa har mahine gas par jaata tha, ab wo bacha ke rakhta hoon!*
>
> ***Testomonial #3:** $400 bach gaya har mahina aur koi shor nahi! Best decision, bhai! Pichhe socha, yeh karte to achha hota. 15 saal se NYC mein chala raha hoon! Nahi jaana tha ki itna paisa bachaya jaa sakta hai.*

*[_View the Full Project_](https://github.com/tech-moh-logy/Data-AI/tree/main/Driver's%20Choice)*

An AI-driven, end-to-end data science solution built to transform how NYC taxi drivers select vehicles — maximizing fuel efficiency, boosting profitability, and reducing environmental impact. This project merges rigorous statistical validation with **advanced machine learning** to deliver real-world results. By developing an XGBoost model to forecast long-term fuel **cost savings** across hybrid, non-hybrid, and EV vehicles, and building a **full ML pipeline from data collection to deployment**, the system **achieved over $1.1M in economic value**, including $150K+ in **verified** fuel savings and up to $15K saved per driver over 20 months. With over 30 NYC taxi drivers influenced, the solution empowered more informed decision-making and encouraged sustainable practices. A **dynamic Streamlit dashboard** delivered real-time, personalized recommendations, while **statistical testing (t-tests, ANOVA)** confirmed significant differences in fuel efficiency. The project leveraged **Python, SQL, and Excel alongside tools like Streamlit, XGBoost, and scikit-learn**, and even explored experimental modeling with **TensorFlow and PyTorch**. By leveraging firsthand, **high-frequency data collected over ten weeks**, the **model avoided reliance on potentially outdated or generalized assumptions**. This ground-truth approach allowed for more accurate feature engineering, more nuanced training, and ultimately, a model that better reflects how people actually drive, spend, and decide in the real world.

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

## Database Design: 

# Social Media Application Relational Database Schema Design and Implementation

This project encompassed the complete design and implementation of a normalized relational database schema to underpin the core functionalities of a social media application. The primary objective was the creation of a well-structured, efficient, and maintainable database model optimized for managing user entities, textual content (tweets), content categorization via hashtags, directed acyclic graph (DAG)-like user relationships (following), and user-content affinity through likes.

The schema is composed of several logically distinct and interconnected entities, represented by the following tables:

* **`Users`**: Stores user entity attributes, including a surrogate primary key (`user_id`), immutable unique identifiers (`username`, `email`), hashed credentials (`password_hash`, `password_salt`), profile metadata, privacy configurations (`is_private`), role-based access control (`role`), and temporal metadata (`created_at`, `updated_at`).
* **`Tweet`**: Persists user-generated textual content, featuring a surrogate primary key (`tweet_id`), a foreign key referencing the `Users` table (`user_id`) with a cascading delete rule for referential integrity, content adhering to a character limit (`content`), a timestamp of creation (`time_tweeted`), and temporal audit columns (`created_at`, `updated_at`).
* **`Hashtags`**: Stores unique hashtag entities, utilizing a surrogate primary key (`hashtag_id`) and enforcing uniqueness on the hashtag text (`hashtag_name`) via a `UNIQUE` constraint.
* **`Follow`**: Implements the user following relationship as a self-referencing many-to-many association on the `Users` entity. It employs a composite primary key (`follower_id`, `followee_id`) to prevent duplicate follow relationships and leverages foreign keys referencing `Users` with cascading delete rules to maintain referential integrity.
* **`LikeTweet`**: Models the user's affinity for tweets through a many-to-many relationship between the `Users` and `Tweet` entities. It utilizes a surrogate primary key (`like_id`) and foreign keys referencing both `Users` and `Tweet` with cascading delete rules. The `created_at` timestamp records when the like occurred.
* **`TweetHashtag`**: Resolves the many-to-many relationship between `Tweet` and `Hashtags`, employing a composite primary key (`tweet_id`, `hashtag_id`) and foreign keys referencing both tables with cascading delete rules.

The design rigorously applies normalization principles to minimize data redundancy and enhance data integrity. The strategic use of `UNIQUE` constraints on natural keys (`username`, `email`, `hashtag_name`), `NOT NULL` constraints to enforce data presence, and `FOREIGN KEY` constraints with `ON DELETE CASCADE` actions ensures transactional consistency and referential integrity across the database.

The inclusion of sample Data Manipulation Language (DML) statements demonstrates the population of the defined schema. Furthermore, analytical Structured Query Language (SQL) queries illustrate the capacity to derive meaningful insights, such as identifying users with the highest follower count and retrieving chronologically ordered tweets associated with specific hashtag entities.

This project showcases a comprehensive understanding of relational database theory, logical data modeling methodologies, and critical database management considerations for architecting a robust and potentially scalable application backend. The design emphasizes data integrity, efficient data organization leveraging appropriate indexing strategies (implicitly considered), and the facilitation of complex relational queries for application logic and data analytics.

*[_View the Full Project_](#)*

<sub>[⬅ Back to Contents](#contents)</sub>

---

## The Motions: 

[Project Not Uploaded Yet]

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
