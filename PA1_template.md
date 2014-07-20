PA1 Assignment
========================================================


```r
  setwd("/Users/chris/Documents")
  data <- read.csv("/Users/chris/Documents/activity.csv")
  dataframe <- data.frame(data)
  df1 <- na.omit(dataframe)
  df <- subset(df1, select = c(date,steps))
  rownames(df) <- NULL
```

```r
  install.packages("ggplot2")
```

```
## Error: trying to use CRAN without setting a mirror
```

```r
  library(ggplot2)
  library(scales)
  ggplot(df, aes(x=steps)) + geom_histogram()
```

```
## stat_bin: binwidth defaulted to range/30. Use 'binwidth = x' to adjust this.
```

![plot of chunk Mean](figure/Mean.png) 

```r
  mean <- mean(df[[2]])
  median <- median(df[[2]])
  print1 <- paste("The mean number of steps is: ", mean, sep="")
  print2 <- paste("The median number of steps is: ", median, sep="")
  print1
```

```
## [1] "The mean number of steps is: 37.3825995807128"
```

```r
  print2
```

```
## [1] "The median number of steps is: 0"
```


```r
  maximum <- max(df$steps)
  max -> dataframe[df$steps==max,3]
```

```
## Error: comparison (1) is possible only for atomic and list types
```

```r
  print3 <- paste("The 5-minute interval that contains the maximum number of steps is: ", max, sep="")
```

```
## Error: cannot coerce type 'builtin' to vector of type 'character'
```

```r
  print3
```

```
## Error: object 'print3' not found
```


```r
  sum <- sum(is.na(dataframe$steps))
  print4 <- paste("The total number of missing values in tha data set is: ", sum, sep="")
  print4
```

```
## [1] "The total number of missing values in tha data set is: 2304"
```


```r
  print5 <- "To imput missing data my strategy would be to find the mean of that particular interval and then in a loop find each NA value and replace it with the corresponding mean value in a new dataset."
  print5
```

```
## [1] "To imput missing data my strategy would be to find the mean of that particular interval and then in a loop find each NA value and replace it with the corresponding mean value in a new dataset."
```


