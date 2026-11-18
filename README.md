# SMS Spam Filter (NLP)

Classifies SMS messages as **spam** or **ham** (not spam).

> 📚 **Course project:** completed while following the Udemy course *Python for Data Science and Machine Learning Bootcamp* (Pierian Data). The dataset and task come from the course.

## Approach
1. Explored message length per class (Seaborn, Matplotlib)
2. Text cleaning: removed punctuation and English stopwords (**NLTK**)
3. Bag-of-words features with **CountVectorizer**, weighted with **TF-IDF**
4. **Multinomial Naive Bayes** classifier, combined into a scikit-learn `Pipeline`

## Results (test set: 1,672 messages)

| Metric | Value |
|---|---|
| Accuracy | **0.96** |
| Macro F1 | 0.88 |
| Weighted F1 | 0.96 |

## Data
SMS Spam Collection dataset (tab-separated file `SMSSpamCollection`). It is **not included** in this repository. Place it at `smsspamcollection/SMSSpamCollection` before running the notebook.

## Tech
Python · pandas · NLTK · scikit-learn · Matplotlib · Seaborn · Jupyter

## Run it
```bash
git clone https://github.com/Aniket1103200/sms-filter-nlp.git
cd sms-filter-nlp
pip install -r requirements.txt
python -m nltk.downloader stopwords
jupyter notebook sms_spam_filter.ipynb
```
