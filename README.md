--
# Interpretability Plots for ML Algorithms

This repository contains code and notebooks for Assignment #6 of the **AIPI 590 - Explainable AI (XAI)** course. The assignment focuses on generating **PDP (Partial Dependence Plots)**, **ICE (Individual Conditional Expectation)**, and **ALE (Accumulated Local Effects)** plots using machine learning models to interpret feature importance and behavior, particularly in the context of phishing website detection using the UCI Phishing Websites Dataset.

## Contents

The repository is structured as follows:

```bash
Interpretability_Plots/
├── notebooks/
│   └── interpretable_plots.ipynb    # Main notebook for PDP, ICE, and ALE plot generation
├── README.md                        # This file
├── requirements.txt                 # Python dependencies and required libraries
```

### Notebooks

- **interpretable_plots.ipynb**: Contains all the code to:
  - Load and preprocess the UCI Phishing Websites dataset.
  - Train a RandomForest model.
  - Generate various interpretability plots (PDP, ICE, and ALE).
  - Perform exploratory data analysis (EDA) and feature importance analysis.

## Getting Started

### Prerequisites

To run the code in this repository, you will need to install the required Python packages. You can do so by running:

```bash
pip install -r requirements.txt
```

### Dataset

The dataset used for this assignment is the [UCI Phishing Websites Dataset](https://archive.ics.uci.edu/dataset/327/phishing+websites), which contains features that help distinguish between phishing and legitimate websites.

### Running the Notebook

1. Clone the repository to your local machine or run the notebook in Google Colab.
2. Open the `interpretable_plots.ipynb` notebook.
3. Follow the steps in the notebook to run the EDA, train the model, and generate the PDP, ICE, and ALE plots.

### Key Features

- **Partial Dependence Plots (PDP)**: Used to show the average effect of a feature on the predicted outcome, while marginalizing over other features.
- **Individual Conditional Expectation (ICE) Plots**: Show how predictions change for individual instances as a particular feature varies.
- **Accumulated Local Effects (ALE) Plots**: Provide a localized, more accurate representation of feature importance and relationships when features are correlated.

### Results

- The RandomForest model trained on the phishing dataset achieves high accuracy (97%) in distinguishing phishing websites from legitimate ones.
- **PDPs** and **ALEs** reveal that features like `sslfinal_state`, `url_of_anchor`, and `web_traffic` play crucial roles in the model’s decisions.

## References

- UCI Phishing Websites Dataset: [Link](https://archive.ics.uci.edu/dataset/327/phishing+websites)
- ALEPython Library: [GitHub](https://github.com/blent-ai/ALEPython)
- scikit-learn PDP/ICE Documentation: [PartialDependenceDisplay](https://scikit-learn.org/stable/modules/generated/sklearn.inspection.PartialDependenceDisplay.html)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.