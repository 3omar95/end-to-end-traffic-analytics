# 🚦 End-to-End Traffic Forecasting System

This repository contains my Master’s Graduation Project in Data Science at Northumbria University.  
The project is a complete pipeline combining Computer Vision, Time-Series Forecasting, and Web Deployment to deliver a traffic monitoring and prediction system.

---

## 📌 Project Aim  
The aim of this project is to design an intelligent monitoring system to:  
- Detect and count vehicles from CCTV footage using deep learning.  
- Forecast traffic volume for the next hour using advanced ML models.  
- Provide an *interactive dashboard* for end-users (city planners, transport authorities).  

---

## 🐍 Python Libraries Used  
- *NumPy & Pandas* – Data manipulation and preprocessing.  
- *Matplotlib & Seaborn* – Exploratory Data Analysis and visualizations.  
- *Scikit-Learn* – Preprocessing (scaling, encoding, PCA) and evaluation metrics.  
- *Ultralytics YOLOv8 & Supervision* – Vehicle detection and multi-object tracking.  
- *TensorFlow* – Building and training deep learning forecasting models (LSTM, GRU, ConvLSTM).  
- *XGBoost* – Gradient boosting for efficient forecasting.  
- *Dash & Plotly* – Interactive web interface and visualizations.  

---

## 🤖 Machine Learning Models  

### *Vehicle Detection & Tracking*  
- *YOLOv8* → Object detection (cars, trucks, buses).  
- *BYTETrack* → Multi-object tracking to prevent duplicate counts.  

### *Traffic Forecasting*  
- *XGBoost (with PCA)* → Best performance and fastest training.  
- *LSTM* → Capturing temporal dependencies.  
- *GRU* → Lightweight recurrent model, faster than LSTM.  
- *ConvLSTM* → Spatiotemporal deep learning architecture.  

---

## 📊 Results and Findings  

| Model         | MAE   | R²     | MAPE   | Notes |
|---------------|-------|--------|--------|-------|
| *XGBoost+PCA* | 50.35 | 0.9746 | 20.6% | ✅ Best generalization |
| GRU (DL)      | 59.75 | 0.9689 | 21.6% | Strong but slower |
| LSTM (DL)     | Similar to GRU | Good fit | Higher training time |
| ConvLSTM      | High cost | Limited by hardware | - |

*Key Insights:*  
- *Time features* (hour, day, weekday) strongly influenced traffic flow.  
- *Weather* had *minimal impact* on vehicle volume.  
- Roads with *more lanes* consistently carried higher traffic.  

📌 *Vehicle Detection* – YOLOv8 + BYTETrack achieved accurate lane-based counts.  
📌 *Forecasting* – XGBoost with PCA consistently outperformed deep learning models.  

### Vehicle Detection & Tracking  
YOLOv8 + BYTETrack achieved accurate lane-based vehicle counts.

![Tracking Model Output](https://github.com/3omar95/end-to-end-traffic-analytics/blob/main/assets/Tracking%20Model%20Output.png)

---

### Forecasting Models Evaluation  
XGBoost with PCA achieved the best overall performance compared to LSTM, GRU, and ConvLSTM.

![Forecasting Models Evaluation](assets/figure_33.png)

---

### Web Deployment Interface  
The system was deployed using *Dash* and *Plotly*, providing:  
- Tabs for *Vehicle Counting* and *Forecasting*.  
- Interactive visualizations with *Plotly*.  
- User inputs for selecting station/location.  
- Dashboard presenting *forecasts, trends, and insights*.  


![Web Interface](assets/figure_34.png)

---

## 🚀 Future Improvements  
- Cloud-based training (*AWS / GCP*) to overcome hardware limits.  
- Real-time CCTV streaming for live monitoring.  
- Unsupervised clustering to categorize *high vs. low congestion*.  
- Enhanced web UI for traffic planners.  
- Integration with IoT sensors for richer insights.  

---

## 🔗 Resources  

- 📂 *Source Code & Notebooks*: [Google Drive Repository](https://drive.google.com/drive/folders/1hU5GHbE47gstaFcwrr3CpgQAXeB1nZKV?usp=drive_link)  
- 📂 *Traffic & Weather Datasets*: [MnDOT + Weather Data](https://drive.google.com/drive/folders/1f4xcXT4rdOYEy28M2Gte5-8NoEdIMeOt?usp=drive_link)  

---

## ✅ Skills Demonstrated  
- Data Cleaning & Feature Engineering  
- Computer Vision (YOLOv8, BYTETrack)  
- Forecasting with ML & DL (XGBoost, LSTM, GRU, ConvLSTM)  
- Evaluation Metrics & Model Comparison  
- Interactive Deployment (Dash/Plotly)  

This project demonstrates *end-to-end data science expertise, with real-world applications in **Smart Cities and Intelligent Transport Systems (ITS)*.  

---
