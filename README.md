# Earthquake Anomaly Detection using Machine Learning

Welcome to the **Earthquake Anomaly Detection** project! This repository showcases the detection of anomalies in a dataset of earthquakes in Indonesia using machine learning techniques. The anomalies detected are validated against actual tsunami events to identify outliers that may be indicative of future tsunamis.

## Project Overview

This project involves:
- **Data Preprocessing**: Merging earthquake date and time fields, extracting useful features, and cleaning the data.
- **Anomaly Detection**: Using three different machine learning models—**Isolation Forest**, **One-Class SVM**, and **Elliptic Envelope**—to identify anomalous earthquakes.
- **Validation**: Comparing anomalies detected by the models with actual tsunami events using a dataset of historical tsunami data.
- **Analysis and Recommendations**: Reporting the results, including model comparison and recommendations for improving the accuracy of government earthquake and tsunami data.

## Dataset

- **Earthquake Dataset**: A dataset consisting of earthquake events in Indonesia, with features like magnitude, depth, latitude, and longitude.
- **Tsunami Dataset**: A dataset from NOAA with historical records of tsunami events, including dates, times, and locations.

## Models Used

- **Isolation Forest**: A model that isolates observations by randomly selecting features and splitting the data to detect anomalies.
- **One-Class SVM**: A support vector machine technique for identifying the boundary that separates normal data from outliers.
- **Elliptic Envelope**: A model that fits a multivariate Gaussian distribution to the data and detects points that do not fit the distribution.

### Key Results

- **Anomalies Detected**:
  - Isolation Forest: 4,645 anomalies
  - One-Class SVM: 4,651 anomalies
  - Elliptic Envelope: 929 anomalies

- **Model Comparison**: The **Elliptic Envelope** model was chosen as the most accurate based on overlap with the other models and its ability to detect meaningful anomalies.

### Tsunami Event Validation
Anomalies detected by the **Elliptic Envelope** model were compared with the actual tsunami data to verify if the detected anomalies corresponded to real-world tsunami events.

## Structure of the Repository

```
├── data/                        # Contains datasets for earthquakes and tsunamis
├── notebooks/                   # Jupyter Notebooks for data analysis and model training
├── scripts/                     # Python scripts for preprocessing, model training, and validation
├── README.md                    # Project overview and instructions (this file)
└── requirements.txt             # List of required Python libraries
```

## Installation and Setup

To get started, clone the repository and set up your environment:

```bash
git clone https://github.com/3m0r9/Earthquake-Anomaly-Detection.git
cd Earthquake-Anomaly-Detection
```

Create a virtual environment and install dependencies:

```bash
python3 -m venv env
source env/bin/activate   # On Windows use 'env\Scripts\activate'
pip install -r requirements.txt
```

## Running the Jupyter Notebooks

You can explore the data and run the models by opening the Jupyter notebooks in the `notebooks/` folder. To launch the Jupyter environment:

```bash
jupyter notebook
```

## Key Files

- **notebooks/Elliptic_Envelope.ipynb**: The Jupyter notebook for the Elliptic Envelope model, which detects anomalies and compares them to actual tsunami events.
- **data/NOAA_Tsunamis.xlsx**: The dataset of historical tsunami events used for validation.
- **scripts/preprocessing.py**: Preprocessing script to clean and prepare the earthquake dataset.
- **scripts/anomaly_detection.py**: Script that applies the machine learning models to detect anomalies.

## Future Work

- Implement additional machine learning models and compare performance.
- Refine the contamination parameter for more accurate anomaly detection.
- Integrate more features such as seismic wave analysis for better prediction accuracy.

## Contributing

Feel free to submit pull requests or report issues if you would like to contribute to the project!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

