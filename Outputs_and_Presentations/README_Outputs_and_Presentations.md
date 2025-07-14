# Outputs and Presentations

This folder contains **scientific outputs** and **presentations** related to the **Yishi Project**.

---

## 📁 Subfolder Structure

### 📄 Publications

Contains all scientific products associated with the project, including:

- Posters
- The Amirim program project
- A Master's thesis
- Peer-reviewed scientific papers

#### 📚 Published Papers

1. **Leaf Water Potential in a Mixed Mediterranean Forest from Machine Learning and Unmanned Aerial Vehicle (UAV)-Based Hyperspectral Imaging**  
   [https://www.mdpi.com/3115264](https://www.mdpi.com/3115264)

2. *(Preprint)* **Early Detection of Drought-Stressed Stands in Mediterranean Forests Using Machine Learning Classification Models and a Rainfall Exclusion Experiment**  
   [https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5292430](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5292430)

---

### 📊 Presentations

Includes:

- Project presentations
- Visualizations of results from various analyses  
  *(many of these figures appear in the published papers)*
- Photos taken during fieldwork

---

### 🧠 Models

Contains models developed during the project, along with the corresponding code.

#### Subfolders:

- **`LWP_Modeling/`**  
  Includes models developed to predict **Leaf Water Potential (LWP)** based on spectral data:  
  - NDSI linear models  
  - Machine learning models (e.g., RF, XGB, SVM)  
  These models and results are presented in the first paper (see "Publications").

- **`Classification_models/`**  
  Contains ML models built to classify tree canopies as **"Drought"** vs. **"Control"**:  
  - `LWP_Treatment_Classification.py` – tests multiple classification algorithms  
  - `Predict-Drought-Classification.py` – a focused script using the best-performing model (SVM) to generate prediction maps  
  - The improved **SVM model** was deployed as a **Streamlit app**, available in the [`Streamlit_App_Classification_Model`](../Streamlit_App_Classification_Model/) folder.
