# NVIDIA Stock Forecasting with FinBERT

This open-source project explores **time series forecasting** of NVIDIA stock prices using deep learning models and sentiment analysis with **FinBERT**.  
The pipeline includes multiple models with different lookback windows (1D, 14D, 30D, 60D, 90D, 180D, 270D, 365D), feature engineering, and an ensemble meta-model that integrates predictions with sentiment signals.

---

## Project Structure

- **Week 1**: Exploratory Data Analysis & Feature Engineering
- **Week 2–3**: Model training with Simple Attention across various lookback windows
- **Week 4**: Meta-model training (ensemble with Ridge regression)
- **Week 5**: Prediction pipeline with sentiment integration via API

---

## Data

- **NVIDIA Stock Dataset**  
  - Source: [Kaggle – Adil Shamim](https://www.kaggle.com/datasets/adilshamim/nvidia-stock-dataset)  
  - License: [CC0 1.0 Universal (Public Domain Dedication)](https://creativecommons.org/publicdomain/zero/1.0/)  
  - Notes: Dataset is in the public domain and free to use. Used for time series forecasting.  

---

## Model

- **FinBERT**  
  - Source: [ProsusAI GitHub Repository](https://github.com/ProsusAI/finBERT)  
  - License: [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)  
  - Notes: FinBERT is not an official Prosus product, but the result of an intern research project.  
    Contacts: Dogu Araci (dogu.araci@prosus.com), Zulkuf Genc (zulkuf.genc@prosus.com).  
  - Model/source transparency and citation continue to apply.  

---

## License

This project’s own code is released under the **MIT License**.  
Third-party components are included under their respective licenses:  

- NVIDIA Stock Dataset — [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)  
- FinBERT — [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0)  

See the [LICENSE](./LICENSE) file for full details.

---

## Citation

If you use this project in your work, please cite:

- Shamim, Adil. *NVIDIA Stock Dataset*. Kaggle. CC0 1.0 Universal.  
- Araci, Dogu & Genc, Zulkuf. *FinBERT*. ProsusAI. Apache License 2.0.  

See [CITATION.cff](./CITATION.cff) for citation metadata.