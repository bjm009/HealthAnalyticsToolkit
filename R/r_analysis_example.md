# Investigating Data Imported from File
The file used in this example can be found [here](https://healthdata.gov/dataset/COVID-19-State-and-County-Policy-Orders/gyqz-9u7n). The information in the file is regularly updated, so do not be concerned if your numerical values are slightly different when following along. Differences can be caused by addition of new data. 


## Watch this video to see the basics in action!
<iframe width="560" height="315" src="https://www.youtube.com/embed/0RZ_9qwScs8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Importing the data

```r
mydata <- read.csv("C:/Users/baile/Desktop/MBID/CS_6440/Practicum/COVID-19_Reported_Patient_Impact_and_Hospital_Capacity_by_State_Timeseries.csv")
```
This will read the data from the file and store it in the variable `mydata`. But what is my data? That we can figure out by using `class()`.

```r
class(mydata)
```

    "data.frame"


`mydata` is a `data.frame`. You may have worked with them before in other languages such as Python. If we want to look at this `data.frame`, we can use `View()`.

```r
View(mydata)
```

View invokes a data viewer that is in a spreadsheet style, allowing us to look at matrix-like R objects. 

## Accessing data like a list and working with the data

Now that we have the data imported and we know the format, we can start working with the data.frame to do an analysis!!

To get specific information out of a `data.frame`, we use \$. See the example below, where I take the `critical_staffing_shortage_anticipated_within_week_yes` column and store it in the variable `crit_short`. This then allows us to do a variety of analyses on the `crit_short` variable, such as mean, standard deviation, range, etc. 

```r
crit_short <- mydata$critical_staffing_shortage_anticipated_within_week_yes
mean(crit_short)
sd(crit_short)
```

Based on the results from the above code, the average number of hospitals reporting a critical staffing shortage anticipated within the week across all states and dates is  **13.27 +/- 24.24 (mean +/- std)**. 

We can also look at other items regarding this data, such as the range. 

```r
range(crit_short)
``` 

```
0 201
```

This tells us that the number of hospitals reporting critical staffing shortages across all states and dates is between 0 and 201. 

Another thing we might want to look at, is how many times each of the states appears in the spreadsheet. To do this, we can use `table()` to get a count. 

```r
table(mydata$state)
```
     AK  AL  AR  AZ  CA  CO  CT  DC  DE  FL  GA  HI  IA  ID 
     384 466 401 405 411 393 389 379 380 395 406 466 406 394 
     IL  IN  KS  KY  LA  MA  MD  ME  MI  MN  MO  MS  MT  NC 
    418 466 435 406 411 380 406 406 406 466 413 417 466 466 
     ND  NE  NH  NJ  NM  NV  NY  OH  OK  OR  PA  PR  RI  SC 
    406 406 380 406 393 448 393 406 406 412 406 411 404 405 
     SD  TN  TX  UT  VA  VI  VT  WA  WI  WV  WY 
    382 393 466 387 405 368 390 408 406 416 406 
    
You can also store this table as a variable and do further analysis on it. 

## Data Summary

One of the ways to do a quick analysis of all the columns and see general information is to use `summary()`.

```r
summary(mydata)
```

       state               date          
    Length:21746       Length:21746      
    Class :character   Class :character  
    Mode  :character   Mode  :character  
                                      
                                      
                                      
                                      
    critical_staffing_shortage_today_yes
    Min.   :  0.00                      
    1st Qu.:  0.00                      
    Median :  3.00                      
    Mean   : 11.08                      
    3rd Qu.: 14.00                      
    Max.   :188.00                      
                                     
    critical_staffing_shortage_today_no
    Min.   :  0.00                     
    1st Qu.:  0.00                     
    Median : 28.00                     
    Mean   : 53.52                     
    3rd Qu.: 84.00                     
    Max.   :490.00                     
                                    
    critical_staffing_shortage_today_not_reported
    Min.   :  0.00                               
    1st Qu.:  2.00                               
    Median :  8.00                               
    Mean   : 33.41                               
    3rd Qu.: 37.00                               
    Max.   :492.00                               
                                              
    critical_staffing_shortage_anticipated_within_week_yes
    Min.   :  0.00                                        
    1st Qu.:  0.00                                        
    Median :  4.00                                        
    Mean   : 13.23                                        
    3rd Qu.: 18.00                                        
    Max.   :201.00                                        
                                                       
    critical_staffing_shortage_anticipated_within_week_no
    Min.   :  0.0                                        
    1st Qu.:  0.0                                        
    Median : 29.0                                        
    Mean   : 51.5                                        
    3rd Qu.: 80.0                                        
    Max.   :473.0                                        
                                                      
    critical_staffing_shortage_anticipated_within_week_not_reported
    Min.   :  0.00                                                 
    1st Qu.:  2.00                                                 
    Median :  8.00                                                 
    Mean   : 33.27                                                 
    3rd Qu.: 36.00                                                 
    Max.   :492.00                                                 

    ..........

Here we get a look at each of the columns, which can be very useful in your initial analysis! 

