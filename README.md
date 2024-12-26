# Optimizing-Facebook-Bidding-Ads-using-A-B-Testing

## Overview
This project analyzes Facebook advertising data to compare the effectiveness of "average bidding" versus "maximum bidding" strategies through A/B testing. The analysis focuses on key metrics including impressions, clicks, purchases, and earnings to determine the most efficient bidding approach.

## Repository Structure
```
├── README.md
├── Optimizing Facebook's Ad Bidding.ipynb
└── data/
    ├── control_group.csv      # Maximum bidding data
    └── test_group.csv         # Average bidding data
```

## Technical Skills & Tools Used

### Required Libraries
```python
# Data manipulation and analysis
import pandas as pd
import numpy as np
from scipy import stats
from datetime import datetime, timedelta
import random

# Visualization
import matplotlib.pyplot as plt
from plotly.subplots import make_subplots
from plotly.offline import iplot, init_notebook_mode, plot
import seaborn as sns
```

### Data Analysis Methods
1. **A/B Testing**
   - Hypothesis formulation
   - Statistical significance testing at 5% level
   - Performance metrics comparison

2. **Statistical Analysis**
   - Descriptive statistics (mean, median, standard deviation)
   - Distribution analysis
   - Comparative analysis between control and test groups

3. **Performance Metrics**
   - Click-Through-Rate (CTR)
   - Conversion Rate
   - Return on Investment (ROI)

### Hypothesis Testing Framework
All statistical tests conducted at 5% significance level for:
- Click-Through-Rate Analysis
  - H₀: Mean CTR for Control group ≤ Test Group
  - Hₐ: Mean CTR for Control group > Test Group

- Conversion Rate Analysis
  - H₀: Mean Conversion Rate for Control group ≥ Test Group
  - Hₐ: Mean Conversion Rate for Control group < Test Group

- Return on Investment Analysis
  - H₀: Mean ROI for Control group ≥ Test Group
  - Hₐ: Mean ROI for Control group < Test Group

- Purchase Analysis
  - H₀: No difference in mean Purchase between groups
  - Hₐ: Difference exists in mean Purchase between groups

- Earnings Analysis
  - H₀: No difference in mean Earnings between groups
  - Hₐ: Difference exists in mean Earnings between groups

- Click Analysis
  - H₀: No difference in mean Clicks between groups
  - Hₐ: Difference exists in mean Clicks between groups

## Project Implementation

### Data Loading
```python
# Load the datasets
control_df = pd.read_csv("data/control_group.csv")    # Maximum bidding group
test_df = pd.read_csv("data/test_group.csv")         # Average bidding group
```

### Analysis Process
1. **Data Preprocessing**
   - Data cleaning
   - Missing value handling
   - Data type verification
   - Feature preparation

2. **Exploratory Analysis**
   - Descriptive statistics
   - Distribution analysis
   - Performance metric comparisons

3. **Statistical Testing**
   - Hypothesis testing for multiple metrics
   - Significance evaluation at 5% level

4. **Visualization**
   - Performance metric plots
   - Statistical comparisons
   - Comparative analysis charts

## Getting Started

### Prerequisites
```bash
pip install pandas numpy scipy matplotlib seaborn plotly jupyter
```

### Project Setup
1. Clone this repository
2. Create a data folder in your project directory
3. Place control_group.csv and test_group.csv in the data folder
4. Install required dependencies
5. Open and run the Jupyter notebook


## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contact
For questions or feedback about this analysis, please open an issue in the repository.
