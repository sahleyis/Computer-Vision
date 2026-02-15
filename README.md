VisionNexus: Integrated CV & Biometric AccessVisionNexus is a multi-modal Computer Vision application that utilizes OpenCV and MediaPipe to perform real-time object detection and physiological tracking. This project is designed to evolve from a tracking suite into a secure Face Verification gateway for application access.🚀 FeaturesColor Detection: Real-time masking and identification of specific HSV color ranges.Hand Tracking: High-fidelity 21-point landmark detection for gesture control.Pose Estimation: Full-body skeletal tracking to differentiate between body parts.Integrated ML Pipeline: Scalable architecture to transition from detection to classification.Future Scope: Face Verification module using FaceNet or DeepFace for app security.🛠️ Tech StackLanguage: PythonCore Library: OpenCV (cv2)ML Framework: MediaPipe (for landmarks) & Scikit-learn (for initial classification)Hardware: Standard RGB Webcam📂 Project StructurePlaintext├── data/               # Training images for Face Verification
├── models/             # Saved .h5 or .pkl models
├── src/
│   ├── color_det.py    # Color masking logic
│   ├── tracking.py     # Hand and Pose estimation
│   └── auth.py         # Face verification logic (In Development)
└── main.py             # Main execution script
⚙️ Installation & SetupClone the repository:Bashgit clone https://github.com/your-username/VisionNexus.git
cd VisionNexus
Install dependencies:Bashpip install opencv-python mediapipe numpy scikit-learn
Run the tracker:Bashpython main.py
🧠 Machine Learning IntegrationTo differentiate between objects and parts, we use a Random Forest Classifier trained on coordinate data extracted from MediaPipe.How it works:Data Collection: Capture $(x, y, z)$ coordinates of landmarks.Training: The model learns the spatial relationship between "Hand" vs "Shoulder."Inference: Real-time classification based on the live webcam feed.$$P(class | landmarks) = \frac{P(landmarks | class) P(class)}{P(landmarks)}$$🔒 Roadmap: Face VerificationThe next phase involves training a Siamese Network or using a pre-trained FaceNet model to compare live webcam frames against a "Golden Image" (your face).[ ] Stabilize Hand/Body differentiation.[ ] Implement 128-d face embeddings.[ ] Create a Python decorator to "Lock" other apps until verification is successful.
