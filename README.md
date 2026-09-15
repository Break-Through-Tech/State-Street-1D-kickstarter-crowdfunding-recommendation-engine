# Kickstarter Crowdfunding Recommendation Engine

> 💡 **Note for the team:** This README is still a work in progress. Sections below with example/placeholder text should be filled in as the project develops, and get feedback from your AI Studio Coach and Challenge Advisor before finalizing it.

---

### 👥 **Team Members**

| Name             | GitHub Handle | Contribution                                                             |
|------------------|---------------|--------------------------------------------------------------------------|
| Michelle Lin   | @michelllinstar | Data exploration, visualization, overall project coordination            |
| Hazera Sarker | @    | Data collection, exploratory data analysis (EDA), dataset documentation  |
| Nitya Vobugari    | @ | Data preprocessing, feature engineering, data validation                 |


---

## 🎯 **Project Highlights**

- Building a **binary classification model** that predicts whether a Kickstarter campaign will succeed or fail, using information available at campaign launch.
- Comparing multiple classification approaches — **Logistic Regression, K-Nearest Neighbors, and Decision Trees/Random Forest** — and evaluating them with Precision, Recall, F1 Score, and ROC-AUC (targeting ~80%+ accuracy).
- Identifying the campaign characteristics most associated with success (e.g., goal, duration, category, updates, reward levels) to keep the model interpretable, not just accurate.
- Prototyping a **recommendation framework** that translates model predictions into actionable guidance campaign creators could use to improve their odds of success.

---

## 👩🏽‍💻 **Setup and Installation**

**Provide step-by-step instructions so someone else can run your code and reproduce your results. Depending on your setup, include:**

* How to clone the repository
* How to install dependencies
* How to set up the environment
* How to access the dataset(s)
* How to run the notebook or scripts

---

## 🏗️ **Project Overview**

This project is part of the **Break Through Tech AI Studio (Fall 2026)** program, which pairs student fellows with host companies to work on real-world, industry-inspired machine learning challenges.

Our **AI Studio host company is State Street**, a financial services and banking holding company specializing in investment management and servicing. State Street operates at the intersection of financial services, data, technology, and analytics, providing context for exploring how machine learning can support data-driven decision-making. *(Note: this challenge does not use any State Street data.)*

**Objective:** Build a **Kickstarter Crowdfunding Recommendation Engine** that predicts whether a crowdfunding campaign will succeed or fail, using information available at campaign launch (e.g., funding goal, duration, category, location, reward levels). Beyond prediction, the project aims to identify the factors most associated with campaign outcomes and translate those insights into actionable recommendations for campaign creators — for example, flagging at-risk campaigns and suggesting adjustments that could improve their odds of success.

**Real-world significance:** Crowdfunding platforms like Kickstarter help entrepreneurs and creators raise capital outside traditional funding channels, but a large share of campaigns fail to reach their goals. A model that reliably predicts campaign outcomes — and explains *why* — could help creators design stronger campaigns before launch and help platforms surface early guidance to at-risk projects, mirroring the kind of predictive, explainable analytics used across financial services.

**What we're building:** A tool that predicts whether a Kickstarter project will succeed or fail, and surfaces what factors could help a project perform better. The primary users are people creating Kickstarter campaigns — the model and its insights can help them make better choices (e.g., goal size, duration, category, reward structure) and improve their chances of reaching their funding goal.

**Market:** This project sits in the crowdfunding space, focused specifically on U.S.-based Kickstarter projects.

**Stakeholders:** Our team, our AI Studio Coach and Challenge Advisor, and State Street and Break Through Tech more broadly — all of whom care about the quality, interpretability, and practical usefulness of the model, not just raw accuracy.

