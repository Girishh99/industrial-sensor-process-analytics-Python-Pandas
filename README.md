# Industrial Sensor Monitoring & Process Analytics

## Project Overview

This project analyzes industrial manufacturing sensor data to understand how process conditions influence production quality. The challenge was aligning high-frequency sensor readings with lower-frequency quality measurements to create a unified dataset for analysis.

## Business Problem

Manufacturing environments generate thousands of sensor readings every day, while product quality is often measured at hourly or batch intervals. This mismatch makes it difficult to identify process conditions that impact quality.

**Objective:** Identify sensor patterns and operational conditions that affect production quality.

## Dataset

### Sensor Data (`data_X`)

* Time-series industrial sensor readings
* Chamber measurements
* Process parameters
* Recorded at high frequency (minute-level)

### Quality Data (`data_Y`)

* Timestamp (`date_time`)
* Production quality target (`quality`)
* Recorded at lower frequency (hourly/batch level)

## Data Engineering & Processing

### Challenge

Sensor and quality timestamps were not perfectly aligned.

### Solution

Implemented a time-window aggregation approach:

1. Converted timestamps to datetime format
2. Sorted datasets chronologically
3. Set datetime as index
4. Resampled sensor readings into hourly averages
5. Merged datasets using `merge_asof()`
6. Created a unified analytical dataset

## Exploratory Data Analysis (EDA)

* Data quality assessment
* Missing value analysis
* Statistical summaries
* Sensor behavior exploration
* Time-series trend analysis
* Feature relationship investigation

## Key Techniques

* Time-Series Analysis
* Data Alignment
* Time Window Aggregation
* Resampling
* Industrial Process Analytics
* Data Preprocessing
* Exploratory Data Analysis (EDA)

## Tech Stack

* Python
* Pandas
* NumPy
* Jupyter Notebook

## Project Workflow

```text
Raw Sensor Data
       ↓
Datetime Conversion
       ↓
Sorting & Indexing
       ↓
Hourly Resampling
       ↓
merge_asof()
       ↓
Final Analytical Dataset
       ↓
EDA & Insights
```

## Key Learning Outcomes

* Handling real-world industrial time-series data
* Aligning datasets with different recording frequencies
* Building scalable preprocessing pipelines
* Extracting insights from manufacturing process data

---
