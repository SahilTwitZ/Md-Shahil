
# StyleFinder: Fashion Recommender System

**StyleFinder** is an intelligent fashion recommendation system that suggests visually similar clothing items based on an uploaded image. It leverages deep learning for visual feature extraction and a k-Nearest Neighbors (k-NN) model for similarity matching. The system is built with an intuitive UI using Streamlit.

---

## 🔍 Features

- **Image-Based Search**: Upload an image of a clothing item to receive similar recommendations.
- **Deep Feature Extraction**: Utilizes a pre-trained ResNet50 model to capture high-level visual features.
- **Fast Recommendations**: Uses k-NN to identify the most visually similar clothing items.
- **Interactive Web Interface**: Developed with Streamlit for a smooth and interactive user experience.

---

## ⚙️ How It Works

1. **Dataset Preprocessing**
   - Clothing images from the dataset are processed using ResNet50 (without the top layer).
   - Extracted features are saved in `embeddings.pkl` for efficient lookup.
   - Associated filenames are saved in `filenames.pkl`.

2. **User Upload**
   - The user uploads a clothing image via the UI.
   - The system extracts features from the uploaded image using the same model.

3. **Similarity Search**
   - The extracted feature vector is compared to the dataset using k-NN.
   - The top 5 visually similar items are returned as recommendations.

4. **Display Results**
   - The recommended items are presented to the user with a preview of the images.

---

## 🛠 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/SahilTwitZ/wardrobe-suggestion.git
cd wardrobe-suggestion
````

### 2. Install Required Dependencies

Ensure Python 3.8+ is installed. Then install dependencies:

```bash
pip install -r requirements.txt
```

### 3. Set Up Your Dataset

* Add your clothing images to the `images/` directory.
* Run the following to preprocess and extract features:

```bash
python main.py
```

This generates:

* `embeddings.pkl`: Image feature vectors
* `filenames.pkl`: Image filenames

### 4. Launch the Web App

```bash
streamlit run app.py
```
---

## 🧠 Technologies Used

* **Frontend**:

  * Streamlit (UI framework)
* **Machine Learning**:

  * TensorFlow & Keras (ResNet50)
  * Scikit-learn (k-NN algorithm)
* **Programming Language**:

  * Python

---

## 🚀 Future Enhancements

* Add filtering options (e.g., color, type, brand).
* Implement personalized recommendations using user history or feedback.
* Expand to suggest complementary fashion items (e.g., accessories, shoes).

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for full details.

---

## 🙏 Acknowledgments

* [ResNet50](https://keras.io/api/applications/resnet/) – Used for image feature extraction.
* [Streamlit](https://streamlit.io/) – Enables the web-based user interface.
