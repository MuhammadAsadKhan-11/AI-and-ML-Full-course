# 🤖 AI & ML Full Course — 30-Day Revision Series

A structured, day-by-day revision of core Artificial Intelligence and Machine Learning concepts — implemented hands-on through real datasets and mini-projects, from fundamentals to advanced techniques.

This repository documents my daily progress as I rebuild my ML foundations from scratch: one topic, one notebook, one commit at a time.

---

## 🎯 About This Repository

Instead of just re-reading theory, this series focuses on **implementing every concept in code** — data analysis, preprocessing, statistics, machine learning algorithms, model evaluation, and eventually deep learning and MLOps.

Each day lives in its own folder containing:
- A Jupyter notebook with fully worked code
- The dataset used (where applicable)
- A dedicated `README.md` explaining that day's concepts in detail

---

## 🗂️ Repository Structure

```
AI-and-ML-Full-course/
│
├── Day 1 EDA/
│   ├── EDA.ipynb
│   ├── insurance.csv
│   └── readme.md
│
├── Day 2 .../               (upcoming)
├── Day 3 .../               (upcoming)
└── ...
```

Each `Day N` folder is self-contained — its own README explains the concepts, tools, and reasoning behind that day's work.

---

## 📚 Topics Covered So Far

### ✅ Day 1 — Exploratory Data Analysis (EDA) & Feature Engineering
Dataset: Medical Insurance Charges

- Data inspection: `.shape`, `.info()`, `.describe()`, missing value checks
- Univariate visualization: histograms with KDE, count plots, box plots
- Correlation analysis using heatmaps
- Data cleaning: handling duplicates
- Categorical encoding: manual label mapping & one-hot encoding (`pd.get_dummies`) with dummy variable trap avoidance
- Feature engineering: binning continuous variables (`pd.cut`) into meaningful categories
- Feature scaling: standardization with `StandardScaler`
- Statistical feature selection:
  - Pearson correlation test (numeric features vs. target, with p-values)
  - Chi-square test of independence (categorical features vs. binned target)
- Final, statistically justified feature set for modeling

📎 [Read Day 1 details →](./Day%201%20EDA/readme.md)

---

## 🛣️ Roadmap — What This Course Will Cover

This repository is structured as a progressive roadmap — starting from data fundamentals and ending at agentic, LLM-powered systems. Every stage builds on the one before it.

### 1️⃣ Data Fundamentals & Statistics
- Exploratory Data Analysis (EDA) — univariate, bivariate, multivariate analysis
- Data cleaning: missing values, duplicates, outlier treatment
- Feature engineering & feature scaling (Standardization, Normalization)
- Encoding techniques: Label Encoding, One-Hot Encoding
- Statistical hypothesis testing: T-test, Chi-square, ANOVA, Pearson/Spearman correlation
- Probability distributions & the Central Limit Theorem

### 2️⃣ Machine Learning (ML)
**Basic**
- Linear Regression, Logistic Regression
- KNN, Naive Bayes, Decision Trees
- Bias-variance tradeoff, overfitting/underfitting, regularization (L1/L2)
- Train-test split, cross-validation, evaluation metrics (accuracy, precision, recall, F1, ROC-AUC, RMSE, R²)

**Advanced**
- Support Vector Machines (SVM)
- Ensemble learning: Bagging, Random Forest, Boosting (AdaBoost, Gradient Boosting, XGBoost, LightGBM, CatBoost)
- Unsupervised learning: K-Means, Hierarchical Clustering, DBSCAN
- Dimensionality reduction: PCA, t-SNE
- Hyperparameter tuning: GridSearchCV, RandomizedSearchCV, Optuna
- Handling imbalanced data: SMOTE, class weighting

### 3️⃣ MLOps
- Experiment tracking & versioning (MLflow, DVC)
- Model packaging & serialization (Pickle, Joblib, ONNX)
- Building ML APIs (Flask, FastAPI)
- Containerization & deployment (Docker, cloud deployment basics)
- CI/CD pipelines for ML projects
- Model monitoring, drift detection & retraining pipelines

