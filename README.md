# Security Awareness Training Analysis

This project uses **Natural Language Processing (NLP)** to analyze feedback from security awareness training programs. The goal is to identify areas where participants have misunderstandings or gaps in knowledge, helping improve training effectiveness by addressing common misconceptions.

### Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Dataset](#dataset)
- [Model Development](#model-development)
- [Deployment](#deployment)
- [Usage](#usage)
- [Results](#results)
- [Future Work](#future-work)

---

### Project Overview

Security awareness training programs are essential for building a strong security culture in organizations. However, participants often face misunderstandings or lack clarity in key areas. This project aims to:
- Identify common topics (like phishing or password management) where misunderstandings are frequent.
- Analyze the sentiment of feedback to gauge participant engagement and comprehension.

---

### Features

1. **Sentiment Analysis**: Detects the sentiment (positive, neutral, negative) of feedback.
2. **Topic Modeling**: Identifies key topics within participant reviews, such as "Phishing Awareness" or "Two-Factor Authentication."
3. **Misunderstanding Detection**: Flags comments that suggest confusion, helping trainers refine course materials.

---

### Dataset

For the project, we analyzed feedback from security awareness training programs. If you'd like to use a similar dataset, you can:
- Collect security training reviews from platforms like Udemy, Coursera, or internal training feedback forms.
- [Placeholder for dataset source if available]

### Model Development

This model was developed using:
- **LDA (Latent Dirichlet Allocation)** for topic modeling
- **Sentiment Analysis** with TextBlob or similar libraries
- **Python Libraries**: Gensim, NLTK, Pandas, Matplotlib, etc.

The model was trained and fine-tuned to extract relevant insights from the feedback data.

---

### Deployment

The project is deployed on **Hugging Face** to make it accessible and interactive. Users can input feedback directly through the interface and receive analyzed results instantly.

#### Deployment Steps

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/username/security-awareness-training-analysis.git
    cd security-awareness-training-analysis
    ```

2. **Run Locally** (Optional):
   To test the model locally, set up a virtual environment and install the required packages.
    ```bash
    pip install -r requirements.txt
    ```

3. **Hugging Face Deployment**:
   The model is deployed on Hugging Face for easy access. Log in to Hugging Face and push the model:
    ```python
    !huggingface-cli login
    lda_model.push_to_hub("your-username/security-awareness-training-analysis")
    ```

4. **Interactive Gradio Interface**:
   The Hugging Face interface integrates with Gradio to allow users to input new feedback and view insights in real-time.

---

### Usage

Once deployed, users can interact with the model through a web-based UI. Here’s how to use it:

1. **Single Review Analysis**:
   - Type or paste a review into the text box (e.g., "I didn’t fully understand why two-factor authentication is necessary").
   - The model will output the identified **topic** (e.g., "Authentication Security") and **sentiment** (e.g., "Neutral").
   - Misunderstanding indicators will highlight areas where additional training may be beneficial.

2. **Batch Analysis** (Optional):
   - Upload a `.csv` file with multiple reviews for batch processing.
   - The model will analyze each entry and provide a summary of topics, sentiment, and flagged misunderstandings.

---

### Results

The model provides valuable insights such as:
- **Topic Distribution**: A breakdown of topics with the highest frequency of misunderstandings.
- **Sentiment Overview**: Overall sentiment, helping trainers understand participants' engagement levels.
- **Misunderstanding Indicators**: Highlights areas needing improvement, based on recurring feedback issues.

---

### Future Work

Potential enhancements:
- **Expand the Dataset**: Add feedback from various industries and demographics.
- **Fine-Tune NLP Models**: Improve the model by integrating advanced NLP techniques, like transformer models for better accuracy.
- **Customizable Analysis**: Allow users to select specific topics or aspects for a more focused analysis.

---

### Contributing

If you’re interested in contributing, feel free to create pull requests or open issues to suggest improvements.

### License

This project is licensed under the MIT License.

---
