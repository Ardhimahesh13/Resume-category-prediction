# Resume-category-prediction
This NLP-powered app automates the first step of recruitment by classifying resumes into 25 job categories.
It uses a Scikit-learn model deployed in an interactive Streamlit web application, demonstrating an end-to-end text classification workflow.

# 📄 NLP-Powered Resume Category Predictor

An intelligent web application that uses Natural Language Processing (NLP) and Machine Learning to automatically classify resumes into one of 25 predefined job categories
. This project automates the initial, time-consuming step of resume screening, enabling recruiters to efficiently sort candidates.
<img width="973" height="707" alt="image" src="https://github.com/user-attachments/assets/3cf48f42-dcf3-4240-971f-50eda0585efe" />
## ✨ Key Features

-   **Multi-Class Text Classification:** The core model accurately distinguishes between 25 different job roles (e.g., Data Science, Java Developer, HR).
-   **Interactive Web Interface:** A user-friendly UI built with Streamlit allows for easy interaction by simply pasting resume text.
-   **End-to-End NLP Pipeline:** Demonstrates a complete and practical data science workflow, from raw text cleaning to model deployment.
-   **High Performance:** The trained model achieves **98% accuracy** on the test dataset, ensuring reliable predictions.

---

## 🛠️ Tech Stack & Libraries

This project leverages a modern stack for data science and web deployment:

-   **Language:** `Python`
-   **Machine Learning:** `Scikit-learn` (for modeling and vectorization)
-   **NLP:** `NLTK` (for text preprocessing)
-   **Web Framework:** `Streamlit` (for building the interactive UI)
-   **Data Manipulation:** `Pandas`, `NumPy`
-   **Model Persistence:** `Pickle` (for saving the trained model)

---

## 📈 The Data Science Workflow

The project follows a structured approach to solving the problem:

1.  **Data Loading & Cleaning:** The process began with a dataset of resumes and their corresponding job categories. A custom text cleaning function using regular expressions (`regex`) was developed to preprocess the raw text by removing URLs, mentions, hashtags, punctuation, and other non-essential characters.

2.  **Feature Engineering (Vectorization):** The cleaned resume text was transformed into a numerical format suitable for machine learning. This was achieved using `TfidfVectorizer`, which creates a matrix of TF-IDF features that represent the importance of each word in the context of all resumes.

3.  **Model Training & Evaluation:** A `KNeighborsClassifier` was selected as the classification algorithm. To handle the multi-class nature of the problem (25 categories), it was wrapped in a `OneVsRestClassifier`. The model was trained on 80% of the data and evaluated on the remaining 20%, achieving an impressive **98.45% accuracy**.

4.  **Deployment:** The trained TF-IDF vectorizer (`tfidf.pkl`) and the classifier (`clf.pkl`) were saved using Pickle. A Streamlit script (`app.py`) was created to load these models and serve a web-based interface for real-time predictions.

---## 🚀 How to Run This Project Locally

To set up and run this application on your local machine, follow these steps:

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/Ardhimahesh13/resume-category-prediction.git](https://github.com/Ardhimahesh13/resume-category-prediction.git)
    cd resume-category-prediction
    ```

2.  **Create a Virtual Environment (Recommended)**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the Required Libraries**
    Make sure you have a `requirements.txt` file with all the necessary libraries. Then run:
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Streamlit App**
    ```bash
    streamlit run app.py
    ```
    The application will open in a new tab in your web browser!
