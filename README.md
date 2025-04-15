## 📌 Project Title
**Object Action Detection Using Deep Learning (Home Surveillance)**
## 🧠 Abstract

Object Action Detection is an intelligent **video surveillance system** developed to strengthen **home security** by detecting **abnormal human activities** from **recorded video footage**. The system uses deep learning (Spatial Autoencoder) to analyze actions and identify suspicious behavior in indoor settings.

Instead of real-time surveillance, the system works with **pre-recorded videos**. It processes the video to detect abnormal actions (like theft or violence) and captures **key frames** where suspicious activity occurs.

When abnormal activity is detected, the system:
- Sends a **mail alert** to the homeowner.
- **Attaches the suspicious frame** as an image.
- Stores the images for future references.

---

## 💻 Technologies Used

### 🔹 Frontend:
- HTML
- CSS
- JavaScript

### 🔹 Backend:
- Python
- Django Framework

### 🔹 Database:
- MySQL

### 🔹 IDE:
- Sublime Text

---

## 🔍 Features

- Detects **abnormal actions** from recorded videos.
- Captures and **saves keyframes**.
- Sends **alert emails** to the user with frame image.
- Optional **real-time detection** using device camera.
- Maintains a **clean and accessible web interface**.
- Built with **Waterfall Software Model**.
- Implements **Spatial Autoencoder** for action recognition.
- Uses datasets:
  - **Avenue Dataset**
  - **UCSD Anomaly Detection Dataset**

---

## 🛠️ Project Structure

Here’s an overview of the folder structure:

ViolenceDetectionProject/
│
├── db.sqlite3                            # Django default database
├── labels.npy                            # Encoded labels for classification
├── manage.py                             # Django project manager
├── my_model.h5                           # Trained ML model (version 1)
├── my_model_2.h5                         # Trained ML model (version 2)
├── requirement.txt                       # Python dependencies
├── video_files_paths.npy                 # List of video file paths
├── webcam_frame.txt                      # Temp storage for webcam frame
│
├── *.ipynb                               # Jupyter notebooks for model training/testing
│   ├── video-violence-guard-transfer-learning.ipynb
│   ├── video_testing.ipynb
│   └── violence-detection-mobilenet-model.ipynb
│
├── violence_detection/                   # App-level assets
│   └── static/
│       └── images/
│           └── surveillance_image.png
│
├── venv/                                 # Python virtual environment
│   ├── Lib/
│   ├── Scripts/
│   ├── share/
│   └── pyvenv.cfg
│
├── ViolenceDetection/                    # Django project root
│   ├── home/                             # Core Django app
│   │   ├── __pycache__/
│   │   ├── migrations/
│   │   │   └── 0001_initial.py
│   │   ├── __init__.py
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── config.json                   # Configs for detection
│   │   ├── email_alert.py                # Alert logic via email
│   │   ├── send_alert_email.py
│   │   ├── models.py
│   │   ├── views.py                      # Real-time logic and views
│   │   ├── urls.py
│   │   ├── tests.py
│   │   ├── surveillance_image.png
│   │   ├── suspicious_image.jpg
│   │   └── suspicious_frame.jpg
│   │
│   ├── media/                            # Uploaded or generated media files
│   │
│   └── templates/                        # HTML templates for frontend
│       ├── base.html
│       ├── bgimage.jpg
│       ├── index.html
│       ├── navbar.html
│       ├── realtime.html                # 🔴 Real-time Monitoring Interface
│       ├── result.html
│       ├── surveillance.png
│       └── upload.html
 

## 🔧 Installation Instructions

```bash
# Clone the repository
git clone https://github.com/yourusername/ObjectActionDetection.git
cd ObjectActionDetection

# Create virtual environment and activate
python -m venv venv
venv\Scripts\activate  # On Windows

# Install dependencies
pip install -r requirement.txt

# Run migrations (if using SQLite or connect MySQL accordingly)
python manage.py makemigrations
python manage.py migrate

# Run the server
python manage.py runserver
```

👉 Then visit: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🧪 Testing

- **Unit Testing**: Tests each Django view and video-processing function.
- **Integration Testing**: Ensures video upload + frame capture + email flow works.
- **System Testing**: Validates all modules together.
- **Validation & Output Testing**: Confirm required outputs are accurate.
- **User Acceptance Testing**: Gathered through direct feedback.

---

## 📋 Test Cases

| Test Case | Description |
|-----------|-------------|
| Registration | User can't leave any field blank, validated IDs |
| Login | Requires valid credentials |
| Upload Video | File format & abnormal frame detection tested |
| Frame Alert | Frame saved, email triggered |
| Real-Time Button | Device camera works and captures frames |

---

## ⚙️ System Requirements

### Hardware:
- Windows 7 or higher
- Intel i3 processor or higher
- 4 GB RAM minimum
- 100 GB disk

### Software:
- Python
- Sublime Text or any IDE
- XAMPP Server
- MySQL

---

## ✅ Advantages

- Detects abnormal behavior from **recorded or real-time** videos.
- Captures **key frames**, not entire footage.
- Lightweight, **no background running** needed.
- **Email alerts** for prompt action.

---

## ⚠️ Limitations

- Only works if video file is uploaded.
- No background surveillance—**must be user-initiated**.
