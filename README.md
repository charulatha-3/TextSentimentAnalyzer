# 🧠 Text Sentiment Analyzer

A simple and interactive **Text Sentiment Analysis** web application that analyzes user-provided text and classifies it as **Positive, Negative, or Neutral**.

The application is developed using **HTML, CSS, and JavaScript** and runs directly in a web browser without requiring a backend server.

---

## 📌 Project Overview

The **Text Sentiment Analyzer** is a Natural Language Processing (NLP)-based application that identifies the emotional polarity of a given text.

The application examines words in the input text, compares them with predefined positive and negative sentiment dictionaries, and calculates a sentiment score.

### Possible Results

* 😊 **Positive**
* 😐 **Neutral**
* 😞 **Negative**

---

## 🎯 Objectives

* Analyze the sentiment of user-provided text.
* Identify positive and negative words.
* Classify text into positive, negative, or neutral categories.
* Display a sentiment score.
* Show positive, negative, and neutral word percentages.
* Maintain a history of recent analyses.
* Provide a simple and user-friendly interface.

---

## ✨ Features

### 📝 Text Input

Users can enter or paste text into the analysis box.

### 🔍 Sentiment Analysis

The application analyzes the input and determines whether the sentiment is:

```text
😊 Positive
😐 Neutral
😞 Negative
```

### 📊 Sentiment Score

A numerical score is generated based on the positive and negative words detected in the text.

### 📈 Sentiment Breakdown

The application displays:

* Positive percentage
* Neutral percentage
* Negative percentage

### 🕘 Recent Analysis

The application stores the latest five analyses in the browser.

### 💾 Local Storage

Recent analysis history is stored using browser `localStorage`.

### 🧹 Clear Option

Users can clear the current text and reset the result.

### 📱 Responsive Design

The interface works on:

* Desktop
* Laptop
* Tablet
* Mobile

---

## 🛠️ Technologies Used

### Frontend

* HTML5
* CSS3
* JavaScript

### Concepts

* Natural Language Processing basics
* Sentiment Analysis
* String Processing
* Word Matching
* Score Calculation
* Local Storage
* DOM Manipulation

---

## 🧠 How Sentiment Analysis Works

The application uses a **rule-based sentiment analysis approach**.

### Step 1 — User Input

The user enters a sentence or paragraph.

Example:

```text
I really love this product. It is amazing and useful.
```

### Step 2 — Text Processing

The application:

* Converts text to lowercase.
* Removes unnecessary punctuation.
* Splits the text into individual words.

Example:

```text
I really love this product
```

becomes:

```text
i
really
love
this
product
```

### Step 3 — Word Matching

Words are compared with predefined sentiment dictionaries.

Example:

```text
love      → +3
amazing   → +3
useful    → +2
```

### Step 4 — Score Calculation

The individual word scores are added together.

```text
+3 +3 +2 = +8
```

A positive score indicates positive sentiment.

### Step 5 — Classification

The final score is classified as:

```text
Score > 1    → Positive

Score < -1   → Negative

Otherwise    → Neutral
```

---

## 🔄 Processing Flow

```text
        User enters text
                ↓
        Convert to lowercase
                ↓
        Remove punctuation
                ↓
          Split into words
                ↓
       Compare with dictionary
                ↓
        Calculate word scores
                ↓
       Check for negation
                ↓
        Calculate final score
                ↓
     ┌──────────┼──────────┐
     ↓          ↓          ↓
  Positive    Neutral    Negative
     ↓          ↓          ↓
        Display Analysis
```

---

## 📂 Project Structure

```text
TextSentimentAnalyzer/
│
├── index.html
│
└── README.md
```

The project is intentionally designed as a single-page application, so all HTML, CSS, and JavaScript are contained inside `index.html`.

---

## 🚀 How to Run

### Step 1

Create a folder:

```text
TextSentimentAnalyzer
```

### Step 2

Open the folder in **Visual Studio Code**.

### Step 3

Create:

```text
index.html
```

### Step 4

Paste the project code into `index.html`.

### Step 5

Save the file.

### Step 6

Run the application using **Live Server**.

In VS Code:

```text
Right Click index.html
        ↓
Open with Live Server
```

The application will open in your default browser.

---

## 🧪 Test Examples

### Positive Example

