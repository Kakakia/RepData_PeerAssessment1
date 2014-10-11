Reproducible Research: Peer Assessment 1
========================================================


## Loading and preprocessing the data


```r
data <- read.csv("activity.csv")
```

```
## Warning: cannot open file 'activity.csv': No such file or directory
```

```
## Error: cannot open the connection
```

```r
summary(data)
```

```
## Error: object of type 'closure' is not subsettable
```
Transform the date variable into Date format

```r
data$Date<-as.Date(data$date)
```

```
## Error: object of type 'closure' is not subsettable
```



## What is mean total number of steps taken per day?

Calculate the total number of steps taken each day

```r
steps.per.day<-tapply(data$steps, data$Date, FUN=sum)
```

```
## Error: object of type 'closure' is not subsettable
```

Histogram of the total number of steps taken each day

```r
hist(steps.per.day, breaks =15, main = "Histogram of Steps Taken per Day", xlab="total steps per day", col="salmon")
```

```
## Error: object 'steps.per.day' not found
```

Calculate and report the mean and median total number of steps taken per day

```r
steps.mean<-mean(steps.per.day, na.rm=TRUE)
```

```
## Error: object 'steps.per.day' not found
```

```r
steps.median<-median(steps.per.day, na.rm=TRUE)
```

```
## Error: object 'steps.per.day' not found
```















