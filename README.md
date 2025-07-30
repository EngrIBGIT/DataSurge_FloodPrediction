# FloodPrediction
## FloodGuardEdge  

**AI-powered Flood Prediction App for Nigeria**   

Combines geospatial intelligence, machine learning, and real-time weather to help predict urban flood risks.

---
## Features
- **Satellite Data Integration** (CHIRPS, SRTM, MODIS)
- **ETL, EDA & ML modeling** using Python & SHAP
- **ML Models**: RF, XGBoost, LightGBM, ANN, etc.
- **Weather Forecast** integration with OpenWeatherMap API
- **Nigeria Map Tab** with real-time data and scrolling info
- **Offline support** for field use (pre-cached weather, saved models)
- UI via **Streamlit**, backend via **FastAPI**


---

## 📁 Project Structure
```
FloodGuardEdge/
├── app.py                  # Streamlit UI
├── main.py                 # FastAPI API backend
├── data/
│   ├── raw/                # Downloaded rasters
│   └── processed/          # Cleaned CSVs, cached weather
├── models/                 # Trained models (pkl, h5)
├── figures/                # Visualizations & SHAP plots
├── notebooks/              # etl.ipynb, eda.ipynb, prediction.ipynb
├── src/
│   ├── etl.py              # Data collection and transformation
│   ├── prediction.py       # Modeling and explainability
│   └── utils.py            # Weather API + location features
├── tests/                  # Unit tests
├── .env                    # API Keys
├── requirements.txt        # Python dependencies
└── README.md
```


##  Getting Started
```bash
# Clone the repo
$ git clone https://github.com/your-username/FloodGuardEdge.git
$ cd FloodGuardEdge

# Install dependencies
$ pip install -r requirements.txt

# Set your OpenWeatherMap API Key
$ echo "OPENWEATHER_API=your_key_here" > .env

# Run the ETL pipeline
$ python src/etl.py

# Train model (or use pre-saved models)
$ python src/prediction.py

# Launch the Streamlit dashboard
$ streamlit run app.py

# Start API server
$ uvicorn main:app --reload
```






---
---
