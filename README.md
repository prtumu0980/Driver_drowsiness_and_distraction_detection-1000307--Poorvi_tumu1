The following project is based on driver drowsiness detection using Convolutional Neural Networks. It can automatically detect the presence of drowsiness depending on the driver's eyes and mouth conditions: whether open, closed, yawning, or not yawning. The main objective is to reduce road accidents due to fatigue by providing an automated real-time alert system.

Data Preparation

The dataset used for this project consists of driver facial images that were categorized into the following four classes: Open Eyes

Closed Eyes

Yawning

No Yawn

Data Organization

dataset/

│

├── train/

│ ├── Open/

│ ├── Closed/

│ ├── Yawn/

│ └── No_Yawn/

│

└── test/

├── Open/

├── Closed/

├── Yawn/

└── No_Yawn/

Preprocessing Steps

Resized all images to 224×224 pixels.

Normalized pixel values to range [0, 1].

Data augmentation-rotation, zoom, flipping-was used to improve generalization.

Divide the data into 80% training and 20% testing.

Evaluation Metrics and Results

Metric/Result

Training Accuracy 64%

Validation Accuracy 63.27%

Loss consistently decreased after each epoch

These results show that a CNN can classify the states of eyes and mouths efficiently, but with more data and fine-tuning, accuracy can be enhanced.

Demonstration of the Project

Testing was made easy and interactive via a Streamlit web application.

Features • Upload an Image or Webcam Input • Predicts whether the driver is Alert, Yawning, or Drowsy. • Confidence percentage for each prediction is displayed. • Real-time webcam testing using pyngrok tunneling.

How to Run

Install dependencies:

pip install tensorflow keras streamlit pyngrok opencv-python

Run the web application:

Streamlit run app.py

Open the ngrok link in your browser and start testing, using either your webcam or sample images. Conclusion: The Driver Drowsiness Detection system is only one such example of deep learning put to use for road safety. This translates to an accuracy of 63.27%, which is a good starting point for real-world drowsiness monitoring systems. Future Improvements Real-time detection by tracking facial landmarks. Larger, more diverse datasets. Integration with vehicle systems for alert sound notifications.

<img width="362" height="622" alt="Screenshot 2025-10-31 204905" src="https://github.com/user-attachments/assets/982cbf6d-ccd0-4bad-8391-1873618eadf3" />

