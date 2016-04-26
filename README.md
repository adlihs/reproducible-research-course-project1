# Loading and preprocessing the data

act <- read.csv("activity.csv")

str(act)

act <- read.csv("activity.csv",colClasses=c("numeric","Date","numeric"))

str(act)

# What is mean total number of steps taken per day?

sum_by_date <- tapply(act$steps,act$date,sum,na.rm=TRUE)

hist(sum_by_date,col=heat.colors(8),xlab="Total Steps by Date",main="Histogram of Total Steps by Date")

 ![img] [https://github.com/adlihs/reproducible-research-course-project1/blob/master/graph%201.png]
