## 🎵 Clustering Music Tracks using Spotify Dataset

This project analyzes and clusters music tracks based on their audio features from a dataset of 2000 songs spanning different years, artists, and genres. It uses unsupervised machine learning techniques to explore patterns in musical characteristics.

---

### 📁 Dataset

**File:** `Spotify-2000.csv`

Contains 2000 music tracks with the following features:

* **Categorical:** Title, Artist, Top Genre, Year
* **Numerical:** BPM, Energy, Danceability, Loudness, Liveness, Valence, Duration, Acousticness, Speechiness, Popularity

---

### 📒 Notebook Overview

**File:** `clustering music.ipynb`

#### 📌 Key Steps:

1. **Importing Libraries**

   * `pandas`, `numpy`, `sklearn.cluster`

2. **Loading Dataset**

   ```python
   data = pd.read_csv("Spotify-2000.csv")
   ```

3. **Correlation Analysis**

   * Compute correlation matrix for all numeric features:

     ```python
     numeric_data = data.select_dtypes(include='number')
     correlation_matrix = numeric_data.corr()
     ```

4. **Data Cleaning**

   * Identifies and separates non-numeric columns.
   * (Optionally) converts string-formatted durations to numeric seconds.

5. **(Expected Next Steps - Add these if missing)**

   * Feature scaling (StandardScaler / MinMaxScaler)
   * KMeans clustering or DBSCAN
   * Elbow method / silhouette score for cluster tuning
   * PCA or t-SNE for visualization

---

### 📊 Possible Improvements

* Convert `"Length (Duration)"` to seconds if in `mm:ss` format.
* Drop or encode categorical variables.
* Add clustering visualizations using Seaborn or Plotly.

---

### 🚀 How to Run

1. Clone the repo or download the files.
2. Install required packages:

   ```bash
   pip install pandas numpy scikit-learn jupyter
   ```
3. Open the notebook:

   ```bash
   jupyter notebook clustering\ music.ipynb
   ```

---

### 📈 Output

* Correlation matrix between audio features
* Cluster assignments (to be added)
* Visualizations (to be added)

---

### 🧠 Technologies Used

* Python 3
* Jupyter Notebook
* Pandas, NumPy
* Scikit-learn (for clustering)

---

### 🗂 Folder Structure

```
project-folder/
│
├── Spotify-2000.csv           # Dataset
├── clustering music.ipynb     # Main notebook
└── README.md                  # Project overview
