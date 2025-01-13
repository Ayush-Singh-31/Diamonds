# Diamond Price Analysis

This repository contains a Python script that elucidates intricate relationships among diamond features by leveraging advanced plotting modalities, regression evaluations, and label encoding. It merges multiple data processing steps—such as outlier expunging and dataset normalization—to ensure refined insights and facilitate robust modeling.

## Features and Workflow

1. **Data Ingestion (`readCSV`)**  
   Incorporates the dataset via `pandas.read_csv`, constructing a `DataFrame` for further manipulations.

2. **Data Formatting & Cleansing (`cleanDF` and `setFormat`)**  
   - Filters spurious observations (e.g., non-positive dimensions).  
   - Eliminates duplicates and missing entries.  
   - Casts key columns (like `carat`, `price`, etc.) into numeric types, ensuring uniform handling of numerical features.

3. **Exploratory Visualization**  
   - **Pair Plots**: Embeds high-level distributional and correlational glimpses between numeric variables (`sns.pairplot`).  
   - **Regression Plots** (`plotRegression`): Generates linear fits (e.g., `x` vs. `y`, `depth` vs. `z`) to observe potential linear alignments, highlighting the magnitude of each relationship.  
   - **Violin Plots** (`violinPlot`): Provides intricate distribution views of price segmented by categorical features such as cut, color, and clarity.

4. **Categorical Encoding (`encode`)**  
   Leverages `LabelEncoder` to transform categorical columns (`cut`, `color`, `clarity`) into numeric format, facilitating subsequent analytical or modeling processes.

5. **Correlation Matrix (`corMatrix`)**  
   Renders a heatmap of the correlation matrix to pinpoint salient interactions among all features in the dataset. Diverging colormaps illustrate both positive and negative correlations with lucid color gradients.

6. **Terminal Output (`describe`)**  
   Summarily displays dataframe dimensions, enumerates descriptive statistics, and prints data sample heads for quick verification of transformations.
