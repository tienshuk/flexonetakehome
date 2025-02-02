# Approach
## The JSON data was converted into a structured pandas DataFrame to facilitate validation and analysis. The hierarchical structure of the data was flattened to allow for roll-up calculations and visualizations.

# Assumptions
## The account_type (assets, liabilities, equity) represents the parent node.
## Each category within an account type represents a sub-category.
## Product names are nested within categories, forming a three-level hierarchy.

# Issues and Inconsistencies
## Some values in category and product name columns are identical to values in account_type, which could indicate misclassification.
## Missing data exists, and in some cases, missing values were assumed to be replaced by the account_type value.
## Roll-up validation showed discrepancies where parent totals did not always match the sum of their child nodes.

# Additional Steps If Time Allows
## Seek clarification on missing and repeated values to determine if they are intentional or data errors.
## Identify appropriate data imputation strategies to handle missing values.
## Improve roll-up validation logic to accommodate edge cases.
## Develop automated data validation checks for future data ingestion.
