# Quantitative-Market-Risk-Natixis-Stocks
Implementation of Non-Parametric VaR (Kernel), EVT (Pickands), Bouchaud’s Price Impact Model, and Haar Wavelets analysis on excel/vba without external packages

### 1. Non-Parametric VaR & Expected Shortfall
- **Methodology:** Implementation of a **Historical VaR** using a **Biweight Kernel Density Estimator** (smoothing via Silverman's rule bandwidth).
- **Risk Measure:** Calculation of **Expected Shortfall (ES)** to capture tail risk beyond the confidence threshold.
- **Backtesting:** Validation of the model on out-of-sample data (Natixis stock), analyzing volatility regime shifts between calibration (2015-2016) and testing periods (2017-2018).

### 2. Extreme Value Theory (EVT)
- **Approach:** Block Maxima method applied to daily returns.
- **Estimation:** Calibration of the **Generalized Extreme Value (GEV)** distribution using the **Pickands Estimator**.
- **Analysis:** Determination of the tail index ($\xi$) to classify distributions (Weibull vs. Fréchet domains) for both gains and losses.

### 3. Market Microstructure: Price Impact
- **Model:** Calibration of **Bouchaud’s Price Impact Model** to analyze how trades affect prices.
- **Regression:** Estimation of the transient impact function (Propagator $G(l)$) by regressing price changes on lagged order signs.
- **Results:** Confirmation of the decay of price impact over time.

### 4. Multiresolution Analysis & Fractals
- **Haar Wavelets:** Decomposition of FX rates (GBPEUR, SEKEUR, CADEUR) to analyze correlation across different time scales.
- **Epps Effect:** Observation of increasing correlation as the time scale grows.
- **Hurst Exponent:** Calculation of the Hurst exponent via scaling of moments to estimate long-memory processes and annualized volatility ($\sigma_{annual} = \sigma \times 252^H$).
