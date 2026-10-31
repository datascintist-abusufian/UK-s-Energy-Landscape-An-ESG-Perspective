# Machine Learning for Sustainable Data Management in the UK Energy Landscape: An ESG Perspective

This project combines public UK energy statistics, GIS data on renewable-energy sites and synthetic ESG datasets. It uses them to model energy consumption and emissions for businesses and households and to map renewable capacity.

> **Synthetic data notice.** `esg_indv_4000.csv`, `New_Dataset_Individual.xlsx`, `esg_businesses_1000.csv`, `New_Dataset_Business.xlsx`, `VIF_DATASET.xlsx` and the IoT files (`iot_dataset_updated_A.csv`, `iot_data_B.csv`, `external_data.csv`) are **synthetic**. The names, postcodes, demographic attributes and businesses in them are computer-generated. They do not describe real people or companies.

## Data

| File | Content | Type |
| --- | --- | --- |
| `esg_indv_4000.csv`, `New_Dataset_Individual.xlsx` | 4,000 individuals with household energy use by fuel | Synthetic |
| `esg_businesses_1000.csv`, `New_Dataset_Business.xlsx` | 1,000 businesses with sector, turnover and energy use by fuel | Synthetic |
| `VIF_DATASET.xlsx` | Household energy variables used for multicollinearity (VIF) checks | Synthetic |
| `iot_dataset_updated_A.csv`, `iot_data_B.csv`, `external_data.csv` | Smart-meter and grid time series with weather and event data | Synthetic |
| `GIS.csv` | Renewable energy sites (operator, technology, capacity, location) | Public: [Renewable Energy Planning Database](https://www.gov.uk/government/publications/renewable-energy-planning-database-monthly-extract) |
| `Energy1.xlsx` | Regional renewable generation by technology and year | Public: UK energy trends statistics |

`Proper_Dataset_Documentation_UK_energy_Landscape.pdf` describes all six source datasets. These include the DESNZ (formerly BEIS) postcode-level gas statistics, the power emissions pathway to 2037 and the UK power plants data.

## Notebooks

| Notebook | Purpose |
| --- | --- |
| `SteamHouse_17_09_23.ipynb` | Exploratory analysis, ANOVA across datasets, VIF checks and linear regression |
| `Cross_Validation_Result_for_each_ML_model*.ipynb` | Cross-validated comparison of linear regression, decision tree, random forest, XGBoost, LightGBM and CatBoost, before and after tuning |
| `SHAP_IoTdata.ipynb` | Random forest on IoT energy data, Isolation Forest anomaly detection and SHAP/ELI5 explanations |
| `GIS(E).ipynb` | Geospatial mapping of renewable sites with GeoPandas |

`ENERGY_MODELS.html` is an exported report of the model results.

## Running it

```bash
pip install pandas numpy scikit-learn xgboost lightgbm catboost shap eli5 statsmodels geopandas shapely seaborn
```

Some notebooks read from `/content/` (Google Colab) or a local Downloads folder. Change these paths to the repository files.

## Licence

No licence has been declared yet. The public UK government datasets are published under the [Open Government Licence](https://www.nationalarchives.gov.uk/doc/open-government-licence/).

## Author

Md Abu Sufian - ORCID [0009-0007-3503-6942](https://orcid.org/0009-0007-3503-6942)
