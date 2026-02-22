# Pipeline Risk Assessment: Muhlbauer Definitive Approach Baseline

This repository implements a **Quantitative Risk Assessment (QRA)** engine based on the Muhlbauer Definitive Approach (www.pipelinerisk.net). It rejects indexing and scoring in favor of physical calculations using the **Exposure-Mitigation-Resistance** triad. It can also be used to develop a fully probabilistic risk assessment (PRA)

## 🎯 The Philosophy of Conservatism
This model does not use "safety multipliers." Instead, it requires the Risk Assessor to select input values based on the intended **Confidence Level**:

1. **P99+ (Integrity Management):** Use the "High Path" (Upper bound of threats, lower bound of resistance). Appropriate for public safety and regulatory compliance.
2. **P50 (Strategic Planning/Due Diligence):** Use the "Central Tendency" (Mean/Median). Appropriate for asset valuation and M&A due diligence.

## 🏗 Mathematical Framework
### Frequency of Failure (FoF)
$$FoF = \text{Exposure} \times (1 - \text{Mitigation}) \times (1 - \text{Resistance})$$
$$TTF = {Resistance} / (Exposure \times (1-Mitigation))$$
**Time-Dependent Threats:** Modeled via a **Weibull Distribution** to determine the annual frequency of reaching a defined Limit State (Critical Wall Thickness).

### Consequence of Failure (CoF)
Calculated as the consequence potential based on the physical **Hazard Zone** that could result from a pipeline release:
$$\text{CoF (\$)} = \text{Spill } (ft^3) \times \text{Spread } (ft^2/ft^3) \times \text{Receptor } (Units/ft^2) \times \text{Product } (\$/Unit)$$

## 🚀 Getting Started
1. Open `PL_risk_Muhlbauer.ipynb` in a Jupyter environment.
2. Complete the **Conservatism Strategy Declaration**.
3. Input segment-specific data.
4. Run the engine to generate the Audit Log and Risk Profile.
