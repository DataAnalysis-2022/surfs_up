# surfs_up



## Background

We will provide more information about temperature trends before the owner decides to open the surf shop. Specifically, the temperature data for the months of June and December in Oahu is the most critical information in order to determine if the surf and ice cream shop business is sustainable year-round.



### Results

 The Summary Statistics for June and December are shown below:

![image-20220807181422307](Resources\image-20220807181422307.png)                                      ![image-20220807181508852](Resources\image-20220807181508852.png)

​			June Statistics															December Statistics



We can see that there are three key differences in weather between June and December:

- The mean temperature in June is 74.9 degree and 71.0 degree in December;
- The minimum temperature in June is 64.0 degree and 56.0 degree in December;
- The maximum temperature in June is 85 degree and 83 degree in December



### Summary:

From the data we gathered, there is some degrees of temperature variation in June and December.  So the surf shop and ice cream store will be sustainable in Oahu.

We can also query for the precipitation for June and December as the followings:

```python
prcp_June = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()
```



```python
prcp_Dec = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
```

