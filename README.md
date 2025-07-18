# US_IO_Capital_Disaggregation
This repository documents code, data and outputs for disaggregating private and government capital formation for detailed U.S historical benchmark input-output data, with the purpose of preparing investing-industry-specific end-use shares.

The methods and documentation are in the progress of being prepared for my MSc Thesis

Below follows a description of the information contained in this repository.

- Python scripts (work in progress):

  - Disagg_government_purchases extracts specified final demand categories from prepared total transactions and use tables from the US historical benchmark input-output tables (1963-2012). Then it creates concordance tables for the defined aggregate categories of government purchases, grouping industry codes based on the year of highest aggregation (1997) (lowest common denominator). Finally it constructs a binary matrix of the aggregate categories as columns with full detail categories in rows with a binary 0/1 format for matrix multiplication to aggregate all years.
 
  - Disagg_private_capital converts industry-specific capital formation sheets in the BEA's detailed Fixed Asset Accounts into full industry annual data frames (and optionally excel sheets). Then it creates new Y-matrices from concordances to aggregate and match the benchmark commodity format to the detailed FAA commodity format, allowing the I-O capital formation to be matched to FAA capital formation.

 - Input data:

   - BEA benchmark IO tables & assembly contains the inter-industry raw data with full final demand categories: total transactions for years 1963 and 1967, and use-tables for 1972-2012 which have been assembled by pHD Jan Streeck: https://github.com/janstre/Material_End_Use_Shares drawn from the BEA's historical benchmark data: https://www.bea.gov/industry/historical-benchmark-input-output-tables
  
   - Detailed Fixed Asset Accounts contains the detailed FAA commodity data for non-residential (structures, equipment and IP) and residential investment data drawn from the BEA's "underlying detail" fixed assets tables: https://apps.bea.gov/national/FA2004/Details/Index.htm, see https://www.bea.gov/itable/fixed-assets for more details
  
- Output data:

  - Aggregated Y-matrices contains output from the Disagg_government_purchases script with disaggregated government final demand for all historical benchmark years.
 
  - New Final demand tables contains output from the Disagg_private_capital scripts with disaggregated private capital formation for years 1901-2023, this output is only temporary as the full script is still a work in progress.
 
