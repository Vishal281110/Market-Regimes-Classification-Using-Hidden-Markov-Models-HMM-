# Market Regimes Classification Using Hidden Markov Models (HMM)

Classifying hidden market regimes (bullish, bearish, volatile) using Hidden Markov Models on financial time-series data to enable adaptive trading strategies and improved risk management.


## Overview

Financial markets often move through different regimes such as bullish, bearish, volatile, or sideways phases. Identifying these regimes is crucial for building adaptive trading strategies and effective risk management. However, market regimes are not directly observable and can change dynamically over time.

This project addresses the problem by using Hidden Markov Models (HMM) to classify hidden market states based on historical stock time-series data, such as returns and volatility. HMM treats market behavior as a probabilistic state machine where the underlying regimes are hidden, and the observed financial metrics serve as emissions.

By training unsupervised HMMs, the project:

1. Detects hidden regimes without prior labeling

2. Visualizes regime transitions and probabilities

3. Backtests regime-specific trading strategies

4. Predicts future regime probabilities using Viterbi decoding and filtering

The outcome is a framework that can help traders, analysts, and researchers gain deeper insights into market dynamics and build data-driven, regime-aware strategies.




## Project Structure
     data/ – Raw and processed INDIA VIX OHLCV data

     notebooks/ – Exploratory analysis and development notebooks

     src/ – Core Python modules: 
            hmm_model.py – Custom HMM implementation
	    feature_engineering.py – Feature extraction and preprocessing
            visualization.py – Plotting and graphical output functions
	    validation.py – Market event correlation validation functions
            persistence.py – Regime persistence analysis utilities
  
     results/ – Generated plots and reports

     requirements.txt – Python dependencies
     README.md – Project documentation


## Methodology
	1.	Data Loading & Preprocessing: OHLCV data → feature computation (returns, volatility,    range).
	2.	HMM Training: Log-domain forward-backward algorithms with Baum-Welch parameter updates.
	3.	Regime Decoding: Viterbi algorithm for most likely regime sequences.
	4.	Validation: Chi-square test for event correlation.
	5.	Persistence Analysis: Duration, consistency, and stability index metrics.
	6.	Visualization & Anomaly Detection: Regime-colored price charts with uncertainty flags.

## Tech Stack
	•	Programming Language: Python 3.12
	•	Core Libraries: NumPy, pandas, matplotlib, seaborn, scipy
	•	Statistical Modeling: Custom Hidden Markov Model implementation
	•	Visualization: Matplotlib, Seaborn
## Features
1. Regime Anomaly Detection:
Regime Anomaly Detection is a technique used to flag unusual behavior in the market by identifying time periods where the model has low confidence in its regime classification. In our HMM-based market analysis, this adds a powerful layer for tracking uncertainty and potential instability in market structure.

2. Market Event Correlation Validator:
The Market Event Correlation Validator serves as a crucial validation mechanism that quantifies the statistical relationship between identified regimes and significant market events. This validator addresses a fundamental challenge in regime identification: determining whether the detected regimes actually correspond to meaningful market conditions rather than spurious statistical patterns.

3. Regime Persistence Analysis:
Market regimes often exhibit persistence, meaning once the market enters a regime (e.g., bull, bear, high-volatility), it tends to remain in that regime for some duration. Regime persistence analysis quantifies how long regimes last, how consistent their durations are, and how stable they are relative to transition dynamics.

## Results
        • Successfully detected 3 distinct market regimes correlated with historical VIX spikes.
	• Statistical validation confirmed significant correlation between detected regimes and extreme market events (p < 0.05).
	• Persistence analysis revealed stability patterns, aiding regime-based strategy design.
 


## Team Information

Team Leader:
Name: Mayank Bisaria  
Roll No.: 240008018    
Discord: mayankbisaria

Member:
Name: Keshvi Lakhotia  
Roll No.: 240008015    
Discord: keshvi 12   

Member:
Name: Garvit Mathur   
Roll No.: 240008012   
Discord: garvit5518   

Member:
Name: Vishal Shakya   
Roll No.: 240008037   
Discord: utkarsh000   

Member:
Name: Pritish Dutta   
Roll No.: 240021012   
Discord: pritish1742   

Member:
Name: Samarth Dhanuka   
Roll No.: 240008011   
Discord: the-samarth   


 

## License

## References
