# Installing R studio or using Co-lab or terminal

In colab click on the downwards arrow and select change runtype:

![image](https://github.com/user-attachments/assets/880d3002-6298-4a4b-92bf-3b174ae65b5b)

Select R
ls() to see a list of the variables in your workspace

rm(list=ls()) to clear your workspace.


If you have a conflict it is a good idea to specify what package you are taking the function from
stats::filter(my_ts_object, filter = my_filter_vector)
dplyr::filter(my_df, column == "value")

To get more information in R
```
?mad
example(mad)
methods(class="ExpressionSet")
methods(class="lm")

```
“Vignettes” are documents which accompany R packages and are required for every Bioconductor package. They typically show an example workflow of the functions of the package using “chunks” of code with descriptive text, exactly as the document you are currently reading.


## dplr and tidyverse
```
install.packages('tidyverse')
library(tidyverse)
library(dplyr)

data <- read_csv("/content/inca_haemonc_250131_2.csv")
head(data)
```
tibbles
In dplyr we use %>% to denote a pipe and can use it to perform consecutive tasks


 To obtain a numeric vector with dplyr, we can apply the unlist function which turns lists, such as data.frames, into numeric vectors:
chowVals <- filter(dat, Diet=="chow") %>% select(Bodyweight) %>% unlist
class( chowVals )

To do this in R without dplyr the code is the following:

chowVals <- dat[ dat$Diet=="chow", colnames(dat)=="Bodyweight"]


## Some basic exploratory analysis:

## Introduction to Bioconductor:

This command installs the core Bioconductor packages:
```
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
```

And then we can load the appropriate librarie


