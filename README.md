# Smartan_Project
computer vision project  -- AI Pose Detection & Exercise Form Analysis

README.md (Final Professional Version)
# 🏋️ Smartan — AI Pose Detection & Exercise Form Analysis

Smartan is a computer vision–based fitness assistant that detects body posture using **MediaPipe Pose** and analyzes exercise movement using **OpenCV**.  
It extracts human body landmarks from uploaded workout videos and helps evaluate form quality for safer and more accurate exercise performance.

---


## 🔍 Problem Statement

In gyms and home workouts, incorrect body posture can lead to:
- Limited muscle activation
- Lack of progress
- Injuries

**Smartan automatically analyzes workout form** and provides digital feedback in a data-driven way.

---

## ✨ Key Features

| Feature | Status |
|--------|:-----:|
| Pose detection using MediaPipe | ✔️ |
| Skeleton overlay visualization | ✔️ |
| Extracting 33 landmarks per frame | ✔️ |
| Save pose data as CSV | ✔️ |
| Angle calculation of joints | In-Progress |
| Rep counting system | Planned |
| Real-time webcam support | Planned |

---

## 🧰 Technologies Used

| Category | Tools |
|---------|------|
| Programming | Python |
| ML/CV Framework | MediaPipe Pose |
| Video Processing | OpenCV |
| Visualization | Matplotlib |
| Environment | Jupyter / Google Colab |

---

## 📂 Repository Structure



Smartan/
│
├── data/
│ └── sample_video.mp4 # User exercise input (3–5 sec)
│
├── src/
│ ├── pose_detector.py # Detect & track pose landmarks
│ ├── visualization.py # Draw skeleton and export video
│ ├── data_export.py # Save keypoints as CSV
│ └── form_analysis.py # (Coming soon) angle & rep logic
│
├── notebooks/
│ └── Smartan_ExercisePose.ipynb # Main demo notebook
│
├── outputs/
│ ├── keypoints.csv # Stored landmark data
│ └── pose_processed.mp4 # Final skeleton-overlay video
│
├── requirements.txt # Dependencies
└── README.md # Project documentation


---

## 🧠 System Workflow

```mermaid
flowchart TD
A[Upload Exercise Video] --> B[MediaPipe Pose Detection]
B --> C[Extract 33 Landmarks (x,y)]
C --> D[Draw Skeleton on Video]
D --> E[Save Processed Video]
C --> F[Export Data to CSV]
F --> G[Form Quality Analysis]


📌 Code Explanation (Module-wise)
🔹 1️⃣ Pose Detection (pose_detector.py)

Loads MediaPipe Pose model (BlazePose)

Reads each frame via OpenCV

Detects body joints like:

nose, shoulders, elbows, wrists, hips, knees, ankles


Stores normalized coordinates (x, y)

🔹 2️⃣ Visualization (visualization.py)

Draws the human skeleton using:

Landmarks

Connectivity mapping from MediaPipe

Produces:
✔ Annotated video
✔ Landmark display frame-by-frame

🔹 3️⃣ Data Export (data_export.py)

Converts MediaPipe results → Pandas DataFrame

Columns stored like:

frame, landmark_0_x, landmark_0_y, ... landmark_32_y


Saves to outputs/keypoints.csv

🔹 4️⃣ Form Analysis (form_analysis.py)

📌 Coming in the next update
It will:

Calculate joint angles

Detect range of motion

Count exercise reps

Provide good/bad form feedback

▶️ Setup & Run Instructions
Install dependencies
pip install -r requirements.txt

Run the Notebook

Open:

notebooks/Smartan_ExercisePose.ipynb


Upload your workout video and Run All cells ✔️

📈 Output Examples
Type	Description
pose_processed.mp4	Detected skeleton overlay on your exercise
keypoints.csv	33 × 2 joint positions per frame
Angle plots (coming soon)	Motion analysis graph
🚀 Roadmap

 Real-time webcam live feedback

 Rep-Counter & Quality Score

 Full-stack dashboard (React + FastAPI)

 Voice assistant instructions

 Multiple exercise detection (Squat, Push-up, Curl etc.)

🤝 Contribution

Pull requests are welcome!
Fork → Improve → Submit PR

📜 License

MIT License © 2025 Adarsh Thakur

Made with ❤️ by Adarsh Thakur


---

### ✔️ Extra Files I can generate for you
| File | Purpose |
|------|---------|
| `requirements.txt` | Dependencies auto-install |
| `LICENSE` | MIT license |
| `.gitignore` | Clean repository |
| `src/*.py` | Split-code from notebook |
| Demo GIF thumbnail | Better repo branding |
| Shields.io badges | GitHub professional look |

---

### Before I push everything…
I just need two answers from you:

1️⃣ What repo name should I use?  
Examples:  
- `Smartan-Pose-Detection`
- `AI-Exercise-Form-Analyzer`
- `Smartan-Fitness-AI`

2️⃣ Should the repo be **Public** or **Private**?

Reply with your choice ⬇️  
and I’ll deliver the full structured repo with all files.
