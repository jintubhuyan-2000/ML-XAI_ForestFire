
# Fire Risk Modeling and Region Transfer Tutorial

Author: **Jintu Moni Bhuyan**  
GitHub Repository: [ML-XAI_ForestFire](https://github.com/jintubhuyan-2000/ML-XAI_ForestFire/tree/main)

---

## 1. Introduction
This tutorial provides step-by-step instructions to run the Fire Risk Modeling workflow and perform Region Transfer validation using **Google Colab** without the need to manually mount Google Drive.  
Instead, data will be directly downloaded from Google Drive using the `gdown` library.

---

## 2. Requirements
Before starting, ensure you have the following:
- Google Colab account  
- GitHub access to the project repository  
- `gdown` library for downloading data  

---

## 3. Running the Fire Risk Model

### **Step 1: Open the Notebook**
1. Go to the following link: [Fire_Risk_RF_Model_Performance.ipynb](https://github.com/jintubhuyan-2000/ML-XAI_ForestFire/blob/main/Fire_Risk_RF_Model_Performance.ipynb)
2. Click **'Open in Colab'**.

### **Step 2: Install gdown and Download the Data**
Run the following commands in Colab:

```python
!pip install gdown --quiet

# Use gdown to download the folder
!gdown "https://drive.google.com/drive/u/0/folders/1VwmSpoD6wxw1WCTQwjK55155gcR8hoRn" --folder
```

**Folder Structure After Download:**  
```
/content/California_Fire_MS/Fire_Risk_RF_Model_Performance/Performance Data
│   FireRisk_Validation_RF_AUC_forest.csv
│   FireRisk_Validation_RF_AUC_grassland.csv
```

### **Step 3: Verify Downloaded Files**
Ensure the following two CSV files are present:
- `FireRisk_Validation_RF_AUC_forest.csv`
- `FireRisk_Validation_RF_AUC_grassland.csv`

### **Step 4: Run the Notebook**
Go to **Runtime > Run all** to execute all cells.  
Results will be saved automatically in:

```
/content/California_Fire_MS/Fire_Risk_RF_Model_Performance/Results
```

---

## 4. Region Transfer Validation

### **Step 1: Open the Region Transfer Notebook**
1. Go to the following link: [RegionTransfer_California_FinalRevised2.ipynb](https://github.com/jintubhuyan-2000/ML-XAI_ForestFire/blob/main/RegionTransfer_California_FinalRevised2.ipynb)
2. Click **'Open in Colab'**.

### **Step 2: Folder Structure for Validation**
Ensure these two folders exist:

```
/content/California_Fire_MS/Fire_Risk_Validation/grassland/Validation Datasets
/content/California_Fire_MS/Fire_Risk_Validation/forest/Validation Datasets
```

When saving results, increment the version folder names (e.g., `V6`, `V7`, `V8`) to avoid overwriting.

**Example:**
```
/content/California_Fire_MS/Fire_Risk_Validation/grassland/Results/results_region_transfer_V6
```

### **Step 3: Run and Save**
Update result directory paths in the code blocks, run the notebook, and results will be saved automatically to the newly created folders.

---

## 5. Temporal Split
The temporal split process follows the **same steps as Region Transfer**.

---

## 6. Video Tutorial
Watch the full tutorial video [here](https://drive.google.com/file/d/1yQ6a-StNYA8H6LFAwYlH8tixj6RJPcOX/view?usp=sharing).

---
