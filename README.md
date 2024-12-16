# Home Sales Analysis with SparkSQL
This project analyzes a dataset of home sales using SparkSQL to answer specific questions about property prices. The data is queried and processed in a PySpark environment, and the results provide insights into real estate trends.

## Dataset
The dataset contains the following columns:

- id: Unique identifier for each sale

- date: Date of the sale

- date_built: Year the home was built

- price: Sale price of the home

- bedrooms: Number of bedrooms

- bathrooms: Number of bathrooms

- sqft_living: Square footage of the living area

- sqft_lot: Square footage of the lot

- floors: Number of floors

- waterfront: Whether the property has a waterfront (1 = yes, 0 = no)

- view: View rating of the property (0-100)

The dataset is loaded into a Spark DataFrame and queried using SparkSQL.

## Questions and Results
### Average Price for a Four-Bedroom House Sold Each Year
| Year_Built              | In Average_Price |
| :---------------- | :------: |
| 2017 | 296,576.69 |
| 2016 | 296,050.24 |
| 2015 | 307,908.86 |
| 2014 | 299,073.89 |
| 2013 | 299,999.39 |

### Average Price of a Home with 3 Bedrooms and 3 Bathrooms Each Year
| Year_Built              | In Average_Price |
| :---------------- | :------: |
| 2017 | 292,676.79 |
| 2016 | 290,555.07 |
| 2015 | 288,770.30 |
| 2014 | 290,852.27 |
| 2013 | 295,962.27 |

### Average Price of a Large Home (3 Bedrooms, 3 Bathrooms, 2 Floors, ≥ 2,000 Sqft)
| Year_Built              | In Average_Price |
| :---------------- | :------: |
| 2017 | 280,317.58 |
| 2016 | 293,965.10 |
| 2015 | 288,770.30 |
| 2014 | 298,264.72 |
| 2013 | 303,676.79 |

### Average Price of a Home Per "View" Rating (Price ≥ $350,000)
| Year_Built              | In Average_Price |
| :---------------- | :------: |
| 99 | 1,061,201.42 |
| 98 | 1,053,739.33 |
| 97 | 1,129,040.15 |
| 96 | 1,017,815.92 |
| 95 | 1,054,325.60 |

## Runtime:

Uncached query runtime: ~0.54 seconds

Cached query runtime: ~0.30 seconds

Partitioned query runtime: ~0.38

Improvement: 0.24 seconds faster

## Conclusion

Using SparkSQL, we efficiently analyzed trends in home sales. Caching and partitioning techniques significantly improved query performance. This analysis highlights the power of distributed computing for large datasets.

## Future Enhancements

- Explore additional filtering criteria, such as waterfront properties.

- Perform advanced aggregations and visualizations.

- Integrate MLlib for predictive modeling.
