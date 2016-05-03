# Working with databases in R



The dplyr package, which is one of my favorite R packages, works with in-memory data and with data stored in databases. In this post, I will share my experience on using dplyr to work with databases.

Using dplyr with databases has huge advantage when our data is big where loading it to R is impossible or slows down our analytics. If our data resides in a database, rather than loading the whole data to R, we can work with subsets or aggregates of the data that we are interested in. Further, if we have many data files, putting our data in a database, rather than in csv or other format, has better security and is easier to manage.

dplyr is a really powerful package for data manipulation, data exploration and feature engineering in R and if you do not know SQL, it provides the ability to work with databases just within R. Further, dplyr functions are easy to write and read. dplyr considers database tables as data frames and it uses lazy evaluation (it delays the actual operation until necessary and loads data onto R from the database only when we need it) and for someone who knows Spark, the processes and even the functions have similarities.

dplyr supports a couple of databases such as sqlite, mysql and postgresql. In this post, we will see how to work with sqlite database. You can get more information from the dplyr database vignette [here](https://cran.r-project.org/web/packages/dplyr/vignettes/databases.html).

When people take drugs, if they experience any adverse events, they can report it to the FDA. These data are in public domain and anyone can download them and analyze them. In this post, we will download demography information of the patients, drug they used and for what indication they used it, reaction and outcome. Then, we will put all the datasets in a database and use dplyr to work with the databases.

You can read more about the advesre events data in my previous post [here](http://datascience-enthusiast.com/R/SQL_R_select.html).

You can simply run the code below and it will download the adverse events data and create one large dataset, for each category, by merging the various datasets. For demonstration purposes, let's use the adverse event reports from 2013-2015. The adverse events are released in quarterly data files (a single data file for every category every three months).

You can get the full post [here](http://datascience-enthusiast.com/R/database_R.html).
