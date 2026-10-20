
<h1 align="center">📝 SmartGrade OMR</h1>

<h3 align="center">A simple OMR grading project built with Python and OpenCV</h3>

<p align="center">
  Automating the basic process of checking multiple-choice answer sheets using computer vision.
</p>

---

## 👨‍💻 About the Project

SmartGrade OMR is a mini project I built to explore how computer vision can help with the evaluation of multiple-choice answer sheets.

The idea is simple: upload an image of an OMR sheet, detect the marked bubbles, compare the answers with an answer key, and calculate the score.

I used Python, OpenCV, and Flask to build a basic web application for this. It is still a prototype, and I have tested it with a limited sample sheet, so there is more work to do before it can handle different OMR formats reliably.

## ✨ What It Can Do

- 📷 Upload an image of an OMR answer sheet.
- 🔍 Detect marked bubbles using OpenCV.
- ✅ Compare the detected answers with an answer key.
- 📊 Calculate the number of correct answers and the percentage score.
- 🖼️ View an annotated image with detected answers highlighted in green or red.
- 🌐 Use a simple web interface to submit a sheet and view the results.

## 🛠️ Built With

- **Python** — Main programming language.
- **OpenCV** — Image processing and bubble detection.
- **NumPy** — Image data and numerical operations.
- **Flask** — Backend and web application.
- **HTML, CSS & JavaScript** — Frontend interface.

## ⚙️ How It Works

1. **Upload an image** — Submit an OMR answer sheet through the web interface.
2. **Process the image** — OpenCV analyses the image and identifies potential answer bubbles.
3. **Detect the answers** — The program uses dark pixel counts in the detected regions to estimate the selected options.
4. **Check the answers** — The detected responses are compared against the provided answer key.
5. **Calculate the score** — The application determines the number of correct answers and the percentage.
6. **View the result** — The score and an annotated image are returned.

## 🚀 Getting Started

Want to try it on your own system? Here is how to run it locally.

### Prerequisites

- Python 3.9 or later
- pip

### 1. Clone the repository

```bash
git clone https://github.com/albinvsoju/Smart-Grade-OMR.git
cd Smart-Grade-OMR
```

### 2. Install the dependencies

```bash
python -m pip install Flask flask-cors opencv-python numpy
```

### 3. Check the HTML filename

The Flask application currently looks for `smartgrade.html`, while the HTML file in the repository is named `SmartGrade OMR.html`.

Rename the file to `smartgrade.html`, or update the filename referenced in `app.py` to match the existing file.

### 4. Run the application

```bash
python app.py
```

### 5. Open it in your browser

Visit:

```text
http://127.0.0.1:5000
```

Upload a sample OMR image and provide its corresponding answer key through the interface.

## 📁 Project Structure

```text
Smart-Grade-OMR/
├── app.py              # Flask application
├── omr.py              # OMR processing and grading logic
├── SmartGrade OMR.html # Web interface
├── test.py             # OpenCV test script
├── test img.jpg        # Sample OMR image
└── static/             # Generated result images
```

**Note:** The HTML filename must match the one configured in `app.py`.

## ⚠️ Current Limitations

This project is still a work in progress. Here are a few things to keep in mind:

- It has been tested with a limited sample OMR sheet.
- The detection logic depends on the layout and spacing of the sheet.
- Different layouts, poor lighting, rotation, and camera angles may affect the results.
- Detection and grading results should be checked manually.
- It has not been validated for large-scale or production use.

## 🔮 What's Next?

There are a few things I'd like to improve as I continue working on this project:

- Support different OMR sheet layouts.
- Make bubble detection more reliable under different image conditions.
- Handle unanswered questions and multiple marked options.
- Add batch processing for multiple answer sheets.
- Improve error handling and grading accuracy.
- Generate downloadable result reports.

## 🎯 What I Learned

This project gave me a chance to work with Python, OpenCV, and Flask in a practical application. It also helped me explore how image processing can be used to solve repetitive tasks, along with the challenges involved in detecting marks accurately from real-world images.

## 👨‍💻 About Me

**Albin V Soju**  
Computer Science and Engineering Student

[GitHub Profile](https://github.com/albinvsoju)

---

<p align="center">
  Built as a learning project to explore computer vision and web-based automation.
</p>
