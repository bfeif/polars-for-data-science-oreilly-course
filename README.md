# Polars for Data Science: Tackling Real-World Data Challenges

Welcome to "Polars for Data Science: Tackling Real-World Data Challenges"!

This course, created in partnership with O'Reilly Media, is designed to provide a comprehensive and practical understanding of [Polars](https://github.com/pola-rs/polars), an innovative tool for data manipulation and analysis. The video course can be found on O'Reilly Media here: [Polars for Data Science: Tackling Real-World Data Challenges](https://learning.oreilly.com/course/polars-for-data/0642572019327/).

This GitHub repository provides the course material, including:
- Jupyter notebooks for each module of the course (see `module_notebooks/`).
- A quiz Jupyter notebook for each module of the course (see `quiz_notebooks/`).
- A corresponding quiz solution Jupyter notebook for each module of the course (see `quiz_solution_notebooks/`).

The course will take you from zero Polars all the way to integrating Polars into your data science workflow. So buckle up!

This README provides instructions for installing the required packages, as well as downloading the data files which are used throughout the course.

## Course Overview

- **Introduction**: Understand what makes Polars a groundbreaking technology for data science, where it sits in the landscape of data science tooling, and have an intuition of the syntax differences between Polars, Pandas, and SQL.
- **Getting Started**: Be familiar with Polars's two modes, lazy-mode versus in-memory mode, and understand how to leverage Polars's query optimization.
- **Data Manipulation I: Basics**: Be familiar with the Polars API, and be able to perform basic selecting and filtering queries.
- **Data Manipulation II: Grouping and Aggregation**: Be able to perform Polars queries that involve aggregations, such as group-by's and window functions.
- **Data Manipulation III: Combining Data**: Be able to perform Polars queries that involve combining data, such as joins and concatenations.
- **Data Manipulation IV: Data Types**: Understand all the different data types that exist in Polars, and how to work with them.
- **Data Manipulation V: IO and Interoperation**: Be able to switch their data seamlessly between Pandas, Numpy, and Polars, and be able to read and write data both locally and to the cloud.
- **Integrating with the Data Science Workflow**: Be comfortable using Polars in a typical everyday data science workflow, integrating it with Matplotlib, Plotly, and Scikit Learn.
- **Conclusion**: Have their understanding of the different facets of Polars unified into one clear picture, and be prepared with all the knowledge and reference resources they need to continue using Polars on an everyday basis while growing their knowledge of the tool.

## Installation Instructions

To get started with the course, you'll need to set up your environment with the required packages. The requirements are listed in the `requirements.txt` file. Below are the instructions for Mac with Intel chip, Mac with M1 chip, and Windows.

### Mac with Intel Chip

1. **Install Python with Homebrew** (if not already installed):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   brew install python
   ```

3. **Create and activate a virtual environment**:
   ```bash
   python3 -m venv polars-env
   source polars-env/bin/activate
   ```

4. **Install the required packages**:
   ```bash
   pip install -r requirements.txt
   ```

### Mac with M1 Chip

1. **Install Homebrew** (if not already installed):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Install Python**:
   ```bash
   brew install python
   ```

3. **Create and activate a virtual environment**:
   ```bash
   python3 -m venv polars-env
   source polars-env/bin/activate
   ```

4. **Install the required packages**:
   ```bash
   pip install -r requirements.txt
   ```

### Windows

1. **Install Python** (if not already installed):
   Download and install Python from the [official website](https://www.python.org/downloads/).

2. **Create and activate a virtual environment**:
   ```bash
   python -m venv polars-env
   polars-env\Scripts\activate
   ```

3. **Install the required packages**:
   ```bash
   pip install -r requirements.txt
   ```

## Downloading the Data
This course uses NYC Taxi data from the [NYC Taxi and Limousine Commission Page](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page); more specifically, it uses:
- Yellow Taxi Trip Records from 2024-02
- Yellow Taxi Trip Records from 2024-03
- Green Taxi Trip Records from 2024-03
- Taxi Zone Lookup Table

These data files (in their required formats) can all be downloaded from the public AWS S3 Bucket https://polars-for-data-science-oreilly-course-data-resources.s3.amazonaws.com. This can be done manually or using the AWS CLI:

### Option 1: Downloading the Data Manually
1. Visit the following URLs in your web browser. For each URL, you should be prompted  to download the file; you should download each file to the directory `data/`:
   - https://polars-for-data-science-oreilly-course-data-resources.s3.amazonaws.com/yellow_tripdata_2024-02.parquet
   - https://polars-for-data-science-oreilly-course-data-resources.s3.amazonaws.com/yellow_tripdata_2024-03.parquet
   - https://polars-for-data-science-oreilly-course-data-resources.s3.amazonaws.com/yellow_tripdata_2024-03.csv
   - https://polars-for-data-science-oreilly-course-data-resources.s3.amazonaws.com/green_tripdata_2024-03.parquet
   - https://polars-for-data-science-oreilly-course-data-resources.s3.amazonaws.com/taxi_zone_lookup.csv

### Option 2: Downloading the Data with the AWS CLI
1. **Install the AWS CLI** (if not already installed):
   - For macOS: `brew install awscli`
   - For Windows: Download and run the installer from [AWS CLI Installation Guide](https://aws.amazon.com/cli/)

2. **Download the data files using AWS CLI**:
   ```bash
   # Download all required files
   aws s3 cp s3://polars-for-data-science-oreilly-course-data-resources/yellow_tripdata_2024-02.parquet data/
   aws s3 cp s3://polars-for-data-science-oreilly-course-data-resources/yellow_tripdata_2024-03.parquet data/
   aws s3 cp s3://polars-for-data-science-oreilly-course-data-resources/yellow_tripdata_2024-03.csv data/
   aws s3 cp s3://polars-for-data-science-oreilly-course-data-resources/green_tripdata_2024-03.parquet data/
   aws s3 cp s3://polars-for-data-science-oreilly-course-data-resources/taxi_zone_lookup.csv data/
   ```

   Note: The AWS CLI commands above should work without AWS credentials since these files are publicly accessible.




## Additional Notes

Ensure that you have Jupyter Notebook installed and ready to use, as the course modules are provided in the form of Jupyter notebooks. If you encounter any issues with the installation or setup, please refer to the [official documentation](https://jupyter.org/install) for additional support.

Happy learning and enjoy your journey into the world of Polars!