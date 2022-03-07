Data Sourcing
--
- Public Data: This is the data that is made publicly available for the purpose of research and learning.
- Private Data: This is organisational data, and organisations have some security and privacy concerns. Company approvals are needed to access such data. It is useful for internal policymaking and business strategy building for an organisation.
- Web Scraping: majorly involves 4 steps -
  - HTML loading and reading: It includes the loading of the HTML page into Python. The library which is used here to request for the HTML page is the “request” library. 
  - HTML parsing: This step involves the process of presentation of HTML code into a readable format. One of the important classes of Python called “BeautifulSoup” is used here to parse the data.
  - Data extraction: This step involves the extraction of data from the web page using HTML elements like tags and attributes.
  - Transformation into required format: Once you have the data, you can save it into your required format, like CSV.
- Given below are the links to some public datasets. You may explore these open sources to get the data:
  - GitHub: [Awesome public data sets](https://github.com/awesomedata/awesome-public-datasets]), [Github data sets](https://github.com/datameet)
  - Open government data set: [Open Government data](https://data.gov.in/).
  - Kaggle website link: [Kaggle Website](https://www.kaggle.com/datasets)
  - UCI repository of machine learning: [UCI machine learning data set repository](https://archive.ics.uci.edu/ml/index.php).

Data Cleaning
--
- Data Types
- Fixing Rows and Columns
- Impute/Remove Missing Values: MCAR, MAR & MNAR
- Handling Outliers: Univariate and Multivariate outliers; Imputation, Deletion, Binning of values, Capping outliers
- Standardising Values: Standardise units, Scale values if required, Standardise precision, Standardise case, Standardise format, remove extra characters
- Fixing Invalid Values and Filter Data: Incorrect datatypes, Fix incorrect structure etc; Filter rows, columns, Aggregate data, deduplicate data

Univariate Analysis
--
- Categorical unordered univariate analysis: Unordered variables are those variables that do not contain any notion of ordering, for example, increasing or decreasing order. These are just various types of any category. The examples can be job types, marital status, blood groups, etc.
- Categorical ordered univariate analysis: Ordered variables are those that have some kind of ordering in them, like high-low, fail-success, yes or no. Examples can be education level, salary group like high or low, gradings in any exam, etc.
- Numerical variable univariate analysis: Numerical variables can be classified into continuous and discrete type. To analyse numerical variables, you need to have an understanding of statistic metrics like mean, median, mode, quantiles, and box plots, etc. It is important to understand that numerical variable univariate analysis is nothing but what we have done earlier, i.e., the treatment of missing values and handling outliers. The crux of univariate analysis lies in the single variable analysis, which is covered in the process of cleaning the dataset.
- The transition of a numerical variable into a categorical variable: This is an important aspect that you need to think about before performing univariate analysis. Sometimes, it is essential to just convert numerical variables into categorical ones, through a process which is called 'binning'.

Bivariate and Multivariate Analysis
--
- Analysis between two numerical variables: The most important thing to remember is that correlation and scatter plots are the best methods to perform an analysis on numerical variables. Correlation coefficient indicates how much two numerical variables are correlated linearly. And scatter plots offer the exact visualisation between the numerical variables.
- Analysis between numerical and categorical variables: This gives an idea about the variation of a particular numerical variable with respect to different categories of a categorical variable. Boxplot is the best way to look at a numerical variable with respect to a categorical variable. However, boxplots may sometimes not be useful because of the huge difference between the maximum and minimum values in the data set, or due to the higher concentration of data in the numerical variable. Another approach could be to look into the mean/median or quartiles, which are a more efficient way to deal with a numerical variable when combined with a categorical variable.
- Correlation vs causation: This is a very important concept of data anaylsis, which states that correlation is not always related to causation. Although there may be a very high correlation between variables, there may be no causation at all.
- Analysis between two categorical variables: A bar graph is the best approach to analysing two categorical variables.
- Multivariate analysis: Multivariate analysis yields very specific information about a data set. It basically involves the analysis of more than two variables at a time. For instance, heat maps are the best way to look at three variables at a time. In multivariate analysis, it is essential to look into the data by grouping the variables and infer decisions from it.

EDA Interview Practice
--
- Additional Links
  - [Missing Values](https://medium.com/@raoufkeskes/missing-data-its-types-and-statistical-methods-to-deal-with-it-5cf8b71a443f)
  - [Outliers](https://towardsdatascience.com/ways-to-detect-and-remove-the-outliers-404d16608dba)
  -  [Correlation](https://www.tylervigen.com/spurious-correlations)
  -  [Correlation vs Causation](https://medium.com/@seema.singh/why-correlation-does-not-imply-causation-5b99790df07e)
  -  [Establishing cause and effect](https://www.statisticssolutions.com/dissertation-resources/research-designs/establishing-cause-and-effect/)