**Success metrics:**
- **Model performance:** ~80%+ accuracy, alongside strong Precision, Recall, and ROC-AUC.
- **Model comparison:** Identify the best-performing classification approach across the models we test.
- **Interpretability:** Clearly explain the campaign characteristics most associated with success.
- **Recommendation value:** By end of November, deliver a prototype recommendation framework that turns model predictions and key features into actionable guidance for at-risk campaigns.

**Ethical considerations:** The historical dataset may not represent all project categories equally, so we're checking for imbalances that could bias recommendations toward or against particular groups. We're also guarding against data leakage by only using features available at campaign launch, and we're careful not to present predictions as guarantees — they reflect patterns in historical data, not certainty about any individual campaign.

See [Challenge-Project-Overview.md](Challenge-Project-Overview.md) for the full challenge brief, dataset details, milestones, and suggested approach from our Challenge Advisor, and [Project-Brief-and-Workplan.md](Project-Brief-and-Workplan.md) for our team's full project brief, risks, tools, and workplan.

---

## 📊 **Data Exploration**

**Dataset:** [Kickstarter Projects dataset](https://www.kaggle.com/parienza/kickstarter) (publicly available on Kaggle). Structured/tabular data with numerical, categorical, and date/time campaign attributes — including project ID, name, URL, category/subcategory, location, status, goal, pledged amount, funded percentage, backers, funded date, reward levels, updates, and comments. The original source data has ~45,957 rows and 17 columns; after filtering to successful/failed U.S. campaigns and removing missing values, the reference dataset has ~38,491 rows and 18 columns.

**Planned approach:**
* Filter to successful/failed U.S.-based campaigns and handle missing values, duplicates, and inconsistent category labels.
* Explore the distribution of successful vs. failed campaigns, and relationships between success and features like goal amount, duration, category, updates, and reward levels using summary statistics, histograms, and box plots.
* Engineer features (e.g., campaign duration, goal-to-pledge ratios, category encodings) that are available at campaign launch, avoiding data leakage from post-launch outcomes.

*(EDA insights and visualizations will be added here as the analysis progresses.)*

---

## 🧠 **Model Development**

**Planned models:** Logistic Regression as an interpretable baseline, compared against K-Nearest Neighbors and Decision Trees/Random Forest (with XGBoost/LightGBM as optional advanced comparisons).

**Approach:** Compare models on Accuracy, Precision, Recall, F1 Score, and ROC-AUC; explore feature selection and hyperparameter tuning to see whether they materially improve results; use tools like SHAP to assess model interpretability and explain which features drive predictions.

*(Training setup, final model choice, and tuning details will be documented here as modeling progresses.)*


---

## 📈 **Results & Key Findings**

**You might consider describing the following (as applicable):**

* Performance metrics (e.g., Accuracy, F1 score, RMSE)
* How your model performed
* Insights from evaluating model fairness

**Potential visualizations to include:**

* Confusion matrix, precision-recall curve, feature importance plot, prediction distribution, outputs from fairness or explainability tools

---

## 🚀 **Next Steps**

**Project milestones:**
* **By 09/30:** Complete EDA and initial data cleaning — filter to U.S. campaigns, address missing fields, perform feature engineering.
* **By 10/31:** Analyze associations between funding outcomes and key features (goal, duration, updates, location, category/subcategory, reward levels).
* **By 11/30:** Build and compare baseline and advanced classification models, run feature selection/engineering, evaluate performance and interpretability, and prototype the recommendation framework for at-risk campaigns.

*(Model limitations, what we'd do differently, and future directions will be added here after modeling is complete.)*

---

## 📝 **License**

Specify how your project can be used by others. Choose an appropriate license and link it here (e.g., MIT, Apache 2.0). Make sure your Challenge Advisor approves of the selected license type. 

**Example:**
This project is licensed under the MIT License.

---

## 📄 **References** (Optional but encouraged)

Cite relevant papers, articles, or resources that supported your project.

---

## 🙏 **Acknowledgements** (Optional but encouraged)

Thank your Challenge Advisor, host company representatives, TA, and others who supported your project.
