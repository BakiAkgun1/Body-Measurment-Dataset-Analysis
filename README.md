# Body Measurements Dataset Analysis
The Body Measurements Dataset offers a range of body measurement data for individuals, including key anthropometric dimensions and demographic details. This dataset is ideal for performing statistical analyses to explore relationships between different body measurements and demographic factors. The primary goal of this analysis is to understand how these measurements interrelate and vary across different groups.

## Dataset

The dataset includes various body measurements and is used for statistical tests and correlation analyses. The dataset is sourced from [Kaggle Body Measurements Dataset](https://www.kaggle.com/datasets/saurabhshahane/body-measurements-dataset).

## Dataset Columns
- **Height**: Height (cm)
- **Weight**: Weight (kg)
- **Neck**: Neck circumference (cm)
- **Chest**: Chest circumference (cm)
- **Abdomen**: Abdomen circumference (cm)
- **Gender**: Gender (Male/Female)
- **Age**: Age (years)

## Tests and Results

### Normality Tests
Normality tests evaluate whether the data follows a normal distribution.

- **Shapiro-Wilk Test:**
  - `TotalHeight` - Statistic: 0.769, p-value: 1.517e-30

- **D'Agostino's K^2 Test:**
  - Statistic: 18.059, p-value: 0.00012

- **Anderson-Darling Test:**
  - `TotalHeight` - Statistic: 3.390, Critical Values: [0.573, 0.652, 0.783, 0.913, 1.086]
  - `LegLength` - Statistic: 7.607, Critical Values: [0.573, 0.652, 0.783, 0.913, 1.086]
  - `ShoulderWidth` - Statistic: 9.623, Critical Values: [0.573, 0.652, 0.783, 0.913, 1.086]

### Non-Parametric Tests
Non-parametric tests are used when data does not meet parametric test assumptions.

- **Mann-Whitney U Test (Gender vs. TotalHeight):**
  - p-value: 0.0858

- **Kruskal-Wallis Test (Age vs. TotalHeight):**
  - p-value: 5.514e-19

- **Friedman Test (TotalLength, ShoulderWidth, LegLength):**
  - p-value: 8.983e-296

### Correlation Tests
Correlation tests measure the strength and direction of relationships between variables.

- **Pearson Correlation Test (LegLength vs. TotalHeight):**
  - Correlation Coefficient: 0.662, p-value: 1.491e-91

- **Spearman Rank Correlation Test:**
  - Correlation Coefficient: 0.595, p-value: 6.519e-70

- **Kendall Tau Correlation Test:**
  - Correlation Coefficient: 0.458, p-value: 2.386e-68

## Visualizations

- **Heatmap:** Visualizes relationships between `TotalHeight`, `LegLength`, and `ShoulderWidth`.
- **Age Distribution:** Histogram showing the distribution of the `Age` variable.
- **Gender Distribution:** Countplot illustrating the distribution of `Gender`.

![download](https://github.com/user-attachments/assets/7bb3ab41-973d-4f33-973a-0389eee6b26e)
![download](https://github.com/user-attachments/assets/a886b2f3-27aa-4f25-81aa-40318b1ef26e)
![download](https://github.com/user-attachments/assets/2b68866e-b61c-4d45-a30b-42749543d16d)
![download](https://github.com/user-attachments/assets/97bf29ed-4e24-43ad-872e-0830307eb303)


## Libraries Used
- `pandas` - Data manipulation
- `scipy.stats` - Statistical tests
- `seaborn` - Data visualization
- `matplotlib` - Data visualization

## Results and Interpretation
- **Normality Tests:** The data for most variables does not follow a normal distribution, which is why non-parametric tests were preferred.
- **Non-Parametric Tests:** Mann-Whitney U, Kruskal-Wallis, and Friedman tests are effective when normal distribution assumptions are not met and were used to analyze relationships between different variables.
- **Correlation Tests:** Pearson, Spearman, and Kendall Tau tests reveal strong relationships and correlations between variables.
 
