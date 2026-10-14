<div align="center">

# Data Science & Analytics Portfolio

</div>

---

| Category | Projects |
|---|---|
| 🤖 AI & Machine Learning | [HEALTHPLUS US — Member Segmentation & Retention Analysis](#1-healthplus-us--member-segmentation--retention-analysis) · [Academic Advising Assistant — RAG & LLM Chatbot](#2-academic-advising-assistant-using-rag--llm) · [ClinTrialMatch — Clinical Trial Site Recommendation Engine](#3-clintrialmatch--clinical-trial-site-recommendation-engine) · [Earnings Report Summarizer — LangChain & LLM](#4-earnings-report-summarizer--langchain--llm) · [Bank Loan Prediction — Logistic Regression](#5-bank-loan-response-prediction--logistic-regression) |
| 🏥 Healthcare AI Strategy & Research | [Severity-Specific EMS Demand Forecasting — AI & BI Proposal](#6-severity-specific-ems-demand-forecasting--ai--bi-proposal) |
| 🗄️ Database & Data Engineering | [Travel Vaccination Advisory System — Relational Database Design](#7-travel-vaccination-advisory-system) |
| 📈 Business Intelligence & Analytics | [Offshore Delivery Center Site Selection — Tableau Decision Dashboard](#8-offshore-delivery-center-site-selection--tableau-decision-dashboard) · [Voltex Electronics — Sales Performance Analysis](#9-voltex-electronics--sales-performance-analysis) · [Weather & Sales Analysis — Descriptive Stats & KNN](#10-weather--sales-analysis--k-nearest-neighbors) · [Bike Buyer Analysis — Customer Segmentation Dashboard](#11-bike-buyer-analysis) |

---

### 🤖 AI & Machine Learning

#### 1. HEALTHPLUS US — Member Segmentation & Retention Analysis
[View Repository](https://github.com/angelintisha/HealthPlus-US-Member-Segmentation-And-Retention-Analysis)

`Python` `Pandas` `Scikit-learn` `XGBoost` `Jupyter`

Conducted end-to-end churn analysis on 500,000 health insurance policyholder records in Python (Pandas, Scikit-learn, XGBoost), resolving 30+ data quality issues across enrollment, claims, and demographic fields before modeling. Applied RFM segmentation to identify high-value member clusters and ran 7 statistical hypothesis tests to validate key churn drivers; built an XGBoost classification model (AUC: 0.663) for churn prediction, a CLV regression model (R²: 0.729) for lifetime value estimation, and a 24-month Exponential Smoothing forecast to project membership trajectories. Delivered targeted retention recommendations for at-risk member segments, enabling health plan teams to prioritize intervention spend toward highest-CLV policyholders — where a 1% reduction in voluntary disenrollment can represent millions in preserved annual premium revenue.

---

#### 2. Academic Advising Assistant using RAG & LLM
[View Repository](https://github.com/angelintisha/Academic-Advising-Assistant-Using-Retrieval-Augmented-Generation)

`Python` `LangChain` `ChromaDB` `Ollama (llama3.2)` `Streamlit`

Built a Retrieval-Augmented Generation (RAG) chatbot in Python using LangChain for orchestration, ChromaDB as the vector store, and a locally hosted LLM (Ollama/llama3.2) for inference, ingesting 5 institutional document types (program handbooks, course catalogs, policies, FAQs, advising guides) into a semantic search pipeline and deploying the interface via Streamlit. The system achieved accurate, grounded responses across 7 distinct advising question categories by anchoring all outputs to retrieved source documents, eliminating hallucination. Demonstrates a production-ready RAG architecture directly applicable to high-stakes healthcare settings — clinical protocol Q&A, regulatory guidance retrieval, and patient-facing advisory systems — where LLM accuracy and full auditability are non-negotiable requirements.

---

#### 3. ClinTrialMatch — Clinical Trial Site Recommendation Engine
[View Repository](https://github.com/angelintisha/clintrialmatch) · [Live App](https://tishaangelin.shinyapps.io/clintrialmatch/)

`R` `Shiny` `shinyapps.io` `Content Filtering` `Similarity Scoring`

Built a web application in R/Shiny implementing a 5-step recommendation pipeline — content filtering by trial phase and therapeutic area, similarity scoring across 4 normalized site attributes (enrollment rate, screen failure rate, PI experience, infrastructure), dynamic urgency-based weighting, collaborative filtering proxy via region bonus, and composite ranking — applied against a database of 20 U.S. investigator sites. Deployed live on shinyapps.io with no API or login required. Phase III Oncology (West, Accelerated) surfaces Stanford and MD Anderson with 94–96/100 match scores; Phase I Cardiology (East, Standard) surfaces Penn Medicine and Johns Hopkins, confirming the engine differentiates meaningfully across inputs. Addresses a critical gap in the $50B+ clinical trial market where site selection is entirely manual — a leading cause of the 80% of trials that miss enrollment timelines, costing sponsors $600K–$8M per month of delay — replacing enterprise CTMS tools priced at $50K–$500K/year with a zero-cost, browser-accessible prototype.

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

### 🏥 Healthcare AI Strategy & Research

#### 6. Severity-Specific EMS Demand Forecasting — AI & BI Proposal
[View Repository](https://github.com/angelintisha/NYC-EMS-Severity-Demand-Forecasting) · [Read the Proposal (PDF)](https://github.com/angelintisha/NYC-EMS-Severity-Demand-Forecasting/blob/main/EMS_Demand_Forecasting_Proposal.pdf)

`Healthcare AI Strategy` `Time-Series Forecasting Design` `BI Dashboard Design` `NIST AI RMF` `NYC Open Data` `Implementation Planning`

Authored a proposal for an AI- and BI-enabled demand forecasting system for FDNY EMS that would convert Computer Aided Dispatch history into forecasts of incident counts by severity segment, dispatch area, and time window, addressing a rise in average response time to life-threatening emergencies from 9:34 to 11:21 between FY2021 and FY2025. The proposal specifies a four-layer architecture (data foundation, forecasting engine, BI delivery, decision layer) and a comparison of seasonal-naive baselines, statistical count models, and gradient-boosted trees under rolling-origin validation, with error reported per severity segment so that performance on common low-acuity calls cannot mask weak performance on rare Segment 1 emergencies (under 2% of incidents). It includes a conceptual dashboard mock-up, NIST AI RMF-aligned governance, an 18-month gated rollout with shadow mode and matched comparison areas, and five KPIs spanning forecast accuracy, adoption, response time, and borough equity. The system runs alongside the 911 dispatch path rather than inside it, leaving every operational decision with EMS personnel.

---

### 🗄️ Database & Data Engineering

#### 7. Travel Vaccination Advisory System
[View Repository](https://github.com/angelintisha/Travel-Vaccination-Advisory-System-DB)

`Oracle SQL` `Relational Database Design` `ERD Modeling` `BCNF Normalization`

Designed and implemented a fully normalized (BCNF) relational database for a Travel Vaccination Clinic in Oracle SQL, modeling 10 entities and 11 foreign key relationships spanning patient profiles, destination risk scores, vaccine schedules, treatment recommendations, and appointment records, with DDL/DML scripts and analytical SQL queries built to automate advisory report generation. The database handles the full advisory workflow — from patient intake to risk-stratified vaccine recommendation — with referential integrity enforced across all 11 FK relationships and patient-specific schedules returned in a single pass across joined tables. The system automates a manual, error-prone clinical advisory process and demonstrates relational database architecture directly applicable to EHR systems, clinical data repositories, and CDISC-compliant trial databases.

---

### 📈 Business Intelligence & Analytics

#### 8. Offshore Delivery Center Site Selection — Tableau Decision Dashboard
[View Repository](https://github.com/angelintisha/Offshore-Delivery-Center-Site-Selection-Tableau) · [Live Dashboard](https://public.tableau.com/views/CountryReadinessDashboardXYZOffshoreDeliveryCenter/ExecutiveDashboard)

`Tableau` `LOD Expressions` `Parameters` `K-Means Clustering` `Sensitivity Analysis` `OECD Going Digital`

Built a Tableau decision framework to shortlist countries for a hypothetical U.S. clinical data management company's first offshore delivery center, scoring 43 candidate countries on nine OECD Going Digital indicators organized into four strategic pillars (Talent, Trust & Data Security, Digital Infrastructure, Market Openness). Used level-of-detail expressions for pillar scores, parameter-driven weight sliders for sensitivity testing across four scenarios, k-means clustering to segment 31 fully scorable countries into three strategic profiles, and a two-tier screen that separates observed risk from missing data. Data validation was material to the outcome: deduplicating 42 double-classified records moved one country from sixth to fourth, and separating evidence gaps from risk cut flagged countries from 25 to 16. Cluster assignments were independently reproduced outside Tableau with identical results. The analysis recommended Finland, Sweden, and Ireland for due diligence (stable across weighting scenarios, no risk flags), and showed that most emerging markets, including India, Brazil, and Costa Rica, could not be ranked due to OECD coverage gaps rather than weak performance — a distinction that prevents a location decision from being made by default.

---

#### 9. Voltex Electronics — Sales Performance Analysis
[View Repository](https://github.com/angelintisha/Voltex-Electronics-Sales-Performance-Analysis) · [Live Dashboard](https://public.tableau.com/app/profile/angelin.tisha/viz/SalesPerformanceDashboardProduct/Dashboard1)

`Excel` `Tableau`

Cleaned and analyzed 108,127 global e-commerce orders for a multinational electronics retailer in Excel, resolving 15 data quality issues including duplicates, null values, and currency inconsistencies across regional datasets, before building an interactive Tableau dashboard with filters by region, product category, and time period to surface revenue trends and performance drivers. Analysis identified a COVID-driven 3x revenue spike peaking at $883K monthly and revealed that the top 3 products drove 85% of $24M in total revenue, alongside regional concentration and seasonal demand patterns across 4 years of order data. Findings directly support marketing spend reallocation toward top-performing SKUs and inventory planning ahead of demand peaks; the revenue concentration insight additionally flags supply chain risk and informs product diversification strategy.

---

#### 10. Weather & Sales Analysis + K-Nearest Neighbors
[View Repository](https://github.com/angelintisha/weather-sales-knn)

`Python` `NumPy` `Matplotlib` `KNN`

Analyzed a daily weather and sales dataset using NumPy Boolean array filtering to identify that high-sales days (sales > $500K) are warmer on average than all days in the dataset, visualized the three-variable relationship between temperature, precipitation, and sales using marker-differentiated scatter plots, and converted temperature readings from Fahrenheit to Celsius across the full array. Extended the analysis with a manual K-Nearest Neighbors implementation (no sklearn) to find the 5 most similar stocks to a query profile (4.5% growth, $4B market cap, 0.5 risk), applying min-max normalization across all features before computing Euclidean distances — demonstrating that feature scaling is essential for distance-based similarity methods.

---

#### 11. Bike Buyer Analysis
[View Repository](https://github.com/angelintisha/Bike-Buyer-Analysis)

`Excel` `Pivot Tables` `Interactive Dashboard`

Cleaned and analyzed 1,000 customer records across 13 demographic attributes (income, age, gender, commute distance, region, marital status, education, occupation, home ownership) in Excel, building an interactive dashboard with pivot tables, dynamic charts, and slicers for marital status, region, and education level to explore purchase behavior across customer segments. Analysis found that middle-aged customers (31–54) purchased bikes at the highest rate, that higher income correlated with purchase across both genders, and that customers with 0–1 mile commutes were most likely to purchase — indicating leisure-use rather than commute-driven demand. Findings provide a customer profile framework for targeted marketing, prioritizing mid-career, higher-income customers with short commutes for outreach and campaign spend.
