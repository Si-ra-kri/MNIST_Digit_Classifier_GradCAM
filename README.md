# 🚀 PyTorch MNIST Digit Classifier with Grad-CAM

This project is a Convolutional Neural Network (CNN) built in PyTorch that classifies handwritten digits (0-9). It is trained on the 60,000-image MNIST dataset and achieves high accuracy.

The key feature is the inclusion of **Grad-CAM** (Gradient-weighted Class Activation Mapping), which generates a visual heatmap to explain *why* the model made its decision. The model also provides a **confidence percentage** for each prediction.

## ✨ Features

* **High-Accuracy Model:** The CNN is trained for 10 epochs to achieve >98% accuracy on the test set.
* **Explainable AI (XAI):** Uses Grad-CAM to create a heatmap, highlighting the pixels the model "looked at" to make its prediction.
* **Confidence Score:** Outputs the prediction's confidence as a percentage.
* **Robust Prediction:** Includes a pre-processing pipeline in `Cell 6` to clean, center, and format user-uploaded images for the model.

## 📸 Demo

![Demo Image](images/demo.png)

Here is the model correctly identifying a user-uploaded image of the digit "2" with 100% confidence. The Grad-CAM heatmap clearly shows the model focused on the correct strokes of the digit.



## 🛠️ Technologies Used

* PyTorch
* OpenCV (cv2)
* Pillow (PIL)
* Matplotlib
* Google Colab (or Jupyter Notebook)

---

## ⚡ How to Use (Prediction)

This is the fast-track guide to make predictions using the included pre-trained model.

**Required Files:**
* `MNIST_Digit_Classifier.ipynb` (This notebook)
* `my_mnist_model.pth` (The pre-trained model file)

**Steps:**

1.  **Open the Notebook:** Open the `.ipynb` file in Google Colab or Jupyter.
2.  **Upload the Model:**
    * In Colab, click the **folder icon** (📁) on the left.
    * Click the **"Upload" icon** and select your `my_mnist_model.pth` file.
3.  **Run Setup Cells:** Run the following cells in order:
    * **`Cell 1: Setup & Imports`**
    * **`Cell 2: Load Data`** (This defines the `transform_test` needed for prediction)
    * **`Cell 3: Model & Helper Functions`** (This defines the `SmallCNN` class)
4.  **SKIP Cell 4:** You can **skip `Cell 4: Run Training`** entirely.
5.  **Load Your Model:** Run **`Cell 5: Load Model & Grad-CAM Setup`**. This will load your uploaded `.pth` file.
6.  **Predict!** Run **`Cell 6: Predict on Your Own Image`** and upload a picture of a digit.

---

## 🧠 (Optional) Train the Model From Scratch

If you don't have the `.pth` file or want to train the model yourself, just run all cells in order.

1.  Run **`Cell 1: Setup & Imports`**
2.  Run **`Cell 2: Load Data`**
3.  Run **`Cell 3: Model & Helper Functions`**
4.  Run **`Cell 4: Run Training`**
    * This will train the model for 10 epochs (about 2-3 minutes) and save the new `my_mnist_model.pth` file.
5.  Run **`Cell 5: Load Model & Grad-CAM Setup`**
6.  Run **`Cell 6: Predict on Your Own Image`**
