# Python Data Analysis — Learning Journey

Hey! This repo is my personal learning log where I'm picking up Python for data analysis from scratch.  
Right now it covers **Pandas** and **NumPy** — and I'll keep adding more as I go.

---

## - What's Inside

| File | Topic |
|------|-------|
| `day_01_pandas.ipynb` | Pandas Basics |
| `day_02_pandas.ipynb` | Real Dataset + Data Cleaning |
| `day_03_handson_pandas.ipynb` | Pandas Practice (Hands-on) |
| `day_04_numpy.ipynb` | NumPy Fundamentals |
| `day_05_numpy_handson.ipynb` | NumPy Practice (Hands-on) |
| `day_06_visualization.ipynb` | Data Visualization Theory (Matplotlib + Seaborn) |
| `day_07_visualization_handson.ipynb` | Data Visualization Hands-on (Real Dataset) |
| `day_08_Statistic_and_Probability.ipynb` | Statistics & Probability (Theory + Code) |
| `day_09_Statistic_and_Probability.ipynb` | Probability — Theory + Hands-on (Real Dataset) |
| `day_10_AirBnb_CaseStudy.ipynb` | Airbnb NYC — End-to-End Case Study |
| `day_11_inferential_stats.ipynb` | Inferential Statistics — Confidence Interval |
| `day_12_inferential_stats.ipynb` | Inferential Statistics — Sampling + Hypothesis Testing |
| `day_13_inferential_stats.ipynb` | Inferential Statistics — T-Tests, ANOVA, Chi-Square |
| `day_14_linear_algebra.ipynb` | Linear Algebra for ML — Vectors, Matrices, Tensors |
| `day_15_handson_linear_algebra.ipynb` | Linear Algebra — Hands-on Practice |
| `day_16_ml_linear_regression.ipynb` | Introduction to ML + Linear Regression Theory |
| `day_17_18_linear_regression.ipynb` | Linear Regression — Hands-on (Insurance Dataset) |


---

## - Day-by-Day Breakdown

### Day 1 — Pandas Basics
Got started with Pandas and learned how data is structured in it.

- Created DataFrames manually using dictionaries and lists
- Understood what a **Series** is (basically a single column)
- Added new columns to an existing DataFrame
- Used `.max()`, `.min()`, `.describe()` to get quick stats
- Learned the difference between **`loc`** (label-based) and **`iloc`** (index-based) for selecting data
- Practiced slicing rows and columns

---

### Day 2 — Real Dataset + Data Cleaning
Worked on a real-world powerlifting dataset and learned how to clean messy data.

- Loaded a CSV file using `pd.read_csv()`
- Explored data with `.head()`, `.tail()`, `.sample()`, `.info()`, `.describe()`
- Renamed columns using `.rename()`
- Handled **null values** — dropped them or filled them with mean/median/0
- Removed **duplicate rows** with `.drop_duplicates()`
- Filtered data based on conditions (single and multiple at once using `&` and `|`)

---

### Day 3 — Pandas Hands-on Practice
Put Day 1 and Day 2 knowledge to the test with practice problems.

