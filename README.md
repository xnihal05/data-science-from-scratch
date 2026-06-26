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

## - Tools Used

- **Python 3.12**
- **Pandas** — for working with tables and datasets
- **NumPy** — for numerical operations and arrays
- **Jupyter Notebook** — for writing and running code interactively
- **Matplotlib** — for core plotting and charts
- **Seaborn** — for advanced, cleaner visualizations built on Matplotlib
- **Plotly** — for interactive 3D charts
- **statistics** — (built-in) | For mean, median, mode, variance — sample-formula based calculations |
- **On Anaconda Navigator - jupyter notebook**
