# bmc_bioinformatics_2017
Data and materials for the publication, 'Unsupervised deep learning reveals prognostically relevant subtypes of glioblastoma'.
The data are zipped in file tcga_expression_data_bmc_bioinformatics_2017.csv.zip. 

To get to 15,404 columns, we removed columns with any NAs in the column:

```python
import pandas as pd
df = pd.read_csv('tcga_expression_data_bmc_bioinformatics_2017.csv')
df2 = df.dropna(axis=1, how='any’)
```

The data here have been binarized (as mentioned in the 'Data' section of the methods of the paper), but have note been preprocessed beyond this.
