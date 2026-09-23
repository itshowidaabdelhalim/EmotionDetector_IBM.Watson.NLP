# Emotion Detector

## Repository for Final Project

The **Emotion Detector** is a web application built with **Python and Flask** that analyzes text and identifies five different emotions:

* Joy
* Sadness
* Anger
* Disgust
* Fear

The application uses the **IBM Watson Natural Language Processing Emotion service** to analyze the input text, return emotion scores, and determine the dominant emotion.

---

## Project Overview

The application allows users to enter a sentence or text through a web interface. The text is sent to the emotion detection function, which communicates with the IBM Watson NLP service.

The workflow is:

```text
User Input → Flask Web Application → Emotion Detection Function
                     ↓
         IBM Watson NLP Emotion Service
                     ↓
               Emotion Scores
                     ↓
          Dominant Emotion → Results
```

---

## Features

* Web-based Emotion Detector interface
* Text input from the user
* IBM Watson NLP emotion analysis
* Detection of five emotions:

  * Joy
  * Sadness
  * Anger
  * Disgust
  * Fear
* Emotion scores for each emotion
* Automatic identification of the dominant emotion
* Flask backend
* HTML, CSS, and JavaScript frontend
* JSON-based API communication

---

## Technologies Used

* Python
* Flask
* Requests
* IBM Watson NLP
* HTML
* CSS
* JavaScript
* JSON

---

## Testing

The application was tested using different text inputs to verify that it correctly:

* Accepts user input.
* Sends the text for emotion analysis.
* Extracts the five required emotion scores.
* Identifies the dominant emotion.
* Displays the results through the web interface.

---

## Test Results

The following screenshots show the results of testing the Emotion Detector with different input statements.

### Test Case 1

![Emotion Detection Test 1](screenshots/Screenshot5.png)

### Test Case 2

![Emotion Detection Test 2](screenshots/Screenshot6.png)

### Test Case 3

![Emotion Detection Test 3](screenshots/Screenshot4.png)

### Test Case 4

![Emotion Detection Test 4](screenshots/Screenshot1.png)

### Test Case 5

![Emotion Detection Test 5](screenshots/Screenshot3.png)

### Test Case 6

![Emotion Detection Test 6](screenshots/Screenshot2.png)

---

## API Processing

The emotion detection module communicates with the IBM Watson NLP service using an HTTP request.

The application:

1. Sends the input text to the NLP service.
2. Receives the JSON response.
3. Converts the response into a Python dictionary.
4. Extracts the emotion scores.
5. Compares the scores.
6. Determines the dominant emotion.
7. Returns the results to the Flask application.

---

## Application Architecture

### Frontend

The frontend provides the interface where users enter text and view the emotion analysis results.

It uses:

* HTML
* CSS
* JavaScript

### Backend

The Flask backend handles requests from the frontend and connects the web application to the emotion detection module.

Main file:

```text
server.py
```

### Emotion Detection

The emotion detection module communicates with the IBM Watson NLP service and processes the returned emotion scores.

Main file:

```text
emotion_detection.py
```

---

## Conclusion

The Emotion Detector project demonstrates how a Flask web application can use an NLP service to analyze text and identify emotions.

The system analyzes **anger, disgust, fear, joy, and sadness**, provides a score for each emotion, and determines the **dominant emotion** based on the highest score.

For the test case **"I am glad this happened"**, the system identified **joy** as the dominant emotion.
