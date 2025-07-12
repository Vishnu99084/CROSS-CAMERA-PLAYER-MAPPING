# CROSS-CAMERA-PLAYER-MAPPING

Features Implemented
👤 Player Detection: Utilized the pretrained YOLOv8m model to detect players in both videos.
✂️ Image Cropping: Players detected in every 10th frame to improve runtime. Cropped and saved with frame and index information.
📊 Feature Extraction: Extracted HSV color histograms using OpenCV for each player image.
🔗 Cross-View Player Matching:
Cosine similarity computed between histograms.
Enforced no duplicate matches across views (one-to-one mapping).

🖼️ Visual Inspection:

Grid-based side-by-side match visualization using Matplotlib.
Matches saved in output/matched_pairs/ directory.

⏱️ Runtime Optimization:
Frame skipping and lightweight features used to balance accuracy and speed.

How to Run
Install dependencies:
pip install ultralytics opencv-python-headless matplotlib scikit-learn tqdm

Run the notebook:
Open LIAT_ASSIGNMENT.ipynb in Jupyter or Colab.
Make sure broadcast.mp4 and tacticam.mp4 are in the correct path (or update VIDEO_PATHS in the notebook).
