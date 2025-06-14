# Fruit Image Classifier

![image](https://github.com/user-attachments/assets/7bd70fa0-786d-47eb-901e-9eb2a5dd2b5c)


A web application that uses deep learning to classify images of fruits with 98% accuracy. Built with Flask, TensorFlow, and Bootstrap.

## Features

- Upload fruit images for classification (JPG, JPEG, PNG formats)
- Sample images for quick testing
- MobileNetV2 deep learning model for accurate predictions
- Beautiful, responsive UI with gradient designs
- Displays prediction results with nutritional information
- Sample image demonstration functionality


### Upload Interface

![image](https://github.com/user-attachments/assets/97a1ffff-796f-4220-85fd-dfc11589524b)

The main interface where users can upload their fruit images or select from sample fruits.

### Classification Result

![image](https://github.com/user-attachments/assets/7ed6e509-53af-4d78-8c17-ec80a551f617)

The result page showing the predicted fruit along with health information about the fruit.

## Technologies Used

- **Backend**: Python, Flask
- **Frontend**: HTML5, CSS3, Bootstrap 5
- **Deep Learning**: TensorFlow, Keras, MobileNetV2
- **Image Processing**: PIL, OpenCV (indirectly through Keras)
- **Deployment**: Ready for deployment on any WSGI server

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/fruit-classifier.git
   cd fruit-classifier
   ```

2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

3. Download the pre-trained model and class labels:
   - Place `fruit_classifier_mobilenetv2.h5` in the root directory
   - Place `class_labels.json` in the root directory

4. Run the application:
   ```bash
   python app.py
   ```

5. Open your browser and navigate to `http://localhost:8080`

## Project Structure

```
fruit-classifier/
├── app.py                # Main Flask application
├── static/               # Static files
│   └── uploads/          # Uploaded images storage
├── templates/
│   ├── index.html        # Main upload interface
│   └── result.html       # Results display page
├── fruit_classifier_mobilenetv2.h5  # Pretrained model
└── class_labels.json     # Class labels for predictions
```

## How It Works

1. The user uploads an image of a fruit through the web interface
2. The Flask backend receives the image and preprocesses it for the MobileNetV2 model
3. The model makes a prediction about which fruit is in the image
4. The result is displayed to the user along with nutritional information
5. The image is converted to base64 for display without needing file storage

## Customization

To customize this project:

1. **Model**: Replace `fruit_classifier_mobilenetv2.h5` with your own trained model
2. **Classes**: Update `class_labels.json` with your own class labels
3. **Styling**: Modify the CSS in the HTML files or add a separate stylesheet
4. **Features**: Extend the Flask application with additional routes and functionality

## Future Enhancements

- [ ] Add user authentication
- [ ] Implement a history of previous classifications
- [ ] Add more detailed nutritional information for each fruit
- [ ] Include confidence scores in the results
- [ ] Deploy as a Docker container
