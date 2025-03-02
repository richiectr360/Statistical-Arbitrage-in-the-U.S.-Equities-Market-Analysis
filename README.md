# Statistical Arbitrage: Pairs Trading in U.S. Equities

## Paper Overview
The paper *"Statistical Arbitrage in the U.S. Equities Market"* by Marco Avellaneda and Jeong-Hyun Lee explores a systematic approach to **pairs trading**, where two correlated stocks are traded based on their spread deviations. The strategy is rooted in mean-reversion and statistical techniques to identify and capitalize on temporary price divergences.

### Key Concepts from the Paper:
1. **Pair Selection**: Stocks are chosen based on their historical price relationship using a distance-based or cointegration approach.
2. **Mean-Reverting Spread**: The spread (price difference between two stocks) follows a mean-reverting process modeled by an Ornstein-Uhlenbeck (OU) equation.
3. **Trading Strategy**:
   - A position is entered when the spread deviates significantly from its mean.
   - Positions are closed once the spread reverts to the mean.
4. **Risk Management**: The strategy ensures market neutrality to reduce exposure to systematic risks.

## Project Overview
This project implements a **statistical arbitrage strategy** based on **pairs trading** in the U.S. equities market, inspired by the above paper. The methodology relies on identifying stock pairs exhibiting mean-reverting behavior and constructing a trading signal based on spread movements.

## Methodology
1. **Pair Selection**: Stocks are chosen based on their historical price relationship using a distance-based approach.
2. **Mean Reversion Analysis**: The spread between selected pairs is tested for mean-reverting properties using:
   - Augmented Dickey-Fuller (ADF) test
   - Half-life of mean reversion estimation
3. **Trading Strategy**:
   - Open long/short positions when the spread deviates significantly from the mean.
   - Close positions when the spread reverts.
4. **Performance Evaluation**:
   - Profitability metrics are computed.
   - Risk-adjusted returns are analyzed.
   - Strategy robustness is assessed.

## Key Findings
- The model successfully identifies **mean-reverting stock pairs** based on statistical criteria.
- Estimated parameters:
  - **Kappa (speed of mean reversion):** 1.76
  - **Equilibrium standard deviation:** 0.44
  - **Long-term mean:** 1.19
  - **Initial deviation:** -0.31
  - **Lookback period:** 300 trading days
- The strategy generates **visual representations of spreads**, indicating potential trading signals.
- Some numerical warnings suggest possible issues with log or square root computations, indicating areas for refinement.

## Future Enhancements
- Improve parameter tuning for robustness.
- Account for transaction costs and execution slippage.
- Test alternative pair selection techniques, such as cointegration.
- Implement machine learning for spread prediction.

## Dependencies
- Python (NumPy, pandas, Matplotlib, statsmodels, sklearn)

## How to Run
1. Load historical price data for selected stocks.
2. Run the Jupyter Notebook to compute spread signals and execute the trading strategy.
3. Evaluate results based on visualizations and numerical outputs.

## Author
Richie Singh
