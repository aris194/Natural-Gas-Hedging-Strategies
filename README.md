# **Volatility-Driven & Spread-Triggered Hedging Optimiser**  
*A comparative framework for ladder hedging, volatility-responsive hedging, and spread-based hedging strategies.*

This repository contains a full optimisation and analytics engine for seasonal natural-gas hedging. It allows you to:

- Build **volatility-responsive hedge paths**
- Optimise **universal hedging rules** across multiple delivery seasons
- Compare **ladder vs optimised hedge paths**
- Run a **spread-based hedging strategy** using 1–5σ trigger thresholds
- Produce full **MtM, WAP, hedge-ratio and PnL analytics**
- Export formatted **Excel workbooks** for reporting
- Generate all **plots, spaghetti charts, heatmaps and sensitivity visuals**

The project mirrors real-world hedging workflows used by trading desks, including season segmentation, rolling forward-curve processing, WAP construction, and delivery-period MtM assignment.

---

## **Included Strategies**

### **1. Baseline Ladder Hedge**
Static hedge profile defined season-by-season. Used as the baseline benchmark.

### **2. Volatility-Driven Hedging**
A dynamic hedging strategy where increments scale up or down depending on rolling volatility conditions.  
Features:
- Multi-parameter global optimiser  
- Adjustable hedge ratios  
- Penalisation for MtM volatility  
- Reward for PnL stability and hedge discipline  

### **3. Spread-Triggered Hedging**
A second optimiser framework where hedging is executed when spreads diverge from long-term equilibrium (1–5σ).  
Supports:
- Same optimisation engine  
- Same metrics and scoring approach  
- Optional season-to-next-season spread signals (W24→S25, S25→W25, etc.)

---

## **Outputs**

### **Excel Reports**
Both optimisation engines generate:
- A raw hedge output table  
- A fully formatted Excel workbook  
- Exposure, hedge volume, WAP, and MtM per reporting month  
- Clean headers, merged season labels, and correct numeric formatting  

### **Visualisations**
The notebooks produce:
- Hedge volume spaghetti charts across the optimiser grid
- Volatility vs hedge increments (dual-axis)
- Optimiser score p
