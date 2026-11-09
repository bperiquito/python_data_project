# Amazon Reviews 2023 – Electronics Data Analysis

## Project Description

This project explores and analyzes data from the **Amazon Reviews 2023 – Electronics** dataset using Python.

The goal of the project is to collect, clean, transform, and visualize product and review data in order to identify highly rated products that could be useful for further Machine Learning analysis.

The project demonstrates fundamental Python and data analysis concepts, including working with datasets, loops, functions, exception handling, data filtering, data transformation, and data visualization.

## Getting Started

The project was developed using **Python and Jupyter Notebook**.

To run the project locally, download or clone this repository and open the Jupyter Notebook.

### Dependencies

The following Python libraries are required:

```bash
datasets<4
pandas
matplotlib
seaborn
pyarrow
```

They can be installed with:

```bash
pip install "datasets<4" pandas matplotlib seaborn pyarrow
```

### Installation

1. Clone the repository:

```bash
git clone <https://github.com/bperiquito/python_data_project>
```

2. Navigate to the project directory:

```bash
cd <python_data_project>
```

3. Install the required dependencies:

```bash
pip install "datasets<4" pandas matplotlib seaborn pyarrow
```

4. Start Jupyter Notebook:

```bash
jupyter notebook
```

5. Open the project `.ipynb` file and run the cells in order.

## Testing

The project does not include automated tests.

Data validation is performed throughout the notebook by checking DataFrame structures, data types, missing values, filtering results, and the number of records produced during the different stages of the analysis.

For example:

```python
len(top_products_df)
len(item_metadata_df)
```

These checks help confirm that the data collection and filtering operations produce the expected results.

## Project Instructions

The project follows a complete basic data-analysis workflow.

### 1. Environment Setup

Install and import the required Python libraries, including:

- datasets
- pandas
- matplotlib
- seaborn
- pyarrow

### 2. Amazon Reviews Dataset

Load the **Amazon Reviews 2023 Electronics** review dataset using the Hugging Face `datasets` library.

The dataset is loaded using streaming and limited to a sample of 100 reviews.

The collected reviews are converted into a pandas DataFrame for exploration.

Screenshot:
![Dataextraction1](screenshots/firstdataextractionpart1.png)
![Dataextraction2](screenshots/second%20data%20extraction%20products%20part2.jpg)

### 3. Product Metadata

Load the Electronics product metadata dataset and collect a sample of 100 products.

The metadata is converted into a pandas DataFrame containing information about the products, including their titles, ratings, and prices.

Screenshot:
![Dataextraction21](screenshots/second%20data%20extraction%20products%20part1.jpg)
![Dataextraction22](screenshots/second%20data%20extraction%20products%20part2.jpg)

### 4. Data Exploration

Explore the datasets using pandas functionality such as:

```python
DataFrame.info()
```

The project also examines the available columns and their respective data types.

### 5. Product Lookup

Create a Python function that searches for a product by title and returns its price.

Exception handling is implemented to manage cases where:

- A product cannot be found.
- A product does not have a valid price.

### 6. Data Cleaning and Filtering

Create a cleaned DataFrame containing the following relevant columns:

- `title`
- `average_rating`
- `price`

Products are initially selected when they:

- Have a valid title.
- Have an average rating of **4.5 or higher**.
- Have a valid numerical price.

The resulting dataset is stored in:

```python
top_products_df
```
Screenshot:
![Cleaning](screenshots/cleaning%20the%20data%20to%20top%20products%20only.jpg)

### 7. Percentage Calculation

Create a reusable Python function to calculate what percentage of the original dataset remains after the cleaning and filtering process.

The calculation follows:

```python
percentage = (part / whole) * 100
```

### 8. Working With Lists

Extract the titles of the top-rated products from the DataFrame and store them in a Python list using a `for` loop and the `.append()` method.

### 9. Data Visualization

Create visualizations using Matplotlib and Seaborn.

A histogram is used to analyze the distribution of prices among highly rated products.

A scatterplot is also created to explore the relationship between:

- Product price
- Average rating

Screenshot:
![View1](screenshots/creating%20data%20visualization%20for%20BI%20team.jpg)

### 10. Highly Rated Products Dashboard

For the final analysis, products with an average rating of **4.7 or higher** are selected.

The products are sorted by average rating in descending order and displayed as a table.

A scatterplot visualizes the relationship between price and rating for these highly rated products.

Screenshot:
![View2](screenshots/creating%20data%20visualization%20for%20BI%20team2.jpg)

### 11. Exporting Results

The final cleaned dataset is exported into two formats:

```text
top_products.csv
top_products.parquet
```
Screenshot:
![Files](screenshots/Saving%20the%20data%20for%20IA%20team.jpg)

The project also produces a `user_inputs.txt` file containing responses to the reflection questions completed throughout the notebook.

## Key Skills Demonstrated

- Python fundamentals
- Jupyter Notebook
- Variables and data types
- Lists
- `for` loops
- Functions
- Exception handling
- Boolean operators
- pandas DataFrames
- Data cleaning
- Data filtering
- Data transformation
- Dataset streaming
- Data visualization
- CSV and Parquet data export
- Basic exploratory data analysis

## Built With

- **Python** – Core programming language
- **Jupyter Notebook** – Interactive development environment
- **pandas** – Data manipulation and analysis
- **Hugging Face Datasets** – Dataset loading and streaming
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical data visualization
- **PyArrow** – Parquet data support

## Dataset

The project uses the **Amazon Reviews 2023** dataset, specifically the Electronics reviews and product metadata datasets provided through Hugging Face.

## Project Outputs

The repository includes or generates:

```text
project_notebook.ipynb
top_products.csv
top_products.parquet
user_inputs.txt
README.md
```

## License

See the [LICENSE](LICENSE.txt) file for license information.