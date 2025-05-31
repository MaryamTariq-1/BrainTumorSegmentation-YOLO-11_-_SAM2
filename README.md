# BrainTumorSegmentation-YOLO-11_-_SAM2


This project applies Meta AI's Segment Anything Model (SAM) to segment brain tumors from MRI scans. It involves evaluating the SAM-generated masks against ground truth tumor masks and filtering them to isolate tumor regions for potential downstream tasks like classification or medical analysis.

## 📁 Dataset

- **Source**: [Kaggle Brain Tumor Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
- **Classes**:
  - Glioma
  - Meningioma
  - Pituitary
  - No tumor

Each image corresponds to one of these classes and is stored in subdirectories.

## 🧠 Objective

- Run SAM (Segment Anything Model) on all brain MRI images.
- Generate segmentation masks.
- Evaluate against ground truth masks using metrics like **IoU**.
- Filter out the most relevant tumor region.
- Visualize and optionally export the results.

## 🛠️ Tech Stack

- Python
- OpenCV
- NumPy
- PyTorch
- Matplotlib
- SAM (Meta AI)
- Kaggle GPU Kernel / local CUDA-enabled machine

## 🚀 Setup Instructions

1. Clone this repository:

```bash
git clone https://github.com/your-username/brain-tumor-sam.git
cd brain-tumor-sam
````

2. Install dependencies:

```bash
pip install torch torchvision opencv-python matplotlib
pip install git+https://github.com/facebookresearch/segment-anything.git
```

3. Download the SAM model weights:

```bash
wget -O sam_vit_b.pth https://dl.fbaipublicfiles.com/segment_anything/sam_vit_b_01ec64.pth
```

4. Organize dataset:

```
/brain-tumor-dataset/
    /Testing/
        /glioma/
        /meningioma/
        /notumor/
        /pituitary/
    /masks/   # Ground truth binary masks
```

5. Run the notebook or script:

```bash
jupyter notebook brain-tumor.ipynb
```

---

## 📊 Evaluation

* Intersection over Union (IoU) is computed per image.
* Optional Dice Score metric is available.
* All results can be exported as CSV or visualized.

## ✅ Features

* Apply SAM segmentation to medical imaging.
* Filter for largest relevant mask (tumor localization).
* Compare SAM output with actual ground truth.
* Export filtered masks for further use (e.g., training).

## 📂 Output

* Visual plots of MRI with SAM-segmented tumor contours.

## 🧪 Sample Result

![Sample Output](https://www.linkedin.com/posts/maryamtariq1_ai-machinelearning-deeplearning-activity-7334593735139201024-tJP0?utm_source=share&utm_medium=member_desktop&rcm=ACoAAE2xIwEBmV84gJqMIgDISLclQGhDfHs3OAs)

---

## 📌 Future Work

* Fine-tune SAM for medical imaging domain.
* Use filtered masks to train a classification model.
* Explore other segmentation models for comparison.

## 🙋‍♀️ Author

**Maryam Tariq**
Machine Learning & Data Analyst Intern
[LinkedIn](https://www.linkedin.com/in/maryamtariq1/)



```
