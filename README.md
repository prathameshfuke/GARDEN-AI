# EcoIrrigate: Smart Irrigation and Water Quality Prediction System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://travis-ci.com/yourusername/ecoirrigate.svg?branch=main)](https://travis-ci.com/yourusername/ecoirrigate)
[![Contributors](https://img.shields.io/github/contributors/yourusername/ecoirrigate)](https://github.com/yourusername/ecoirrigate/graphs/contributors)

EcoIrrigate is an innovative, open-source project that combines advanced garden automation with real-time water quality prediction powered by machine learning. Designed for hobbyists, researchers, and eco-conscious gardeners, this system harnesses sensor data, Raspberry Pi technology, and robust ML models to optimize garden care, conserve water, and maximize plant health.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Modules](#modules)
  - [Dataset Collection](#dataset-collection)
  - [Data Preprocessing](#data-preprocessing)
  - [Data Visualization](#data-visualization)
  - [Machine Learning Models](#machine-learning-models)
  - [Water Quality Classification & Prediction](#water-quality-classification--prediction)
- [Performance Metrics](#performance-metrics)
- [System Specifications](#system-specifications)
- [Development](#development)
- [Deployment](#deployment)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Future Enhancements](#future-enhancements)
- [Contributors](#contributors)
- [License](#license)

---

## Project Overview

EcoIrrigate streamlines garden management by merging smart sensor integration with advanced water quality analytics. The system continuously monitors environmental and water quality parameters, processes the data with machine learning algorithms such as Random Forest and Gaussian Naive Bayes, and automatically controls irrigation. This ensures that your garden receives precise watering tailored to current conditions, thereby enhancing plant growth and conserving valuable water resources.

---

## Features

- **Automated Irrigation Control:** Dynamically adjusts watering schedules based on real-time water quality predictions.
- **Machine Learning Integration:** Employs ensemble and probabilistic classifiers for accurate analysis.
- **Comprehensive Sensor Suite:** Monitors water temperature, pH levels, light intensity, humidity, barometric pressure, and soil moisture.
- **Data Preprocessing & Visualization:** Processes raw sensor data and provides insightful visualizations.
- **User-Friendly Web Interface:** Easily monitor system performance and garden status via a web dashboard.
- **Modular & Scalable:** Built with modular components to allow seamless upgrades and integration of additional features.

---

## Modules

### Dataset Collection

EcoIrrigate gathers critical environmental data using a variety of sensors:
- **Water Temperature Sensor:** Monitors water temperature to determine optimal irrigation conditions.
- **pH Sensor:** Evaluates the acidity or alkalinity of water.
- **Light Intensity Sensor:** Measures turbidity to assess water clarity.
- **DHT22 Sensor:** Records ambient temperature and humidity.
- **BMP180 Sensor:** Captures barometric pressure.
- **Soil Moisture Sensor:** Detects moisture levels in the soil for precise watering control.

### Data Preprocessing

Raw sensor data is refined through several preprocessing steps:
- **Data Cleaning:** Removal of noise and correction of anomalies.
- **Handling Missing Values:** Imputation and exclusion of incomplete records.
- **Feature Scaling:** Normalization of data to enhance model performance.
- **Feature Selection:** Identification of key parameters influencing water quality.

### Data Visualization

A suite of visualization tools is used to uncover trends and patterns:
- **Pie Charts & Count Plots:** Analyze categorical distributions.
- **Distribution & KDE Plots:** Visualize the spread and density of data.
- **Correlation Matrices:** Identify relationships among variables.
- **Pandas Profile Reports:** Provide comprehensive overviews of the dataset.

### Machine Learning Models

EcoIrrigate leverages two primary ML algorithms:
- **Random Forest:** An ensemble method that aggregates multiple decision trees to improve prediction accuracy.
- **Gaussian Naive Bayes:** A probabilistic model based on Bayes’ theorem, suitable for continuous data analysis.

### Water Quality Classification & Prediction

This critical module is responsible for:
- **Classifying Water Samples:** Assessing water quality based on sensor data.
- **Predicting Irrigation Suitability:** Determining if water conditions are optimal for plant irrigation.
- **Scheduling Irrigation:** Automatically setting watering schedules based on predictive insights.
- **Irrigation Control:** Activating and regulating garden watering systems.

---

## Performance Metrics

To measure and refine the system’s accuracy, the following metrics are utilized:
- **Accuracy:** Overall correctness of the prediction.
- **Precision:** Exactness of the predictions.
- **Recall:** Ability to capture all relevant cases.
- **F1 Score:** Harmonic mean of precision and recall.
- **Confusion Matrix:** Detailed breakdown of true vs. false predictions.

---

## System Specifications

| **Component**           | **Details**                                      |
|-------------------------|--------------------------------------------------|
| **Operating System**    | Ubuntu Server 22.04                              |
| **Hardware**            | Raspberry Pi 4                                   |
| **Sensors**             | DHT22, BMP180, Soil Moisture, pH Sensor, Temperature Sensor |
| **Frameworks & Tools**  | TensorFlow, OpenCV, Django                       |

---

## Development

To set up the development environment using Docker, execute the following command:

```bash
docker build -t yourusername/ecoirrigate:latest -f docker/devel.dockerfile .
```

---

## Deployment

### Install System Packages

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install python3-lgpio python3-pip -y
```

### Clone the Repository

```bash
git clone https://github.com/yourusername/ecoirrigate.git
cd ecoirrigate/
```

### Install Python Dependencies

```bash
python3 -m pip install -r requirements.txt --no-cache-dir
```

### Launch the Application

```bash
cd ecoirrigate/
python3 manage.py runserver 0:8000
```

---

## Contributors

- **Prathamesh Fuke** – Project Lead, Developer, and Contributor

---

## License

This project is licensed under the [MIT License](LICENSE).
