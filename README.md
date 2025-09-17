# Master's Thesis: Fragility Index for Ethereum's Open-Source Ecosystem (in progress)

A special thank you to Trevor Jacka from Builder.love for providing the data used in this thesis

## Overview
This project develops a **fragility index** to measure systemic risk in the Ethereum open-source ecosystem, treating protocol repositories as a networked system.  
The index integrates multiple dimensions of developer concentration, automation balance, and core structure, and tests whether these structural patterns anticipate stress events such as liquidity crunches, price drawdowns, or repository abandonment.

## Objectives
- Construct a fragility index that captures systemic vulnerabilities in Ethereum’s developer ecosystem.  
- Quantify risks such as contributor concentration, over-reliance on automation, and small core developer groups.  
- Incorporate commit-level NLP features to detect signals of organizational or financial stress.  
- Evaluate whether these metrics correlate with adverse market and ecosystem outcomes.  

## Methodology
1. **Data Collection**  
   - Extracted contributor and commit data from Ethereum-related GitHub repositories using the Builder.love data warehouse (contains over 900 million commits and 1 million repos)
   - Augmented with financial/market data for ETH and comparable financial software projects.  

2. **Fragility Index Construction**  
   - Features:  
     - *Human concentration*: top-contributor shares, Herfindahl indices, bus factor.  
     - *Automation balance*: bot share, bot concentration, human-to-bot ratios.  
     - *Core size*: relative distribution of contributors in central vs peripheral roles.  
   - Processing:  
     - Robust scaling with median and interquartile range transformations.  
     - Clipping extreme values for stability.  
     - Mapping to bounded monotone scores.  
   - Aggregation: weighted geometric mean, with higher weight on concentration risk.  
   - Uncertainty: bootstrap resampling of contributor rows.  

3. **NLP & Machine Learning**  
   - Commit text analysis using NLP feature extraction.  
   - Predictive modeling with tree-based and neural architectures to test predictive validity.  

4. **Evaluation**  
   - Benchmarked fragility index against ETH price drawdowns, liquidity crunches, and repository abandonment.  
   - Comparative analysis with adjacent financial software ecosystems.  

## Tools & Libraries
- **Python**: pandas, NumPy, scikit-learn, PyTorch  
- **NLP**: HuggingFace Transformers, TF-IDF vectorizers  
- **Network Analysis**: NetworkX, igraph  
- **Statistical Methods**: bootstrap resampling, robust scaling  

## Expected Contributions
- A novel **fragility index** framework adaptable to crypto ecosystems and financial open-source projects.  
- Evidence on whether developer concentration and commit dynamics can serve as early warning signals of systemic stress.  
- Foundation for future research on systemic risk at the intersection of open-source development and financial markets.  

## Author
**Arsh Misra**  
M.A. Quantitative Methods in the Social Sciences, Columbia University  
Thesis Advisor: [Insert Advisor Name]  
