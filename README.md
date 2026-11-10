# Hyderabad Road Risk AI 🚦

An AI-based project that explores road safety in Hyderabad by identifying road segments that may have a higher risk of accidents.

## About the Project

Road accidents are a major concern, especially in busy cities like Hyderabad. Some roads may be more accident-prone because of their layout, traffic conditions, speed limits, and other factors.

This project uses road information, accident-related data, and machine learning to study road segments and classify them into three risk levels:

- **Low Risk**
- **Medium Risk**
- **High Risk**

The aim is to make road safety information easier to understand through a simple interactive map and dashboard.

## What Can It Do?

- Display road segments on an interactive map of Hyderabad.
- Predict the risk level of a selected road segment.
- Search for roads by name.
- View accident-related information.
- Show basic statistics through a dashboard.
- Use a LightGBM machine learning model for road risk classification.

## Technologies Used

| Area | Technologies |
|---|---|
| Programming | Python |
| Machine Learning | LightGBM |
| Data Processing | Pandas |
| Backend | Flask |
| Frontend | HTML, CSS, JavaScript |
| Map | Leaflet.js |
| Map Data | OpenStreetMap, OSMnx |
| Weather Data | Open-Meteo |
| Model Storage | Joblib |

## How the Prediction Works

The model uses road-related features such as:

- Road type
- Speed limit
- One-way information
- Road length
- Number of lanes
- Road geometry
- Distance between road endpoints
- Road shape complexity

These features are processed by the trained LightGBM model to predict a risk category.

## Project Structure

```text
Hyderabad-Road-Risk-AI/
│
├── app/
│   ├── app.py
│   └── index.html
│
├── models/
│   └── road_risk_model.pkl
│
├── data/
│   ├── hyderabad_accidents_clean.csv
│   └── hyderabad_ml_predictions.csv
│
├── scripts/
│
├── requirements.txt
├── .gitignore
└── README.md
```

## Getting Started

Follow these steps to run the project on your computer.

**1. Clone the repository**

```bash
git clone https://github.com/flowerfork/-Road-Segment-Risk-Classification-Using-Decision-Trees-and-LightGBM.git
```

**2. Open the project folder**

```bash
cd -Road-Segment-Risk-Classification-Using-Decision-Trees-and-LightGBM
```

**3. Create a virtual environment**

```bash
python -m venv venv
```

**4. Activate the environment**

For Windows:

```bash
venv\Scripts\activate
```

For Linux/macOS:

```bash
source venv/bin/activate
```

**5. Install the required libraries**

```bash
pip install -r requirements.txt
```

**6. Run the application**

```bash
python app/app.py
```

Open the following address in your browser:

```text
http://127.0.0.1:5000
```

Make sure the required dataset and trained model files are available in their respective folders before running the application.

## API Endpoints

The Flask application provides the following endpoints:

| Endpoint | Purpose |
|---|---|
| `/` | Opens the main dashboard |
| `/api/stats` | Returns dashboard statistics |
| `/api/search?q=roadname` | Searches for a road |
| `/api/roads` | Returns road information |
| `/api/predict` | Predicts road risk |
| `/api/accidents` | Returns accident-related information |

## Data and Limitations

The project uses road network information from OpenStreetMap and weather information from Open-Meteo, along with accident-related datasets.

Some accident-related attributes used during development were synthetically generated. Therefore, the predictions should be treated as experimental results rather than official accident-risk assessments.

The system is intended for learning and demonstration purposes. It should not be used as the only source for real-world road safety decisions.

## Future Improvements

There are several ways this project could be improved:

- Include more verified historical accident records.
- Improve prediction accuracy with additional real-world data.
- Add live traffic information.
- Expand the analysis to more areas.
- Improve the dashboard with more detailed visualizations.

## Author

**Mahathi**

GitHub: [@flowerfork](https://github.com/flowerfork)

---

*Built as a project to explore how machine learning and map-based data can be used to understand road safety.*
