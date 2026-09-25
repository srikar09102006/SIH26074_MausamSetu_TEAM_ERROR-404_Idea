# MausamSetu

### Panchayat-Level Weather Downscaling & Agro-Meteorological Advisory Platform

**Smart India Hackathon 2026 — Prototype**

**Problem Statement:**
**Downscaling of weather forecast from Block level to Panchayat level for agro-meteorological advisory services**

**Ministry:** Ministry of Earth Sciences (MoES)

---

## 📌 Overview

**MausamSetu** is a web-based prototype designed to demonstrate how block-level weather forecasts can be transformed into **localized Panchayat-level weather intelligence** for agricultural decision-making.

Weather conditions can vary significantly within a single administrative block. A forecast available only at the Block level may therefore not adequately represent conditions at individual Panchayats.

MausamSetu addresses this challenge by combining block-level forecast information with localized spatial variations to generate **Panchayat-level demonstration estimates** for parameters such as:

* 🌧️ Rainfall
* 🌡️ Temperature
* 💧 Relative humidity
* 💨 Wind speed
* 🌱 Estimated soil-moisture indicator
* ⚠️ Weather-related agricultural risk

The platform then converts this information into **action-oriented agro-meteorological advisories**.

---

## 🎯 Objective

The primary objective of MausamSetu is to demonstrate a scalable system for:

> **Downscaling coarse-resolution weather information into finer Panchayat-level information and using it to support agricultural advisories.**

The prototype focuses on providing an intuitive interface through which agricultural officers and other stakeholders can:

1. Select a district and block.
2. View the associated Panchayats.
3. Visualize localized weather conditions.
4. Explore multi-day forecasts.
5. Identify Panchayats with elevated weather risks.
6. Generate weather-based agricultural guidance.
7. Review alerts.
8. Export Panchayat-level forecast data.

---

## 🧩 Key Features

### 1. Panchayat-Level Weather Map

The dashboard provides a spatial representation of Panchayats within the selected Block.

Users can switch between:

* **Rainfall**
* **Temperature**
* **Soil Moisture**

The map highlights different Panchayats according to the selected weather variable and allows individual Panchayats to be selected for detailed information.

---

### 2. Block → Panchayat Downscaling

The prototype demonstrates the central concept of the problem statement:

```text
Block-Level Weather Forecast
            ↓
   Spatial Downscaling
            ↓
Panchayat-Level Estimates
            ↓
Agro-Meteorological Advisory
```

Panchayat values are generated as localized variations around the selected Block forecast.

This prototype implementation is intended to demonstrate the **downscaling workflow and user experience**. The current Panchayat-level values are explicitly treated as demonstration estimates rather than official meteorological observations.

---

### 3. Weather Forecast Explorer

MausamSetu provides a multi-day weather forecast interface containing:

* Daily rainfall
* Maximum temperature
* Minimum temperature
* Forecast trends
* Selected-date analysis

Users can navigate between forecast periods and select individual forecast days for further analysis.

---

### 4. Agro-Meteorological Advisory Center

The platform converts weather conditions into simple agricultural guidance.

Examples include:

* Heavy rainfall precautions
* Irrigation guidance
* Crop-care recommendations
* Recommendations to postpone spraying during unsuitable weather
* Harvest protection guidance
* Heat-stress precautions

The prototype includes crop selection for:

* Grapes
* Onion
* Maize
* Soybean
* Pomegranate

---

### 5. Weather Risk & Alerts

Panchayats are categorized according to weather-related risk levels:

* **Low**
* **Medium**
* **High**

The prototype provides alerts for conditions such as:

* Heavy rainfall
* Rainfall-related risks
* High-temperature conditions

The alert center allows users to review active alerts.

---

### 6. Panchayat Comparison

Users can compare Panchayats within the selected Block using:

| Parameter   | Description                    |
| ----------- | ------------------------------ |
| Rainfall    | Estimated rainfall             |
| Temperature | Estimated temperature          |
| Risk        | Weather-related risk category  |
| Confidence  | Prototype confidence indicator |

The comparison can be expanded to display all Panchayats available in the prototype dataset.

---

### 7. Reports & Data Export

MausamSetu provides a downloadable CSV report containing Panchayat-level information such as:

* Panchayat name
* Rainfall
* Temperature
* Humidity
* Confidence
* Risk

This can support further analysis and reporting workflows.

---

### 8. Location-Aware Forecasting

The prototype supports multiple District → Block combinations.

Currently demonstrated locations include:

#### Nashik

* Niphad
* Sinnar
* Dindori

#### Pune

* Haveli
* Baramati
* Junnar

#### Ahmednagar

* Rahuri
* Shrigonda
* Karjat

Each location is associated with prototype Panchayat names and geographic coordinates.

---

## 🏗️ System Architecture

The conceptual architecture of MausamSetu is:

```text
                 WEATHER DATA
                      │
                      ▼
          Block-Level Forecast
                      │
                      ▼
          Data Preprocessing
                      │
                      ▼
          Spatial Downscaling
                      │
        ┌─────────────┴─────────────┐
        ▼                           ▼
 Panchayat Weather            Weather Variables
    Estimates              Rain | Temp | Humidity
        │                   Wind | Moisture
        └─────────────┬─────────────┘
                      ▼
             Risk Assessment
                      │
                      ▼
          Agro-Meteorological
               Advisory
                      │
                      ▼
             Web Dashboard
```

---

## 🌐 Data Source

The prototype integrates with the **Open-Meteo forecast API** to obtain weather information for the selected Block location when an online connection is available.

T
