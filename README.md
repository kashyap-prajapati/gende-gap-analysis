# gende-gap-analysis

# Gender Pay Gap Analysis

This project aims to analyze and visualize the gender pay gap across different regions and job titles. Using data from a Cassandra database, the project explores the disparities in pay between men and women, investigates legal provisions related to gender pay equality, and presents the findings through various charts and graphs.

## Table of Contents

1. [Setup Instructions](#setup-instructions)
2. [Data Sources](#data-sources)
3. [Project Structure](#project-structure)
4. [Key Components](#key-components)
5. [Usage](#usage)
6. [Contributing](#contributing)
7. [License](#license)

## Setup Instructions

### Prerequisites

Ensure you have the following software installed:

- Python 3.x
- Anaconda (recommended)
- Astra Token and Secure Connect Bundle for connecting to the Cassandra database

### Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/yourusername/gender-pay-gap-analysis.git
   cd gender-pay-gap-analysis
   ```

2. Create and activate a virtual environment:

   ```sh
   conda create --name gender-pay-gap python=3.8
   conda activate gender-pay-gap
   ```

3. Install the required packages:

   ```sh
   pip install -r requirements.txt
   ```

4. Obtain your Astra Token and Secure Connect Bundle from DataStax Astra. Place the `secure-connect-bundle.zip` and `fairview-db-token.json` files in the root directory of the project.

### Configuration

1. Open the `fairview-db-token.json` file and ensure it contains your client ID and secret.

2. Update the `cloud_config` dictionary in the script to point to your secure connect bundle:

   ```python
   cloud_config = {
     'secure_connect_bundle': 'secure-connect-fairview-db.zip'
   }
   ```

## Data Sources

The data used in this project is sourced from the Fairview database hosted on DataStax Astra. It includes datasets on:

- Wage and salaried workers percentage of employment
- Gender pay gap details across various job titles
- Global and regional pay scores from the Women, Business, and the Law (WBL) study

## Project Structure

- `gender_pay_gap_analysis.ipynb`: Jupyter notebook containing the main analysis and visualizations.
- `requirements.txt`: List of dependencies required for the project.
- `secure-connect-fairview-db.zip`: Secure connect bundle for Cassandra database.
- `fairview-db-token.json`: JSON file containing client ID and secret for database authentication.

## Key Components

### Data Extraction

Data is extracted from the Cassandra database using the `cassandra-driver` library. Queries are executed to fetch relevant datasets for analysis.

### Data Visualization

Visualizations are created using libraries such as `matplotlib`, `seaborn`, and `plotly`. Key visualizations include:

- Line plots showing the percentage of male and female employment over the years.
- Bar charts comparing base pay and bonus pay for different job titles between men and women.
- Pie charts illustrating the legal provisions related to gender pay equality across different economies.

### Analysis

The analysis focuses on identifying trends and disparities in the gender pay gap, both globally and regionally. It also examines the impact of legal provisions on gender pay equality.

## Usage

1. Run the Jupyter notebook:

   ```sh
   jupyter notebook gender_pay_gap_analysis.ipynb
   ```

2. Follow the instructions in the notebook to execute each cell and generate the visualizations.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes. Ensure your code adheres to the existing style and includes relevant tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

