# VisionGuard: AI-Based Diabetic Retinopathy Detection

A web application that classifies the severity of diabetic retinopathy from retinal fundus images using a deep learning model, served through a Flask REST API.

> **Disclaimer:** This project is for educational and research purposes only. It is not a medical device and must not be used for clinical diagnosis.

## Table of Contents

- [Description](#description)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Model Details](#model-details)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Usage](#usage)
- [Screenshots](#screenshots)
- [Contributors](#contributors)

---

## Description

VisionGuard predicts the **severity stage of diabetic retinopathy** from an uploaded retinal image. The model classifies each image into one of five stages:

| Class | Stage |
|-------|-------|
| 0 | No Diabetic Retinopathy |
| 1 | Mild |
| 2 | Moderate |
| 3 | Severe |
| 4 | Proliferative |

The Flask backend handles image preprocessing and model inference, and the web interface lets users upload an image and view the predicted stage.

---

## Results

<!-- FILL IN with your real numbers from training/validation. Delete any line you do not have. -->

| Metric | Value |
|--------|-------|
| Training accuracy | 94% |
| Validation accuracy | 92% |

---

## Technologies Used

**Model and data**

- [FILL IN: TensorFlow/Keras or PyTorch, whichever you used]
- EfficientNet-B0 (transfer learning)
- NumPy, Pandas, Scikit-learn
- OpenCV / PIL for image preprocessing (keep only what you used)

**Backend**

- Python, Flask (REST API for preprocessing and inference)

**Frontend**

- HTML, CSS, JavaScript (image upload and API calls)

---

## Dataset

The model was trained on the [APTOS 2019 Blindness Detection dataset](https://www.kaggle.com/c/aptos2019-blindness-detection), which contains retinal fundus images labelled into 5 severity classes.

---

## Model Details

- **Architecture:** EfficientNet-B0 (pretrained on ImageNet, fine-tuned on APTOS 2019)
- **Framework:** [FILL IN]
- **Input:** Retinal fundus images resized to [FILL IN, e.g. 224x224] with [FILL IN: your preprocessing steps]
- **Output:** Classification into 5 severity stages (0 to 4)
- **Training setup:** [FILL IN: epochs, batch size, optimizer, any augmentation]

---

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/ggauthamm/VisionGuard.git
   cd VisionGuard
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Make sure the trained model file is inside the `model/` folder.

---

## Project Structure

```
VisionGuard/
├── static/               # CSS, JavaScript, and images
├── templates/            # HTML files
├── model/                # Trained model file
├── screenshots/          # Screenshots used in this README
├── app.py                # Flask application
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
```

---

## How to Run

1. Start the Flask server:

   ```bash
   python app.py
   ```

2. Open your browser and go to `http://127.0.0.1:5000/`.

3. Upload a retinal image to get a prediction.

---

## Usage

1. **Open the web interface** on your local server.
2. **Upload an image** using the upload button.
3. **View the prediction.** The app displays the predicted stage of diabetic retinopathy.

---

## Screenshots

**Home page**

![Home page](screenshots/home.png)

**Website**

![Website](screenshots/webpage.png)

**Image upload**

![Upload section](screenshots/diagnosis-section.png)

**Prediction output**

![Prediction output](screenshots/results.png)

---

## Contributors

- [Bharath C](https://github.com/BharathC050903)
- [Gautham Krishnan](https://github.com/ggauthamm)
