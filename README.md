# Real-Time Emotion Analysis System

This project implements a real-time emotion analysis system using a React frontend and a Flask backend. The application captures images from a webcam at regular intervals, sends them to the Flask backend for processing, and performs emotion analysis on the captured images. The results of the analysis can be used for user behavior tracking, mental health studies, or enhancing user experience in interactive systems.

## Objectives

### Frontend (React):
- Request webcam access and capture images at user-defined intervals.
- Display the captured images in real-time.
- Send the captured images to the backend for emotion analysis.
- Provide start and stop functionality for image capturing.

### Backend (Flask):
- Process the images received from the frontend.
- Perform emotion analysis on the images using machine learning or deep learning models.
- Send the analysis results back to the frontend.

## Technologies Used

### Frontend:
- **React**: For building an interactive user interface.
- **react-webcam**: To integrate webcam functionality.
- **axios**: To handle HTTP requests for data transfer.
- **canvas**: For rendering captured images.

### Backend:
- **Flask**: For building RESTful API endpoints.
- **flask-cors**: To enable cross-origin resource sharing.
- **OpenCV**: For image preprocessing.
- **DeepFace**: For loading pre-trained emotion analysis models.
- **Pillow**: For image manipulation and conversion.

## Features Implemented

### Frontend:
- **Webcam Integration**: Requests user permission to access the webcam.
- **Image Capture**: Captures images at regular intervals using the react-webcam library.
- **Image Display**: Displays the captured image on a canvas in real-time.
- **Data Transfer**: Sends captured images in Base64 format to the Flask backend via POST requests.
- **User Controls**: Includes buttons to start and stop image capturing, displaying the current state of the webcam.

### Backend:
- **Image Handling**: Decodes and processes the received Base64 image data.
- **Emotion Analysis**: Uses a pre-trained emotion recognition model to classify the emotions in the image (e.g., happy, sad, angry, surprised).
- **Response Management**: Sends the emotion analysis results (e.g., detected emotion and confidence level) back to the React frontend.

## Implementation Details

### Frontend Workflow:
1. **Request Webcam Access**: The application uses the react-webcam library to access the webcam.
2. **Capture and Render Images**: Images are captured at specified intervals and displayed on an HTML canvas.
3. **Send Images to Backend**: Captured images are encoded in Base64 format and sent to the Flask backend using axios.
4. **Display Results**: Receives emotion analysis results from the backend and displays them in the interface.

### Backend Workflow:
1. **Receive Image Data**: The Flask API accepts POST requests containing image data in Base64 format.
2. **Image Preprocessing**: Converts the Base64 string to an image file using libraries like Pillow.
3. **Emotion Analysis**: Uses a pre-trained deep learning model to predict emotions.
4. **Return Results**: Sends the detected emotion and its confidence level back to the frontend in JSON format.

## Key Challenges

- **Model Integration**: Selecting a suitable pre-trained model for emotion analysis and optimizing it for real-time performance.
- **Image Processing**: Ensuring image preprocessing (e.g., resizing, normalization) is consistent with the model's requirements.
- **CORS Issues**: Handling cross-origin requests between React and Flask, resolved using the flask-cors library.

## Results

- **Emotion Analysis**: The system successfully classifies emotions like happiness, sadness, anger, and surprise from the captured images.
- **Real-Time Functionality**: Captures and processes images seamlessly in real-time with minimal latency.
- **User Feedback**: Displays the analyzed emotions in the frontend for user interaction.

## Future Enhancements

- **Advanced Emotion Recognition**: Use more robust models to detect subtle emotions and expressions.
- **Data Visualization**: Add graphs and analytics to visualize the user's emotional trends over time.
- **Performance Optimization**: Optimize data transfer and processing to handle high frame rates efficiently.
- **Extended Features**: Include video-based emotion analysis by capturing multiple frames and aggregating results.
- **Emotion-Aware Systems**: Integrate the system with other applications to create emotion-aware features (e.g., personalized recommendations, alerts).

