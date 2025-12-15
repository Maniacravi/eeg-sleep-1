# EEG Sleep Analysis

![Python Version](https://img.shields.io/badge/python-3.11%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## 📖 Overview

**EEG Sleep Analysis** is a specialized toolkit designed for the processing, exploration, and visualization of EEG (Electroencephalogram) sleep data. This project provides a robust pipeline for handling complex physiological signals, enabling researchers and engineers to analyze sleep micro-architecture such as Sleep Spindles, K-Complexes, REM cycles, and other sleep-related events.

The core objective of this project is to streamline the transition from raw EEG signal data (MAT files) and event annotations (CSV) into actionable insights and structured epochs ready for machine learning applications or clinical review.

## ✨ Key Features

*   **Data Ingestion**: Seamlessly load raw EEG data from `.mat` files and corresponding annotations from `.csv` files.
*   **Signal Processing**: 
    *   Automated creation of MNE `Raw` objects with proper channel information.
    *   Support for standard sleep event markers: Spindles (S), K-Complexes (K), REM, Sleep Onset (Son), Sleep Offset (Soff), Arousals (A), and Microsleep (MS).
    *   Custom epoching logic to extract specific time windows around events.
*   **Visualization**: Dedicated plotting utilities to visualize raw EEG traces along with event markers, enabling qualitative assessment of signal quality and event timing.
*   **Data Conversion**: Helper functions for time-domain conversions (samples to minutes) to facilitate interpretation.

## 🛠️ Technology Stack

This project leverages a modern Python scientific stack:

*   **[MNE-Python](https://mne.tools/)**: For exploring, visualizing, and analyzing human neurophysiological data.
*   **[NumPy](https://numpy.org/) & [Pandas](https://pandas.pydata.org/)**: For high-performance numerical computing and data manipulation.
*   **[SciPy](https://scipy.org/)**: For loading MATLAB files and advanced scientific computing.
*   **[Matplotlib](https://matplotlib.org/)**: For creating static, animated, and interactive visualizations.
*   **[PyTorch](https://pytorch.org/)**: Included for potential future deep learning modeling on the processed data.

## 🚀 Getting Started

### Prerequisites

*   Python 3.11 or higher
*   [uv](https://github.com/astral-sh/uv) (recommended) or pip

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/eeg-sleep-1.git
    cd eeg-sleep-1
    ```

2.  **Install dependencies:**

    Using `uv` (fastest):
    ```bash
    uv sync
    ```

    Using `pip`:
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: If `requirements.txt` is not present, you can install from `pyproject.toml` or manually install the dependencies listed in the Tech Stack section).*

## 📂 Project Structure

```text
eeg-sleep-1/
├── data/               # Directory for storing raw and processed data
│   └── raw/            # Place your .mat and .csv files here
├── notebooks/          # Jupyter notebooks for exploration and analysis
│   └── 01_data_exploration.ipynb
├── src/                # Source code for the project
│   └── utils.py        # Core utility functions for loading and processing EEG data
├── main.py             # Entry point for the application
├── pyproject.toml      # Project configuration and dependencies
└── uv.lock             # Lock file for dependencies
```

## 💻 Usage

To get started with the data exploration, launch the Jupyter Notebook:

```bash
jupyter notebook notebooks/01_data_exploration.ipynb
```

This notebook demonstrates the standard workflow:
1.  Importing required modules.
2.  Loading subject data (`load_eeg` and `load_labels`).
3.  Visualizing signal properties and event distributions.
4.  Epoching data based on specific sleep markers (e.g., REM).

## 📊 Sample Visualizations

*The toolkit includes functions like `plot_eeg` to visualize the EEG signal overlayed with event markers, providing a clear view of the temporal relationship between physiological signals and annotated sleep events.*

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---
*This project is part of a professional portfolio demonstrating skills in biomedical signal processing and Python software engineering.*