```text
I absolutely love this product. It is amazing and beautiful!
```

Expected result:

```text
😊 Positive
```

---

### Negative Example

```text
This product is terrible and disappointing. I hate the poor quality.
```

Expected result:

```text
😞 Negative
```

---

### Neutral Example

```text
The meeting is scheduled for tomorrow at 10 AM.
```

Expected result:

```text
😐 Neutral
```

---

### Negation Example

```text
I do not like this product.
```

The application includes a basic **negation check** to handle words such as:

```text
not
never
no
don't
didn't
isn't
can't
won't
```

---

## 📊 Example Output

```text
┌────────────────────────────────────┐
│       ANALYSIS RESULT              │
│                                    │
│              😊                    │
│           Positive                 │
│                                    │
│       Sentiment Score: +8          │
│                                    │
│ Positive      43%                  │
│ Neutral       43%                  │
│ Negative      14%                  │
└────────────────────────────────────┘
```

---

## 💾 Local Storage

Recent analysis results are stored using:

```javascript
localStorage
```

The storage key used by the application is:

```text
sentimentHistory
```

The application stores up to **five recent analyses**.

---

## 🔐 Privacy

This application performs the analysis directly in the browser.

No text is sent to an external server or API by this implementation.

---

## ⚠️ Limitations

This project uses a **basic rule-based approach**, so it is not equivalent to advanced machine-learning or large-language-model sentiment analysis.

It may have difficulty understanding:

* Sarcasm
* Slang
* Complex sentences
* Context-dependent meanings
* Multiple emotions
* Ambiguous words
* Long-form language patterns

For example:

```text
"Oh great, my phone crashed again."
```

A human may understand the sarcasm, while a simple word-based system may classify it incorrectly.

---

## 🔮 Future Enhancements

The project can be upgraded with:

* 🤖 Machine Learning-based sentiment classification
* 🧠 NLP libraries
* 📊 Advanced sentiment charts
* 🎯 Confidence score
* 🌍 Multi-language sentiment analysis
* 😊 Emotion detection
* ☁️ Cloud-based analysis
* 🎙️ Speech-to-text input
* 🔊 Speech sentiment analysis
* 📱 Progressive Web App
* 📈 Sentiment history dashboard

---

## 🎙️ Connection to Speech Analysis

This project can later be extended to accept voice input.

The future flow can be:

```text
User speaks
    ↓
Speech Recognition
    ↓
Speech → Text
    ↓
Text Sentiment Analyzer
    ↓
Positive / Neutral / Negative
```

This makes the project a foundation for the later **Speech Analysis applications** in the Text and Speech Analysis project series.

---

## 🎓 Academic Applications

This project can be used as:

* NLP Mini Project
* Text Analysis Application
* Web Technology Project
* Artificial Intelligence Prototype
* Text and Speech Analysis Application
* CSE Laboratory Project
* College Mini Project

---

## 📚 Concepts Demonstrated

```text
HTML
 ↓
User Interface

CSS
 ↓
Responsive Design

JavaScript
 ↓
Text Processing
 ↓
Word Matching
 ↓
Sentiment Scoring
 ↓
Classification
 ↓
Result Visualization
 ↓
Local Storage
```

---

## 👩‍💻 Author

**Charulatha S**

B.E. Computer Science Engineering
Prathyusha Engineering College

---

## ⭐ Project Summary

**Text Sentiment Analyzer** demonstrates how basic Natural Language Processing techniques can be used to determine the emotional polarity of text.

It provides a simple foundation for developing more advanced **Text and Speech Analysis applications** using machine learning, NLP, and speech recognition technologies.

---

### 📌 Application 1 of 10

**Text & Speech Analysis Application Series**

```text
✅ Application 1 — Text Sentiment Analyzer
⬜ Application 2 — Text Emotion Detector
⬜ Application 3 — Text Statistics Analyzer
⬜ Application 4 — Keyword & Topic Extractor
⬜ Application 5 — Text Summarizer
⬜ Application 6 — Speech-to-Text Analyzer
⬜ Application 7 — Speech Emotion Analyzer
⬜ Application 8 — Voice Command Application
⬜ Application 9 — Speech Characteristics Analyzer
⬜ Application 10 — Text & Speech Chat Assistant
```
