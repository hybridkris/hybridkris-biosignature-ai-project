# 🌌 Biosignature AI Project

This project combines bioinformatics, exoplanetary data, and machine learning to predict the viability of extremophile organisms surviving on discovered exoplanets. It includes real genome metadata from NCBI, NASA exoplanet archives, and integrates with the Unistellar Odyssey telescope for observational follow-up.

---

## ✨ Key Features
- **Real extremophile genome data** from NCBI Datasets CLI
- **Exoplanet environmental data** from NASA Exoplanet Archive
- **Feature engineering** for biological and environmental compatibility
- **Machine learning** model (logistic regression and optional random forest)
- **Prediction of biosignature viability** for organism-planet pairs
- **Telescope-ready target links** (Unistellar Odyssey deep links)
- **QR code generation** for telescope pointing
- **Data export to Google Drive as CSV**

---

## 📊 Dataset Inputs
### 1. Extremophiles
- Thermophiles, Psychrophiles, Halophiles from known genera
- Features: `gc_content`, `genome_size`, `is_hot_adapted`, `is_cold_adapted`, `is_salt_adapted`, `is_aerobic`

### 2. Exoplanets
- Extracted from `pscomppars` table
- Features: `equilibrium_temp`, `radius_Earth`, `mass_Earth`, `ra`, `dec`

---

## 🧰 Pipeline Overview
1. **Extract** genome metadata using the NCBI Datasets CLI
2. **Label** organisms based on environment keywords
3. **Query** exoplanet data from NASA with RA/Dec and physical traits
4. **Pair** genomes with planets and assign viability labels
5. **Train** a logistic regression model (or upgrade to Random Forest)
6. **Score** all pairings and rank by viability likelihood
7. **Generate** Unistellar links + QR codes
8. **Export** the results to Google Drive

---

## 🔧 Usage Instructions
1. Run the full Colab notebook
2. Upload genome `.jsonl` files using NCBI CLI
3. Execute all code cells to:
   - Generate pairings
   - Train the model
   - Visualize predictions
   - Export data
4. Mount Google Drive and check for `biosignature_predictions_with_links.csv`

---

## 🌐 Output
Each prediction includes:
- Organism name
- Planet name
- Predicted biosignature match probability
- RA/Dec (for telescope targeting)
- Deep link to Unistellar Odyssey
- QR code link

---

## 🌟 Future Improvements
- Add support for additional adaptation traits (e.g., pH, radiation resistance)
- Use a neural network model
- Build a public-facing web interface with Streamlit
- Integrate live telescope controls

---

## 📄 File Export Location
All predictions are saved to:
```
/content/drive/MyDrive/biosignature_predictions_with_links.csv
```

---

## 🚀 Authors & Credits
- AI design, model training, and engineering: You + ChatGPT
- Genomic data: NCBI Datasets API
- Exoplanet data: NASA Exoplanet Archive
- Telescope integration: Unistellar Odyssey

---
