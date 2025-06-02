## 👗 Fashion Recommendation System Using Image Features

This project builds a **content-based fashion recommendation system** that suggests visually similar fashion products using **image embeddings** extracted via a deep learning model (e.g., ResNet).

---

### 📌 Features

* Uses a **pre-trained CNN** (ResNet50) to extract high-level visual features from product images.
* Computes image embeddings and stores them using efficient data structures.
* Uses **nearest neighbors** (via cosine similarity) to find visually similar products.
* Displays top-N recommended images for a given query product.

---

### 🧰 Requirements

Install the required Python libraries:

```bash
pip install numpy pandas matplotlib scikit-learn opencv-python tensorflow keras
```


### 🧠 How It Works

1. **Image Preprocessing**
   All images are resized and converted to format suitable for ResNet.

2. **Feature Extraction**

   * Uses pre-trained `ResNet50` (from Keras) with the top classification layer removed.
   * Embeddings are extracted from the `avg_pool` layer.

3. **Similarity Matching**

   * Cosine similarity is calculated between the query image and the dataset.
   * Top-N similar images are retrieved and displayed.

4. **Visualization**

   * Query image + similar recommendations shown using `matplotlib`.


### 📦 Optional Improvements

* Use **FAISS** or **Annoy** for faster similarity search.
* Add **text-based filtering** (e.g., categories, color).
* Deploy using **Streamlit** or **Gradio** for an interactive web app.

---

### 🙏 Credits

Inspired by [AmanXAI - Fashion Recommendation System using Image Features](https://amanxai.com/2024/02/05/fashion-recommendation-system-using-image-features/)

---

### 📄 License

MIT License — use freely, modify, and share.
