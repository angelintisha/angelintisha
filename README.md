<div align="center">

# Data Science & Analytics Portfolio

</div>

---

| Category | Projects |
|---|---|
| 🤖 AI & Machine Learning | [ClinTrialMatch — Clinical Trial Site Recommendation Engine](#1-clintrialmatch--clinical-trial-site-recommendation-engine) · [HEALTHPLUS US — Member Segmentation & Retention Analysis](#2-healthplus-us--member-segmentation--retention-analysis) · [Academic Advising Assistant — RAG & LLM Chatbot](#3-academic-advising-assistant-using-rag--llm) · [Earnings Report Summarizer — LangChain & LLM](#4-earnings-report-summarizer--langchain--llm) · [Bank Loan Prediction — Logistic Regression](#5-bank-loan-response-prediction--logistic-regression) |
| 🗄️ Database & Data Engineering | [Travel Vaccination Advisory System — Relational Database Design](#6-travel-vaccination-advisory-system) |
| 📈 Business Intelligence & Analytics | [Voltex Electronics — Sales Performance Analysis](#7-voltex-electronics--sales-performance-analysis) · [Weather & Sales Analysis — Descriptive Stats & KNN](#8-weather--sales-analysis--k-nearest-neighbors) · [Bike Buyer Analysis — Customer Segmentation Dashboard](#9-bike-buyer-analysis) |

---

### 🤖 AI & Machine Learning

#### 1. ClinTrialMatch — Clinical Trial Site Recommendation Engine
[View Repository](https://github.com/angelintisha/clintrialmatch) · [Live App](https://tishaangelin.shinyapps.io/clintrialmatch/)

`R` `Shiny` `shinyapps.io` `Content Filtering` `Similarity Scoring`

Built a web application in R/Shiny implementing a 5-step recommendation pipeline — content filtering by trial phase and therapeutic area, similarity scoring across 4 normalized site attributes (enrollment rate, screen failure rate, PI experience, infrastructure), dynamic urgency-based weighting, collaborative filtering proxy via region bonus, and composite ranking — applied against a database of 20 U.S. investigator sites. Deployed live on shinyapps.io with no API or login required. Phase III Oncology (West, Accelerated) surfaces Stanford and MD Anderson with 94–96/100 match scores; Phase I Cardiology (East, Standard) surfaces Penn Medicine and Johns Hopkins, confirming the engine differentiates meaningfully across inputs. Addresses a critical gap in the $50B+ clinical trial market where site selection is entirely manual — a leading cause of the 80% of trials that miss enrollment timelines, costing sponsors $600K–$8M per month of delay — replacing enterprise CTMS tools priced at $50K–$500K/year with a zero-cost, browser-accessible prototype.

---

#### 2. HEALTHPLUS US — Member Segmentation & Retention Analysis
[View Repository](https://github.com/angelintisha/HealthPlus-US-Member-Segmentation-And-Retention-Analysis)

`Python` `Pandas` `Scikit-learn` `XGBoost` `Jupyter`

Conducted end-to-end churn analysis on 500,000 health insurance policyholder records in Python (Pandas, Scikit-learn, XGBoost), resolving 30+ data quality issues across enrollment, claims, and demographic fields before modeling. Applied RFM segmentation to identify high-value member clusters and ran 7 statistical hypothesis tests to validate key churn drivers; built an XGBoost classification model (AUC: 0.663) for churn prediction, a CLV regression model (R²: 0.729) for lifetime value estimation, and a 24-month Exponential Smoothing forecast to project membership trajectories. Delivered targeted retention recommendations for at-risk member segments, enabling health plan teams to prioritize intervention spend toward highest-CLV policyholders — where a 1% reduction in voluntary disenrollment can represent millions in preserved annual premium revenue.

---

#### 3. Academic Advising Assistant using RAG & LLM
[View Repository](https://github.com/angelintisha/Academic-Advising-Assistant-Using-Retrieval-Augmented-Generation)

`Python` `LangChain` `ChromaDB` `Ollama (llama3.2)` `Streamlit`

Built a Retrieval-Augmented Generation (RAG) chatbot in Python using LangChain for orchestration, ChromaDB as the vector store, and a locally hosted LLM (Ollama/llama3.2) for inference, ingesting 5 institutional document types (program handbooks, course catalogs, policies, FAQs, advising guides) into a semantic search pipeline and deploying the interface via Streamlit. The system achieved accurate, grounded responses across 7 distinct advising question categories by anchoring all outputs to retrieved source documents, eliminating hallucination. Demonstrates a production-ready RAG architecture directly applicable to high-stakes healthcare settings — clinical protocol Q&A, regulatory guidance retrieval, and patient-facing advisory systems — where LLM accuracy and full auditability are non-negotiable requirements.

---

#### 4. Earnings Report Summarizer — LangChain & LLM
[View Repository](https://github.com/angelintisha/earnings-report-summarizer)

`Python` `LangChain` `Ollama (llama3.2)` `Prompt Engineering`

Built a structured financial document summarizer using LangChain document loaders, a custom prompt template enforcing a six-section output format (Financial Highlights, Segment Highlights, Cash Flow & Capex, Strategic Moves, Key Risks), and a locally hosted LLM (Ollama/llama3.2) for inference — applied to Nvidia's Q2 FY2025 earnings report. The pipeline joins multi-page documents into a single text block, passes them through a structured PromptTemplate, and produces consistent, auditable summaries with no external API or internet connection required at runtime. Demonstrates a prompt engineering and LangChain architecture directly transferable to healthcare document summarization — e.g., clinical study reports, regulatory submissions, and adverse event narratives.

---

#### 5. Bank Loan Response Prediction — Logistic Regression
[View Repository](https://github.com/angelintisha/bank-loan-prediction)

`Python` `Pandas` `Scikit-learn` `Logistic Regression`

Built a binary classification model predicting whether a bank customer will respond to a personal loan offer, using logistic regression on 5,000 customer records with demographic and relationship attributes (age, income, education, family size, credit card spend, account holdings). Resolved dummy variable encoding for the Education column, applied a 60/40 train/test split, and evaluated model performance using confusion matrices and accuracy scores on both sets — achieving similar train and test accuracy, confirming the model is not overfitting. Extended the model to predict loan response for a new customer profile (Age=40, Income=84K, Graduate education), demonstrating an end-to-end classification workflow from data preparation through prediction.

---

### 🗄️ Database & Data Engineering

#### 6. Travel Vaccination Advisory System
[View Repository](https://github.com/angelintisha/Travel-Vaccination-Advisory-System-DB)

`Oracle SQL` `Relational Database Design` `ERD Modeling` `BCNF Normalization`

Designed and implemented a fully normalized (BCNF) relational database for a Travel Vaccination Clinic in Oracle SQL, modeling 10 entities and 11 foreign key relationships spanning patient profiles, destination risk scores, vaccine schedules, treatment recommendations, and appointment records, with DDL/DML scripts and analytical SQL queries built to automate advisory report generation. The database handles the full advisory workflow — from patient intake to risk-stratified vaccine recommendation — with referential integrity enforced across all 11 FK relationships and patient-specific schedules returned in a single pass across joined tables. The system automates a manual, error-prone clinical advisory process and demonstrates relational database architecture directly applicable to EHR systems, clinical data repositories, and CDISC-compliant trial databases.

---

#### 7. Voltex Electronics — Sales Performance Analysis
[View Repository](https://github.com/angelintisha/Voltex-Electronics-Sales-Performance-Analysis)

`Excel` `Tableau`

Cleaned and analyzed 108,127 global e-commerce orders for a multinational electronics retailer in Excel, resolving 15 data quality issues including duplicates, null values, and currency inconsistencies across regional datasets, before building an interactive Tableau dashboard with filters by region, product category, and time period to surface revenue trends and performance drivers. Analysis identified a COVID-driven 3x revenue spike peaking at $883K monthly and revealed that the top 3 products drove 85% of $24M in total revenue, alongside regional concentration and seasonal demand patterns across 4 years of order data. Findings directly support marketing spend reallocation toward top-performing SKUs and inventory planning ahead of demand peaks; the revenue concentration insight additionally flags supply chain risk and informs product diversification strategy.

---

### 📈 Business Intelligence & Analytics

#### 8. Weather & Sales Analysis + K-Nearest Neighbors
[View Repository](https://github.com/angelintisha/weather-sales-knn)

`Python` `NumPy` `Matplotlib` `KNN`

Analyzed a daily weather and sales dataset using NumPy Boolean array filtering to identify that high-sales days (sales > $500K) are warmer on average than all days in the dataset, visualized the three-variable relationship between temperature, precipitation, and sales using marker-differentiated scatter plots, and converted temperature readings from Fahrenheit to Celsius across the full array. Extended the analysis with a manual K-Nearest Neighbors implementation (no sklearn) to find the 5 most similar stocks to a query profile (4.5% growth, $4B market cap, 0.5 risk), applying min-max normalization across all features before computing Euclidean distances — demonstrating that feature scaling is essential for distance-based similarity methods.

---

#### 9. Bike Buyer Analysis
[View Repository](https://github.com/angelintisha/Bike-Buyer-Analysis)

`Excel` `Pivot Tables` `Interactive Dashboard`

Cleaned and analyzed 1,000 customer records across 13 demographic attributes (income, age, gender, commute distance, region, marital status, education, occupation, home ownership) in Excel, building an interactive dashboard with pivot tables, dynamic charts, and slicers for marital status, region, and education level to explore purchase behavior across customer segments. Analysis found that middle-aged customers (31–54) purchased bikes at the highest rate, that higher income correlated with purchase across both genders, and that customers with 0–1 mile commutes were most likely to purchase — indicating leisure-use rather than commute-driven demand. Findings provide a customer profile framework for targeted marketing, prioritizing mid-career, higher-income customers with short commutes for outreach and campaign spend.