- Converted Python lists, tuples, and sets into Pandas Series (and figured out why sets cause issues — they're unordered!)
- Practiced `.head()`, `.tail()`, and updating values at specific index positions
- Built DataFrames from dictionaries and renamed columns
- Filtered rows by conditions (e.g. age ≥ 19)
- Loaded another real dataset (`adult_data`), explored it fully, and cleaned all null + duplicate values
- Used `.shape` to check total rows and columns

---

### Day 4 — NumPy Fundamentals
Switched to NumPy and understood why it exists in the first place.

- Learned why NumPy arrays are faster and lighter than Python lists  
  *(Python lists are slow; NumPy is built on C/C++ so it uses a compiler, not an interpreter)*
- Created **0D, 1D, 2D, and 3D arrays** and checked their `.shape` and `.ndim`
- Understood NumPy's type hierarchy: `int < float < string`
- Learned **indexing** and **slicing** across 1D, 2D, and 3D arrays
- Used **`.reshape()`** to change the shape of an array
- Explored special arrays: `np.zeros()`, `np.ones()`, `np.full()`, `np.identity()`, `np.eye()`
- Generated random numbers with `np.random.randint()` and `np.random.choice()`
- Did arithmetic on arrays (`+`, `-`, `*`, `/`) — unlike lists, arrays actually calculate!
- Used `.sum()`, `.mean()`, `.median()`, `np.sort()`, and `.flatten()`

---

### Day 5 — NumPy Hands-on Practice
Solidified NumPy basics with focused exercises.

- Created int and float arrays with specific dtypes
- Built 0D, 1D, 2D, and 3D arrays and checked their shape
- Made a 2×5 zeros array and a 2×5 array filled with 5 using `np.full()`
- Generated 25 random integers between 0–100
- Created a 2×3 random matrix and reshaped it to 3×2
- Made a 3×3 matrix of all ones

---

### Day 6 — Data Visualization Theory (Matplotlib + Seaborn)
Learned the core chart types and when to use each one.

- Understood what data visualization is — turning data into graphs, charts, and plots
- **Matplotlib** (`pyplot`) as the base plotting library; **Seaborn** as its advanced wrapper built on top of it
- **Line Plot** — for continuous/time-series data (e.g. sales over a week); customized with `color`, `marker`, `linestyle`, `markersize`, `markerfacecolor`, `markeredgecolor`, and `grid()`
- Plotted **multiple lines** on one chart using `label` + `legend()`
- **Bar Plot** — for comparing categories; used `plt.bar()` for vertical and `plt.barh()` for horizontal
- **Pie Chart** — for showing proportions; used `autopct` for percentage formatting, `explode` to highlight a slice, and `shadow` for styling
- **Scatter Plot** — for checking correlation between two variables (e.g. roll number vs marks)
- **Histogram** — for frequency distribution across ranges; used `bins` to control grouping
- **Box Plot** (`sns.boxplot`) — for distribution and outlier detection; showed how anomaly values (like age=300) stick out visually
- **Violin Plot** (`sns.violinplot`) — like box plot but also shows data concentration/density
- **Subplots** — `plt.subplots()` creates the figure, `plt.subplot(rows, cols, position)` places each individual plot

---

### Day 7 — Data Visualization Hands-on (Real Dataset)
Applied all visualization concepts on a real `cars.csv` dataset.

- Loaded and explored the dataset — checked `.info()`, `.describe()`, nulls, and duplicates (dataset was clean)
- **Scatter Plot** — plotted `mpg` vs `hp`, then added `hue='brand'` to color-code by car brand
- **Subplots with Seaborn** — created side-by-side and stacked scatter plots (`mpg vs hp` and `cylinders vs hp`)
- **Bar Plot subplots** — `cylinders vs hp` and `cylinders vs mpg` side by side using `sns.barplot()` with `hue='brand'`
- **Pie Chart** — plotted brand distribution using `value_counts()` on the brand column with `explode` and `shadow`
- **Box Plot** — `cylinders vs hp` grouped by brand to compare distributions
- **Heatmap** — used `df.select_dtypes([int, float])` + `.corr()` to build a correlation matrix, then visualized it with `sns.heatmap()`, `annot=True`, and different `cmap` options (`Set2`, `Blues`)
- **3D Scatter Plot** — used `plotly.express` (`px.scatter_3d`) to plot `mpg`, `hp`, and `brand` in an interactive 3D chart

---

### Day 8 — Statistics & Probability (Theory + Code)
Covered statistics from scratch — theory first, then implemented everything in Python using `numpy` and the `statistics` library.

- What statistics is — collecting, organizing, analyzing, interpreting, and presenting data
- Types of Stats — Descriptive (summarize data) vs Inferential (draw conclusions/predictions)
- Measure of Central Tendency — Mean, Median, Mode using both `np` and `stats` library; understood why `stats` returns int vs `np` returns float, and how `stats.mode()` vs `stats.multimode()` differ
- Population vs Sample — sample is a subset of population; biased samples give biased results
- Types of Sampling — Random (`random.sample()`), Systematic (every kth element via slicing), Stratified (split into groups, sample each)
- Measure of Dispersion — Range (`np.ptp()`), Variance (`np.var()`), Standard Deviation (`np.std()`); understood why `numpy` and `statistics` give different answers — numpy uses population formula (÷n), stats uses sample formula (÷n-1)
- Percentile & Quartiles — `np.percentile()` for any percentile; Q1/Q2/Q3 at 25/50/75
- Outlier Detection — IQR method (Lower Bound = Q1 − 1.5×IQR, Upper Bound = Q3 + 1.5×IQR); visualized using box plot
- Correlation — Positive, Negative, Zero; used iris dataset with `.corr()` + `sns.heatmap()` to visualize relationships
- Types of Data — Qualitative (Nominal, Ordinal) vs Quantitative (Discrete, Continuous)

---

### Day 9 — Probability (Theory + Hands-on)
Covered probability concepts with theory and applied them on a real dataset using Pandas.

- What probability is — measure of how likely an event is to occur; P(A) = favourable outcomes / total outcomes
- Key terms — Experiment (any process with an outcome), Event (specific group of outcomes), Outcome (result of a single trial)
- Types of Events — Simple event (one specific outcome) vs Compound event (group of outcomes, e.g. getting an even number on a dice)
- Marginal Probability — probability of a single event without considering others (e.g. P(red ball) = 5/8)
- Joint Probability — probability of two or more events happening simultaneously (e.g. rolling 3 on two dice = 1/6 × 1/6 = 1/36)
- Conditional Probability — probability of an event given another has already occurred (e.g. P(King | Face card) = 4/12)
- Hands-on — used `Country.csv` and `tips` dataset; calculated marginal probability of a day being Sunday using `len()` filtering and `value_counts()`

---

### Day 10 — Airbnb NYC Case Study (End-to-End EDA)
Applied everything learned so far on a real Airbnb New York City dataset (~48,895 rows, 16 columns). Full EDA pipeline from loading to visualization.

- Loaded `Airbnb_datanew.csv` using `pd.read_csv()` and explored shape, columns, and data types
- Checked duplicates (none) and null values — found nulls in `listing_name`, `host_name`, `last_review`, and `reviews_per_month`
- Handled nulls contextually — filled `listing_name` with `'Unknown'`, `host_name` with `'no_name'`, `reviews_per_month` with `0`; dropped `last_review` column entirely (date column, not needed for analysis)
- Removed price outliers using IQR method — filtered out extreme pricing values before analysis
- Used `value_counts()` to analyze distribution of `room_type` (Entire home/apt: 22,784 | Private room: 21,996 | Shared room: 1,138)
- Visualized neighbourhood group distribution with `sns.countplot()`
- Visualized room type distribution with `sns.countplot()`
- Plotted `neighbourhood` vs `reviews_per_month` using `sns.barplot()` on a random 30-row sample with `plt.xticks(rotation=90)`

---

### Day 11 — Inferential Statistics: Confidence Interval
Understood why we can't always study the full population and how confidence intervals solve that.

- Why inferential stats exist — population is too large, time-consuming, expensive; we use samples to infer about population
- Point Estimation vs Confidence Interval — point estimation says sample mean = population mean (not accurate); CI gives a range instead
- Margin of Error — maximum error allowed while estimating sample mean; used to construct the CI range
- Bigger interval = more confidence, smaller interval = less confidence; 100% confidence makes the interval useless
- Normal Distribution — mean, median, mode are equal and symmetric; used as the basis for CI calculations
- Z-score — measures how far the sample mean is from the population mean in standard deviations
- Confidence levels — 90%, 95%, 99% each correspond to a specific Z-score; chosen based on the problem

---

### Day 12 — Inferential Statistics: Sampling + Hypothesis Testing
Covered Central Limit Theorem, sampling strategies, and introduced hypothesis testing with Z-test and T-test.

- Central Limit Theorem — if sample size > 30, the sampling distribution will always be normally distributed regardless of population shape; 30 is the bare minimum
- Random Sampling — works when population is homogeneous (e.g. all ₹20 Lays packets)
- Stratified Sampling — divide population into groups (rich, middle, poor) and sample proportionally from each; used when population has clear subgroups
- Hypothesis Testing — Null Hypothesis (H₀) = no change/difference; Alternative Hypothesis (H₁) = there is a difference
- One Sample Z-Test — used when population std is known; calculated Z-statistic and p-value using `scipy.stats.norm.sf()`; if p < 0.05 → reject null
- One Sample T-Test — used when population std is unknown; first checked normality with `shapiro()`, then ran `ttest_1samp()`; if shapiro fails → use `mannwhitneyu` instead
- p-value logic — if p < 0.05 we have enough evidence to reject the null hypothesis

---

### Day 13 — Inferential Statistics: Two-Sample T-Test, ANOVA, Chi-Square
Applied hypothesis testing on real problems with multiple samples and categorical data.

- Two-Sample T-Test — compares means of two independent groups; prerequisites: both normally distributed (`shapiro()`), equal variance (`levene()`); used `ttest_ind()` with `equal_var=True/False` based on Levene result
- Practiced on dept salaries (unequal variance → `equal_var=False`) and battery suppliers (equal variance → `equal_var=True`)
- ANOVA (`f_oneway`) — used when comparing more than 2 groups; same prerequisites (normality + equal variance + independence); if any condition fails → use `kruskal` test instead
- Practiced on 4 service center satisfaction scores; p < 0.05 → centers perform differently
- Chi-Square Test (`chi2_contingency`) — used for categorical data to test independence between two variables; practiced on advertising medium vs purchase decision contingency table
- Libraries used — `scipy.stats`: `shapiro`, `levene`, `ttest_ind`, `f_oneway`, `kruskal`, `chi2_contingency`

---

### Day 14 — Linear Algebra for ML
Covered the math behind how ML models actually see and process data.

- Data types in linear algebra — Scalar (single number), Vector (1D array), Matrix (2D array), Tensor (3D+ array)
- How images work — grayscale images are 2D matrices of values 0–255; colored images are 3D tensors (RGB channels stacked)
- Vectors have magnitude and direction — ML uses these to understand where data points are in space
- Transpose — converts rows to columns; ML does this by default before any calculation; used in portrait ↔ landscape image conversion
- Text vectorization — unique words extracted from a column become features; each sentence is represented as a vector of 0s and 1s
- Matrix operations in NumPy — addition/subtraction (`+`, `-`), scalar addition, element-wise multiplication (Hadamard product: `mat1 * mat2`), actual dot product (`mat1 @ mat2` or `np.dot()`)
- Matrix Rank — `np.linalg.matrix_rank()`; tells how many rows/columns carry unique info; low rank = redundant data
- Determinant — `np.linalg.det()`; if zero → singular matrix → no inverse exists
- Inverse — `np.linalg.inv()`; used in ML for finding weights (W); only exists when determinant ≠ 0
- Eigen Vectors — vectors that don't change direction when multiplied by a matrix; Eigen Values = how much they scale

---

### Day 15 — Linear Algebra Hands-on Practice
Practiced all Day 14 concepts with focused NumPy exercises and logical problems.

- Created 3×3 matrix with random ints (1–100) and performed all scalar operations — add, subtract, divide, multiply
- Created 4×4 matrix and iterated using nested loops to print odd numbers row by row
- Calculated mean of each row using `.mean()` inside a loop
- Created two 2×2 matrices and applied all matrix operations — `np.add()`, `np.subtract()`, element-wise `*`, dot product `@`, and division
- Proved all 4 transpose properties using `np.array_equal()`:
  - `(A')' = A` ✓
  - `K × A' = (KA)'` ✓
  - `(A+B)' = A' + B'` ✓
  - `(AB)' = B'A'` ✓
- Filtered even numbers less than 69 from each row of a 4×4 matrix using nested loop + conditions
- Printed all values greater than the array mean from a 1D array of 10 random ints
- Found maximum value in a 15-element array using a `while` loop (without `np.max()`)
- Built a character frequency dictionary from a string using a loop — `{char: count}`
- Calculated string length without any built-in function using a counter loop

---

### Day 16 — Introduction to ML + Linear Regression Theory
Covered the full ML landscape and understood the math behind linear regression before touching any code.

- What ML is — giving weightages (W) to input columns so the model can predict output; W is calculated by the model itself
- Types of ML — Classical ML (structured data) vs Deep Learning (large/unstructured data)
- Classical ML split — Supervised (labeled input + output) vs Unsupervised (only input, no labels)
- Supervised tasks — Regression (numerical output e.g. house price) vs Classification (categorical output e.g. fraud/not fraud)
- Unsupervised — clustering similar data points into groups (e.g. market segmentation)
- Deep Learning — ANN (large data), CNN (images/videos), RNN (sequential data like stocks/books)
- NLP — converts human language to machine-understandable format (used in GPT, Gemini)
- Reinforcement Learning — agent gets reward for right action, punishment for wrong; used in self-driving cars and LLM training
- Linear Regression — technique for prediction; finds the best fit line through data points
- Best fit line — the line for which Mean Squared Error (MSE) is minimum; squared to eliminate negative errors
- Finding m and c — done by taking derivative of MSE and setting it to 0 (minimization using calculus)
- Gradient Descent — iterative method to minimize error when calculus approach isn't feasible on real messy data

---

### Day 17 & 18 — Linear Regression Hands-on (Insurance Dataset)
Built a full linear regression pipeline on a real insurance dataset — from raw data to model evaluation.

- Loaded `new_insurance_data.csv`, explored with `.head()`, `.info()`, `.describe()`, `.isnull().sum()`
- Null handling — total nulls were ~3% of rows, so dropped them with `dropna(inplace=True)`
- Outlier check — plotted boxplots for all numerical columns; kept all outliers as natural medical extremes
- Multicollinearity — when two+ independent columns are highly correlated, model gets confused about feature importance
- VIF (Variance Inflation Factor) — higher VIF = more correlated with other columns; VIF > 10 is bad; used `variance_inflation_factor` from `statsmodels`
- Dropped columns iteratively based on VIF — removed `num_of_steps`, `Anual_Salary`, `NUmber_of_past_hospitalizations`, `bmi` until all VIF < 10
- Label Encoding — converted categorical columns to numerical using `LabelEncoder` from `sklearn`; ML models only work with numbers
- Train-Test Split — `train_test_split(x, y, test_size=0.2, random_state=0)`; 80% train, 20% test
- Model building — `LinearRegression()` from `sklearn`, trained with `.fit(x_train, y_train)`
- Prediction — `model.predict(x_test)`; compared actual vs predicted charges in a DataFrame
- Evaluation — R² Score using `r2_score(y_test, y_pred)`
- Key insight — removing multicollinearity doesn't always improve prediction accuracy (R²) but it does fix feature importance; with high VIF the `coef_` values are misleading
- Visualized prediction vs actual using `sns.regplot()` with a regression line

  
---

## - Tools Used

- **Python 3.12**
- **Pandas** — for working with tables and datasets
- **NumPy** — for numerical operations and arrays
- **Jupyter Notebook** — for writing and running code interactively
- **Matplotlib** — for core plotting and charts
- **Seaborn** — for advanced, cleaner visualizations built on Matplotlib
- **Plotly** — for interactive 3D charts
- **statistics** — (built-in) | For mean, median, mode, variance — sample-formula based calculations 
- **scipy** For statistical tests — Z-test, T-test, ANOVA, Chi-Square, Shapiro-Wilk, Levene 
- **statsmodels** - For VIF (Variance Inflation Factor) to detect multicollinearity
- **scikit-learn** - For Label Encoding, Train-Test Split, Linear Regression, and R² Score
- **On Anaconda Navigator - jupyter notebook**
