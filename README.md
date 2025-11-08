# Deep-Learning-Based-Image-Segmentation-with-FCN-8-Architecture

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)](https://www.tensorflow.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Google%20Colab%20%7C%20Jupyter-lightgrey.svg)](#)

---

### 🎯 Pixel-Level Classification and Segmentation using TensorFlow

This project implements a **Fully Convolutional Network (FCN-8)** for **pixel-level image segmentation** on the **Multi-MNIST dataset**, where overlapping handwritten digits are separated into distinct segmented regions.  
The model achieves a **mean Intersection over Union (IoU) of 0.6497** — equivalent to a **grade of 64.97**, showing strong generalization across all ten classes.

> ⚙️ This project was developed as part of the **DeepLearning.AI “Advanced Computer Vision with TensorFlow”** course on Udemy.  
> While certain code templates and guidelines were provided as part of the assignment, the **core implementation, analysis, model design, and documentation** were independently written by the author.  
> No proprietary course materials or instructor code are redistributed here; this repository serves solely for **learning, research, and portfolio** purposes.

---

## 🧩 Project Overview

- Designed and trained an **FCN-8 architecture** for semantic segmentation.  
- Performed **pixel-wise classification** on complex overlapping digit images.  
- Evaluated model accuracy with **class-wise IoU** and **Dice Scores**.  
- Related results to **mechanical engineering use cases**, including:
  - **Defect detection** and **surface damage identification** in manufacturing.  
  - **Robotic vision** for component inspection and quality assurance.  
  - **Autonomous fault detection** in mechanical systems.  

---

## 📊 Model Results

| Digit | IoU | Dice Score |
|:------:|:----------------:|:----------------:|
| 0 | 0.707 | 0.829 |
| 1 | 0.708 | 0.829 |
| 2 | 0.595 | 0.746 |
| 3 | 0.606 | 0.755 |
| 4 | 0.629 | 0.773 |
| 5 | 0.560 | 0.718 |
| 6 | 0.712 | 0.832 |
| 7 | 0.665 | 0.799 |
| 8 | 0.677 | 0.807 |
| 9 | 0.637 | 0.778 |

**Average IoU:** 0.649  
**Overall Grade:** 64.97  
✅ **Result:** Passed  

---

## 🧠 Key Insights

- The network outputs **class probability maps** for each pixel.  
- Example pixel predictions:
  ```python
  print(results[0,0,0,0])  # 0.043152
  print(results[0,0,0,10]) # 0.9756403
````

→ The pixel is **97.56% confident** it belongs to class 10.

* Final segmentation map shape:

  ```python
  (192, 64, 84)
  ```

* Visualizing results:

  ```python
  plt.imshow(results[0])
  plt.title("Predicted Segmentation Map")
  plt.axis("off")
  plt.show()
  ```

---

## ⚙️ Technologies Used

| Category        | Tools                           |
| :-------------- | :------------------------------ |
| **Language**    | Python 3.10+                    |
| **Frameworks**  | TensorFlow, Keras               |
| **Libraries**   | NumPy, Matplotlib               |
| **Environment** | Jupyter Notebook / Google Colab |

---

## 🔗 Mechanical Engineering Relevance

Although this work was inspired by a computer vision course, it has **direct mechanical engineering applications**:

* **Defect detection:** Automate inspection of cracks, corrosion, or deformation on components.
* **Material analysis:** Segment and classify surface textures or composite layers.
* **Robotic inspection:** Enable real-time vision for automated maintenance systems.
* **Smart manufacturing:** Integrate segmentation into quality control pipelines.

By adapting FCN-based models, engineers can enhance **autonomous systems** for inspection, predictive maintenance, and adaptive control in modern mechanical systems.

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/fcn8-image-segmentation.git
cd fcn8-image-segmentation
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Open the Notebook

Run locally:

```bash
jupyter notebook FCN8_Segmentation.ipynb
```

Or open directly in [Google Colab](https://colab.research.google.com) and upload the notebook file.

---

## 📸 Example Output

*(Add a segmentation result image here)*

```python
plt.imshow(results[0])
plt.title("Predicted Segmentation Map")
plt.axis("off")
plt.show()
```

---

## 🧾 License

This project is released under the [MIT License](LICENSE).
All original educational content belongs to **DeepLearning.AI** and the **Advanced Computer Vision with TensorFlow** course on Udemy.

---

## 🙌 Acknowledgements

* **DeepLearning.AI** – for their excellent “Advanced Computer Vision with TensorFlow” course.
* TensorFlow documentation and Keras community for open-source tools.
* Multi-MNIST dataset for research and experimentation.

---

### 👨‍🔬 Author

**Richard Olamide Olanite**
Mechanical & Machine Learning Engineer
📧 **Email:** (richardolanite@gmail.com)  
🔗 **LinkedIn:** (https://linkedin.com/in/richardolanite)  
💻 **GitHub:** (https://github.com/thatboypage)
