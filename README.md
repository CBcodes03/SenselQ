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
