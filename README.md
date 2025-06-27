# Smart-Sorting-Transfer-Learning-for-Identifying-Rotten-Fruits-and-Vegetables
Smart Sorting is an innovative project focused on enhancing the precision and efficiency of detecting rotten fruits and vegetables using cutting-edge transfer learning techniques. By leveraging pre-trained deep learning models and adapting them to specific datasets of fruits and vegetables.



---

## 🚀 Features

- 🔍 Detects rotten or fresh status from uploaded fruit/vegetable images
- 🧠 Uses Transfer Learning (VGG16) for high-accuracy classification
- 🌐 Flask-based web application with user-friendly interface
- 📸 Upload images and get instant predictions with confidence scores
- 💡 Tips page with food storage advice
- 📬 About Us & Contact form
- 🔐 Sign-in interface (basic)

---

## 📂 Project Structure

here is the drive link for dataset and other files: https://drive.google.com/drive/folders/1LWbySgVZaeVTV-6f_R3gfQqGkXKoHDu2?usp=sharing
SmartSorting/
├── app.py
├── trainmodel.py
├── model/
│   └── healthy_vs_rotten.h5
├── fruit_dataset/
├── static/
│   └── uploads/
├── templates/
│   ├── home.html
│   ├── predict.html
│   ├── tips.html
│   ├── about.html
│   └── signin.html
├── requirements.txt
└── README.md


🧠 Model Details
Architecture: VGG16 (pre-trained on ImageNet)

Layers Added: Flatten → Dropout → Dense (Softmax)

Classes: Apple, Banana, Carrot, Orange, Potato (Fresh & Rotten)

Training done using trainmodel.py

 Install Dependencies
Create a virtual environment (recommended):
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate



Then install:
pip install -r requirements.txt



 Run the App:
 Make sure the model/healthy_vs_rotten.h5 exists. Then:  python app.py

Visit http://127.0.0.1:5000 in your browser.



📸 How Prediction Works
User uploads an image via web interface

Image is resized to 150x150, normalized

Model predicts class and confidence score

Output is shown with label and image preview



💬 Future Enhancements
Real-time camera input (for conveyor belts or smart fridges)

Deploy as mobile or IoT edge device with TensorFlow Lite

Add Google Sign-In or Firebase for advanced authentication



🧪 Dataset

- Directory structure based on **class folders** (e.g., `Banana__Healthy`, `Potato__Rotten`)
- Contains **labeled images** of 5 fruits/vegetables in both healthy and rotten conditions
- Used **ImageDataGenerator** for rescaling, rotation, shear, and flip augmentations



🧭 Project Stages

| Stage                      | Description |
|-----------------------     |-------------|
| **1. Problem Definition** | Food waste due to manual errors in sorting fruits/vegetables |
| **2. Data Collection**    | Gathered and labeled image data |
| **3. Model Training**     | Transfer learning with VGG16 and model tuning |
| **4. Web Development**    | Built multi-page Flask app with prediction UI |
| **5. Deployment**         | Integrated trained model with front-end for real-time predictions |
| **6. Evaluation**         | Measured accuracy and confidence of predictions |
| **7. Enhancement**        | Added food tips, sign-in page, and contact form |


🧭 Contexts & Use Cases
📦 Scenario 1: Food Processing Industry
Automated sorting on conveyor belts using cameras and this AI model.

🛒 Scenario 2: Supermarket Receiving
Detect rotten items during inventory check at receiving docks.

🏠 Scenario 3: Smart Refrigerators
Camera-equipped fridges notify users of rotting produce.



📊 Example Prediction Output
Input: Uploaded image of a carrot

Output: Carrot__Rotten

Confidence: 94.78%

Display: Prediction + uploaded image on the webpage


Requirements:
Flask==2.3.2
numpy==1.24.3
tensorflow==2.12.0
keras==2.12.0



📬 Contact & Contribution
Pull requests and feedback are welcome!
Open issues for bugs or suggestions.










