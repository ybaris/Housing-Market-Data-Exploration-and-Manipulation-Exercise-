The City of Syracuse approached us to build a predictive model of the house market sale prices for all the properties in the city based on the physical characteristics of the building and other metrics. They shared with us four different datasets:

- Sales
- Improvements
- Residential Building
- Assessments

The City also provided data dictionaries and some tips about the data:

- A parcel can contain several sites. Sometimes each site is a property, but other times it's only an addition that will be sold together with the main house.
- Once an improvement is built (either at the same time of the construction or later), the improvement is registered each time that there is an inspection of the property.
- Improvements are registered independently of the time of a sale. For the same property, we might find improvements done both before and after a sale, but we only want to take into account those that affect the sale price.
- There is a field in the sales table, ARMS\_LENGHT (spelling corresponds with the original city data), that provides information on whether or not the sale represents an

  arms-length transaction. Therefore, it can be used to filter the sales considered not representative.

- There are also sales that, despite being marked as arms\_lenght transaction, might not be. For example: Suspicious sales happen when a house is bought, refurbished, and sold again within a small time frame, or when the sale price is very low.

We want to explore the data, and properly combine the datasets so that we have all of the information in a unique table. The final table should have a unique sale in each row, with all the building characteristics and improvements remarkable to that sale in the same row, and should be ready for modeling (all values numeric). To prepare a final table:

1. Explore the data on each of the Sales, Improvements, and Residential Building tables.
1. Clean the data on the previous tables: look for duplications, missing or incorrect data, data type issues, necessary filters, etc. If you had to make any assumption during that process, it’s ok! Take notes and share them with us.
1. Combine the previous three datasets in a single table:

   0. Merge the datasets.
   0. Do any final cleaning with all the information combined, if necessary.
   0. Make sure each row in the final table is a unique sale (we want to predict sale prices).

We also want to explore the assessments done by city inspectors and check whether there might be any equity issues with the assessment process. Combining the assessment information with the sale prices of properties, create a graph with sale prices on the x-axis and the difference between assessment value (full market price) and sale price on the y-axis. Briefly comment what you see with an equity angle.


