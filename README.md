# OCR Futures Data Processor and Trading Algorithm

This repository contains a comprehensive set of tools for analyzing financial market data, identifying patterns, and automating trading strategies. The project combines Python scripts for data analysis and visualization with integration into NinjaTrader for trading automation. 

---

## Repository Overview

```
OCR-Futures-Data-Processor-and-Trading-Algorithm/
├── Python_Scripts/
│   ├── 1.py                    # Utility script for general functions.
│   ├── Screen_rec_final.py     # Captures live screen recording for trading data analysis.
│   ├── ORDER_SCAN_FOOTPRINT_ES.py # Analyzes order flow and footprint charts to detect trading patterns.
├── NinjaTrader/
│   └── OCRPLUS.cs              # Custom NinjaTrader strategy written in C#.
├── Config/
│   └── config.json             # Configuration file for various script settings.
├── Data/
│   └── candle_data.xlsx        # Example data for analysis and testing.
├── README.md                   # Documentation about the project.
└── requirements.txt            # List of Python dependencies.
```

---

## Features and Tools

### Python Scripts

#### **1.py**
This script contains utility functions that are used across the project. These include:
- Data transformation and preprocessing.
- Helper functions for handling configurations and logging.

#### **Screen_rec_final.py**
- Captures live trading screens for analysis.
- Integrates with `pytesseract` for OCR to extract text from screen data.
- Processes extracted data to generate actionable trading insights.

#### **ORDER_SCAN_FOOTPRINT_ES.py**
- Analyzes order flow and footprint data to identify patterns such as buying/selling imbalances.
- Implements logic for detecting divergences and other market patterns.
- Outputs trading signals based on defined strategies.

### NinjaTrader Strategy

#### **OCRPLUS.cs**
- A NinjaTrader strategy written in C#.
- Processes order flow data for automated trade execution.
- Configurable settings for thresholds, stop-loss, and take-profit levels.
- Designed for seamless integration with NinjaTrader 8.

### Configurations

#### **config.json**
- Stores configuration parameters such as:
  - Default screen dimensions for `Screen_rec_final.py`.
  - Threshold values for divergence detection.
  - Connection settings for external APIs or databases.

### Data

#### **candle_data.xlsx**
- Sample market data provided for testing and validation of scripts.
- Includes historical OHLC data and delta values.

---

## Setup

### Prerequisites

1. **Install Python 3.8 or higher**:
   - Ensure Python is installed and added to the system path.

2. **Install Required Python Libraries**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Install Tesseract-OCR**:
   - Download and install Tesseract from [https://github.com/tesseract-ocr/tesseract](https://github.com/tesseract-ocr/tesseract).
   - Configure the `tesseract_cmd` path in the scripts if necessary.

4. **NinjaTrader**:
   - Install NinjaTrader 8.
   - Import `OCRPLUS.cs` as a custom strategy.

---

## Usage

### Python Scripts

1. **Screen Recording**:
   - Run `Screen_rec_final.py` to start capturing and processing live trading screens.
   - Ensure Tesseract-OCR is properly configured to extract text data from the screen.

2. **Order Scanning**:
   - Execute `ORDER_SCAN_FOOTPRINT_ES.py` to analyze order flow and footprint data.
   - Customize parameters such as delta thresholds and timeframes within the script.

### NinjaTrader Strategy

1. Open NinjaTrader and import `OCRPLUS.cs` as a strategy.
2. Configure strategy settings and attach it to a trading chart.
3. Enable the strategy for automated trading based on predefined rules.

---

## Features

1. **Pattern Recognition**:
   - Detects divergence patterns in market data.
   - Identifies key buying and selling imbalances.

2. **Live Screen Analysis**:
   - Processes live trading screens to extract actionable insights.
   - Uses OCR technology for real-time data extraction.

3. **Trading Automation**:
   - Automated strategy execution using NinjaTrader.
   - Customizable parameters for adapting to different market conditions.

4. **Data Analysis**:
   - Tools for processing and visualizing market data.
   - Includes sample data for testing and debugging.

---

## Contributing

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Submit a pull request with a detailed description of your changes.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---
