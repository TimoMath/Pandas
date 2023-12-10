# Pandas
Data Analysts files
We're ready to get started!
Create a new file using this button in the folder you just created and call it `basic_python_datatypes.ipynb`
### Libraries and Installing new libraries

One of the reasons that Python is such a great programming language is that people are constantly creating things called Libraries. These are large lumps of code that you can call in order to execute very complicated operations. If you wanted to run a machine learning algorithm for example, you'd install a library in your computer and call that library.
* conda install numpy
* Pandas or "Panel Data" is the core library to handle structured data in Python. Structured data is just data in a tabular format (like in Excel). First let's install Pandas. We will install it the same way we installed NumPy.
Import Pandas
Like before, we need to import the library into our code editor. We'll alias it as pd
import pandas as pd
​
Series
The core of Pandas is the DataFrame. A DataFrame is basically a table and is composed of Series. A Series is a set of values that are indexed. Try the code below.
series_test = [1, 2, 3, 6, 7]
print(pd.Series(series_test))

### DataFrames

Although we've almost entirely created our own data throughout this process, you'll usually work with data that already exists. This is where the `read_***` method of Pandas comes in. This allows you to read in data from any number of data sources including:

- CSVs
- Excel
- Stata
- SAS
- SPSS
- SQL
- Big Query
- ORC
- and much more!

For this tutorial we'll be sticking mostly to reading CSV's because there usually are special setups you need to get right to read data from SQL databases. 

A CSV stands for "comma-separated values" and is a text format that separates each record with a comma and each line with a newline ("enter" key). It is part of a family of formats that include tab-separated values where the commas are separated by tabs, and pipe-separated values where the commas are separated by pipes (|). The commas, tabs, and pipes are what we call "delimiters".

In the folder you downloaded, there should be a file called "simple_csv.csv". Let's import that.

* import os # This will be used to tell us where the file is
import pandas as pd

pwd = os.getcwd() # This creates a string of the folder this Python Script is stored in

filepath = pwd + "/simple_csv.csv" # This creates a string that is the filepath to the simple_csv file

first_import = pd.read_csv(filepath) # This reads the csv into Python
first_import