### 4️⃣ Deep Learning (DL)
**Basic**
- Perceptron, Artificial Neural Networks (ANN)
- Forward & backward propagation, gradient descent
- Activation functions (ReLU, Sigmoid, Tanh, Softmax)
- Loss functions & optimizers (SGD, Adam, RMSprop)
- Regularization: Dropout, Batch Normalization, Early Stopping

**Advanced**
- Convolutional Neural Networks (CNNs) — image classification, object detection basics
- Recurrent Neural Networks (RNNs), LSTM, GRU — sequence modeling
- Autoencoders & GANs (generative fundamentals)
- Transfer learning & fine-tuning pretrained models
- TensorFlow/Keras & PyTorch implementations

### 5️⃣ Natural Language Processing (NLP)
**Basic**
- Text preprocessing: tokenization, stemming, lemmatization, stopword removal
- Bag of Words, TF-IDF
- Word embeddings: Word2Vec, GloVe

**Advanced**
- Sequence models for text (RNN/LSTM for NLP)
- Attention mechanism
- Transformer architecture (encoder-decoder, self-attention, positional encoding)
- Pretrained language models: BERT, GPT family — architecture & use cases
- Named Entity Recognition (NER), sentiment analysis, text classification pipelines

### 6️⃣ Generative AI & Large Language Models (LLMs)
- LLM fundamentals: tokenization, context window, temperature, top-k/top-p sampling
- Prompt engineering: zero-shot, few-shot, chain-of-thought prompting
- Fine-tuning vs. prompting vs. RAG — when to use which
- Parameter-efficient fine-tuning: LoRA, QLoRA
- Working with LLM APIs (OpenAI, Gemini, Claude/Anthropic API)
- Embeddings & vector representations of text

### 7️⃣ Retrieval-Augmented Generation (RAG)
- Vector databases (FAISS, ChromaDB, Pinecone)
- Embedding generation & semantic search
- Chunking strategies & retrieval pipelines
- Building RAG pipelines with LangChain / LlamaIndex
- Hybrid search (keyword + semantic), re-ranking
- Evaluating RAG systems (faithfulness, relevance, groundedness)

### 8️⃣ Agentic AI
- Agent fundamentals: reasoning, planning, and tool use (ReAct framework)
- Function calling / tool calling with LLMs
- Multi-step task decomposition & memory (short-term vs. long-term)
- Multi-agent systems & orchestration
- Frameworks: LangChain Agents, LangGraph, CrewAI, AutoGen
- Building real-world agentic workflows (email assistants, report generation agents, RAG-powered chatbots)

*(Roadmap will be updated as the series progresses — not all topics are guaranteed to be covered in exactly 30 days, but each day builds directly on the last, following this exact progression: Data → ML → MLOps → DL → NLP → GenAI/LLM → RAG → Agentic AI.)*

---

## 🛠️ Tech Stack

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Scikit-learn` `SciPy` `TensorFlow / Keras` `Jupyter Notebook`

---

## ⚙️ How to Use This Repository

```bash
# Clone the repository
git clone https://github.com/MuhammadAsadKhan-11/AI-and-ML-Full-course.git
cd AI-and-ML-Full-course

# Navigate into any day's folder
cd "Day 1 EDA"

# Install common dependencies
pip install pandas numpy seaborn matplotlib scikit-learn scipy jupyter

# Launch the notebook
jupyter notebook
```

---

## 🙋‍♂️ About Me

**Muhammad Asad Khan**
Final Year BSSE Student, NUML Islamabad
AI/ML enthusiast | Building DigiServe — an AI-focused digital software house

🔗 [GitHub](https://github.com/MuhammadAsadKhan-11)

Following along daily on LinkedIn as part of this 30-day AI/ML revision challenge — feel free to connect and follow the journey.

---



---

⭐ If you find this useful for your own ML revision, consider starring the repo!
