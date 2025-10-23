# Fixed Income Structured Note Case Study

This repository packages a structured note case study.  The Jupyter notebooks value a capped/floored floating note, stress-tests the curve, and explores hedging with an interest rate swap.

## Highlights
- Builds a EURIBOR discount curve from the market data.
- Prices a capped/floored floating-rate note and reports discounted cash flows.
- Measures DV01 across level, slope, and curvature curve moves.
- Illustrates how to hedge the note with a vanilla swap and tests the hedge under different shocks.

## Repository Layout
- `notebooks/`
  - `fixed_income_showcase.ipynb` – primary storytelling notebook for recruiters.
  - `structured_note_hedging.ipynb` – detailed supporting analysis and stress testing.
  - `risk_factor_analysis.ipynb` – additional questions, credit spread stress, and VaR exploration.
- `data/`
  - `FI.xlsm` – historical EURIBOR fixings, discount factors, and cash-flow inputs.
  - `market_data.xlsx` – supplemental data used in the extended analysis notebook.
- `archive/graphs.mlx` – original MATLAB Live Script reference.
- `requirements.txt` – Python dependencies for the notebooks.

## Getting Started
1. Create and activate a virtual environment (optional but recommended).
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```
2. Install the dependencies. QuantLib can take a moment to build.
   ```bash
   pip install -r requirements.txt
   ```
3. Launch Jupyter Lab/Notebook and open `notebooks/fixed_income_showcase.ipynb`.
   ```bash
   jupyter lab
   ```

QuantLib wheels are published for the main Python versions on macOS, Linux, and Windows. If the installation fails, consult the [QuantLib Python documentation](https://quantlib-python-docs.readthedocs.io/en/latest/installation.html).

## Data Notes
- The Excel workbooks are included because the analysis relies on specific historical fixings and curve quotes and the bootstrap of the discont factors.

