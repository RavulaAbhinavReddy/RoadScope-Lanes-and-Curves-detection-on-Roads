

# 🚗 RoadScope: Lanes and Curves Detection on Roads

A classical computer vision project for detecting **straight and curved road lanes** and predicting **turn directions**, inspired by **Lane Departure Warning Systems** used in self-driving cars.

---

## 📌 Features

- 🎯 Detects **solid and dashed lanes**
- 🌀 Detects **curved road lanes**
- 🧠 Predicts **left, right, or straight turns**
- 📐 Calculates **radius of curvature**
- 🖼️ Works with both **images and videos**
- 🚗 Designed for self-driving simulation and intelligent transport systems

---

## 🧠 Techniques Used

- 📏 **Homography & Perspective Warping**
- 📊 **Polynomial Curve Fitting**
- 📈 **Hough Line Transform**
- 🎯 **HSV Thresholding**
- 🧮 **Slope Analysis & Turn Prediction**

---

## 🧪 Pipeline

### 🔹 **Straight Lane Detection**

#### ✅ Solid Lane:
- ROI masking
- Hough Transform (tuned line length)
- Mean point and slope detection
- Single-line lane drawing

#### ✅ Dashed Lane:
- ROI masking
- Hough lines with slope-based filtering
- Mean point detection
- Dashed lane rendering

---

### 🔸 **Curved Lane Detection & Turn Prediction**

#### ⚪ White Lane:
- Bird’s-eye view (homography)
- Thresholding white pixels
- Coordinate extraction
- Curve fitting and plotting
- [Radius of Curvature](https://www.cuemath.com/radius-of-curvature-formula/) calculation

#### 🟡 Yellow Lane:
- HSV conversion and yellow masking
- Coordinate extraction and curve plotting
- Curvature calculation

#### 🔁 Turn Direction:
- ➕ Positive coefficient → **Right Turn**
- ➖ Negative coefficient → **Left Turn**
- 0 → **Straight Road**

---

## 🖥️ Demo Preview

![Curved Lane Detection Demo](https://github.com/abhijitmahalle/lane_detection/blob/master/gif/curved_lane_detection.gif)

---

## ⚙️ Requirements

- Python 3.x
- pip (Python package installer)

---

## 📦 Dependencies

pip install opencv-python numpy

🚀 How to Run
Clone the repository:

git clone https://github.com/RavulaAbhinavReddy/RoadScope-Lanes-and-Curves-detection-on-Roads.git
cd RoadScope-Lanes-and-Curves-detection-on-Roads
Install dependencies:

pip install -r requirements.txt

Run the scripts:

python straight_lane_detection.py
python curved_lane_detection.py

🗂️ Project Structure

RoadScope/
├── straight_lane_detection.py
├── curved_lane_detection.py
├── test_images/
├── test_videos/
├── requirements.txt
└── README.md
📈 Generalization Capability
✅ Straight Lane:
Works when:

One solid & one dashed line exist

Similar road shades and lighting

Similar field of view as original video

✅ Curved Lane:
Works when:

One white & one yellow lane exists

Lanes may be solid/dashed

Camera view is similar to source


👨‍💻 Author
Abhinav Reddy
📧 Email: abhinavreddy2307@gmail.com
🔗 GitHub: RavulaAbhinavReddy

