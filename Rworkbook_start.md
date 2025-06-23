# Installing R studio or using Co-lab or terminal

In colab click on the downwards arrow and select change runtype:

![image](https://github.com/user-attachments/assets/880d3002-6298-4a4b-92bf-3b174ae65b5b)

Select R
ls() to see a list of the variables in your workspace

rm(list=ls()) to clear your workspace.


If you have a conflict it is a good idea to specify what package you are taking the function from
stats::filter(my_ts_object, filter = my_filter_vector)
dplyr::filter(my_df, column == "value")


## dplr and tidyverse
```
install.packages('tidyverse')
library(tidyverse)
library(dplyr)

data <- read_csv("/content/inca_haemonc_250131_2.csv")
head(data)
```
tibbles