## Conclusion

This project successfully implements a real-time emotion analysis system using a React frontend and a Flask backend. By capturing and analyzing webcam images, it demonstrates the potential for interactive applications in mental health, user experience design, and real-time feedback systems. The system's modular design allows for easy enhancements, making it a versatile framework for emotion-based interactive applications.

# Interactive Parent-Child Activity Planner

## Overview

The Interactive Parent-Child Activity Planner is a web-based application that recommends activities for parents and children to enjoy together. By analyzing shared hobbies and interests, the platform provides tailored suggestions to enhance family bonding and create memorable experiences.

## Aim

The key objectives of this project are as follows:

- **User Input Collection:** Gather details about the child’s interests, age, and preferences.
- **ML Model Integration:** Utilize a trained machine learning model to predict suitable hobbies.
- **Activity Retrieval from Database:** Fetch activities from MongoDB based on predicted hobby and age group.
- **Personalized Recommendations:** Generate customized activity suggestions.
- **Interactive UI:** Provide an intuitive and user-friendly interface for parents.

## Demo

Experience the live application: [Interactive Parent-Child Activity Planner](https://interactive-parent-child-activity-planner.onrender.com/)

## Dataset Description

The dataset used for training the model contains various child interests, age groups, and activity preferences. The structured data allows the model to identify patterns and suggest the most relevant activities.

- **Dataset Source:** [Hobby Prediction Dataset](https://www.kaggle.com/datasets/abtabm/hobby-prediction-basic/data)
- **Features:**
  - Child’s age (categorized into **4-5** and **6-8** years)
  - Interests (Arts, Sports, Academics)
  - Preferred activity type (indoor, outdoor)
  - Time availability
  - Parental participation level

## How It Works

1. **User Input Handling:** Collects child-related details through a form.
2. **ML Model Prediction:** The trained model predicts the child's hobby (Arts, Sports, or Academics).
3. **Fetching Data from MongoDB:** Based on the predicted hobby and age group, the system retrieves activity recommendations from the MongoDB database.
4. **Recommendation Display:** Presents the personalized recommendations (videos, descriptions, required materials) on the web interface.

## MongoDB Database Structure

The database stores activities under three categories: **Arts, Sports, and Academics**, further classified into two age groups (**4-5** and **6-8**). Each activity entry includes:

- **URL**: A link to an instructional video.
- **Title**: Activity name.
- **Description**: Brief details about the activity.
- **Image**: Stored as a Base64 binary.
- **Materials**: List of required materials.
- **Duration**: Estimated time to complete the activity.
- **Age Group**: Either **4-5** or **6-8**.

## Model Training and Evaluation

The machine learning models used in this project were trained using a dataset from Kaggle.

- Dataset: Hobby Prediction Dataset
- Libraries Used: pandas, numpy, matplotlib, seaborn, sklearn

## Models Implemented:

1. RandomForestClassifier (Primary Model)
2. Logistic Regression

## Model Evaluation:

- Metrics Used:

  - Accuracy Score
  - Classification Report
  - Confusion Matrix

- Performance on Test Data:
  - Achieved 91% accuracy

## Hyperparameter Tuning:

- Used GridSearchCV to optimize the model parameters.
- Improved model performance by tuning hyperparameters for better accuracy.

# Child Safety Object Detection

## Overview

This project uses **Flask** to implement a real-time object detection system fo>

## Technologies Used

- **Flask**: Web framework to serve the application.
- **HTML-CSS-JS**: Serves UI and Frontend


## Manual Deployment

```bash
cd folder  # The folder you want to clone project into
```

```bash
git clone https://github.com/CBcodes03/combined.git .
```

```bash
pip install -r requirements.txt
```

```bash
gunicorn -w 4 -b 0.0.0.0:8000 app:app
```
