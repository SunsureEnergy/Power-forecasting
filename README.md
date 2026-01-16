IES-Ready Power Forecasting Dashboard (Demo)
Overview

This repository documents an in-house power forecasting and analytics capability developed for utility-scale solar plants. The objective is to demonstrate how high-frequency forecasting, automated intraday revisions, and forecast-vs-actual analysis can form a strong foundation for future aggregation, scheduling, and settlement workflows envisioned under the India Energy Stack (IES).

This is an analytics demonstration, not a live market or grid-integrated system.

Why This Exists

As renewable penetration increases, forecasting accuracy and intraday responsiveness become critical — not only for plant operations, but also for deviation management and future transactive energy models.

This work focuses on building the analytics layer first:

Reliable forecasts

Revision discipline

Transparent comparison with actual generation

Quantification of deviation exposure

These capabilities are prerequisites for any future aggregator or IES-aligned participation.

What the Dashboard Demonstrates

The dashboard illustrates the following core capabilities:

Power forecasting driven by satellite-based weather data

Up to 8 automated intraday forecast revisions

Forecast vs actual power comparison at time-block level

15-minute / hourly aligned analytics

Plant-level and aggregated portfolio views

Revision-wise DSM / DSN charge impact analysis

Together, these demonstrate operational readiness for:

Scheduling discipline

Aggregation of generation

Settlement and deviation analysis

What This Demo Intentionally Does Not Show

To maintain clarity and security, the following are out of scope:

No live APIs or system integrations

No real plant names, capacities, or locations

No grid operations, SLDC, or DISCOM interfaces

No billing or commercial transactions

No exposure of internal or VPN-restricted systems

All data and visuals used are masked or synthetic.

How the System Works (Conceptually)

At a high level, the analytics flow follows a modular design:

Satellite weather data is ingested and transformed through feature engineering pipelines.
Machine learning models convert these features into power predictions.
Each new weather update automatically triggers a new forecast revision, which is stored and versioned.
Actual generation data is then aligned at the same time-block granularity.
Deviation and DSM/DSN charge exposure are computed for each revision.
All outputs are presented through a read-only dashboard layer.

This separation ensures the system is extensible and future-ready.

Machine Learning–Based Power Prediction

Power prediction is performed using machine learning regression models trained on historical weather and generation data.

Key characteristics include:

Non-linear mapping between weather variables and power output

Plant-specific calibration

Robust handling of intraday variability

The models are:

Data-driven

Retrainable

Extensible to new features or assets

Automated Intraday Forecast Revisions

A core strength of the system is its ability to automatically generate multiple forecast revisions throughout the day.

Each revision:

Is timestamped and versioned

Reflects the best available forecast at that moment

Can be independently compared against actual generation

This mirrors real-world scheduling and gate-closure dynamics and allows clear visibility into how forecast accuracy improves closer to delivery.

Forecast vs Actual and Deviation Analytics

Actual generation is aligned to the same 15-minute or hourly blocks as forecasts. This enables:

Clean forecast vs actual comparison

Revision-wise error analysis

Transparent, auditable performance tracking

On top of this, the system computes deviation volumes and DSM / DSN charge exposure for each revision using configurable logic. This allows stakeholders to:

See how deviation risk reduces with better revisions

Understand the financial impact of forecast accuracy

Quantify the operational value of intraday updates

Aggregation Readiness

Although currently demonstrated at plant level, the design is aggregation-ready:

Forecasts can be rolled up across multiple assets

Deviations and charges can be computed at portfolio level

The data model supports future Virtual Power Plant (VPP) or aggregator use cases

This makes the platform extensible beyond individual sites.

Alignment with India Energy Stack (IES)

While no external APIs are exposed in this demo, the platform aligns closely with IES principles:

Time-block discipline through high-frequency forecasting

Intraday revision tracking

Settlement-grade analytics

Auditability and transparency

Aggregation capability

In essence, this work represents the analytics layer that would feed future IES-aligned APIs as regulatory and commercial frameworks evolve.

Repository Contents

This repository contains:

A short dashboard walkthrough video

Example data schemas (structure only, no real values)


Intended Use

Internal strategy and architecture discussions

IES and transactive energy conversations

Technology and capability demonstration

Disclaimer

All data, visuals, and examples in this repository are synthetic or masked and shared solely for demonstration purposes.
This repository demonstrates capability, not production deployment.

Closing Note

This in-house power prediction dashboard demonstrates that the forecasting and analytics foundation required for IES participation already exists. By combining satellite weather data, machine learning models, automated revisions, and deviation charge analytics, the system supports operational excellence today and positions the platform for IES-aligned participation in the future.

Link of Video of power prediction dashboard demonstrates that the forecasting
https://github.com/user-attachments/assets/c75243d2-8760-46e7-b890-b68b5ccf6ef1


Link of Video of power prediction dashboard DSM analytics
https://github.com/user-attachments/assets/d54850a8-7b4a-44df-b549-c446ed5dc0cc




