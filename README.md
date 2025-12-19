# Asymmetric Flare Decomposition

This repository contains algorithms for detecting and decomposing solar flares using asymmetric models from GOES X-ray satellite data.

## Overview

The project implements an automated pipeline for:
- Detecting significant peaks in solar flare time series
- Fitting asymmetric flare profiles using global optimization (differential evolution)
- Decomposing complex flares into multiple components
- Calculating quality metrics, energy estimates, and flare classifications

## Files

- `flare_detection algorithme.ipynb`: Main Jupyter notebook containing the complete flare detection and analysis algorithm

## Requirements

- Python 3.7+
- numpy
- scipy
- pandas
- matplotlib
- joblib
- pybaselines

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/pretamdas007/Asymmetric_Flare_Decompition.git
   cd Asymmetric_Flare_Decompition
   ```

2. Install dependencies:
   ```bash
   pip install numpy scipy pandas matplotlib joblib pybaselines
   ```

## Usage

1. Open `flare_detection algorithme.ipynb` in Jupyter Notebook or JupyterLab
2. Ensure you have GOES X-ray data in the appropriate format
3. Run the cells sequentially to process the data and detect flares
4. Results include fitted parameters, flare classifications, and energy estimates

## Algorithm Details

The algorithm uses:
- Peak detection with configurable prominence and distance thresholds
- Asymmetric flare model: `A * exp(-(t-t0)^2/(2*sigma_r^2)) * exp(-(t-t0)/tau_d)` for t > t0
- Global optimization with differential evolution for robust fitting
- Quality assessment using R², AIC, and BIC metrics

## Contributing

Contributions are welcome! Please open issues or submit pull requests.

## License

This project is open source. Please check the license file for details.