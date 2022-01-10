# PyBer_Analysis

# PyBer with Matplotlib

## Overview of Project

### Purpose

In this project we are working for a company called PyBer as a data analyist. We were given a large amount of ride data to analyze to help PyBer understand what they can do to improve the availability and affordability to under served neighborhoods. To do this we first need to get use functions like groupby to sort the data by city type, and get it into a more readable format. Then create visualization in the form of a chart so that the data is easily presentable.

## Results

To reach the results of this analysis we had to start by getting data for each city type. This was done by using the groupby function with the condition "type" to get our data categorized based on city type. Then we needed to condition the groupby function to get certain data. To get the total rides for each city the count function was used on the groupby function with the condition of 'ride_id'. This got the results below:

![image](https://user-images.githubusercontent.com/92827264/148708672-2ac26bfb-8418-4cc8-8e36-0b4ed48593ca.png)

Then I needed to get the driver count for each city type, which I did with using the sum function.

![image](https://user-images.githubusercontent.com/92827264/148708702-84ccb87b-f175-4a1d-aee0-3aca709dbaee.png)

Last piece of data that I needed from groupby function was total fares for each city type. The sum function was also used to get this data.

![image](https://user-images.githubusercontent.com/92827264/148708823-2d830528-53ff-48b3-b67f-f5eff08259cc.png)

Afer this data was collected I used math functions to get averages of fares based on driver and ride.

![image](https://user-images.githubusercontent.com/92827264/148708890-aede8cd8-c252-4049-9ba0-3bde267b3a09.png)

I then created a dataframe using the data gathered above and formated it.

![image](https://user-images.githubusercontent.com/92827264/148708948-93d32cb8-91c6-479c-b2ba-e8a32c1174f5.png)
![image](https://user-images.githubusercontent.com/92827264/148708961-d900b59e-4043-4462-9438-5d3279cb3943.png)

From this data you can see that the drivers in the rural areas are getting a lot more than the urban areas. This is because due to the lack of drivers in the rural areas they can charge more for the rides.

I then needed to get total weekly fare for each city type. This was done by using group be on the merged data by 'date' and 'type', and using the sum function on 'fare'.

![image](https://user-images.githubusercontent.com/92827264/148710057-5b828d8f-8e82-4608-b4c8-61e79607d5aa.png)

I then reset the index and used the pivot function on the data to create a table of dates with fare amounts per city. I then narrowed down the results by using the loc function to return rides from January thru April.

![image](https://user-images.githubusercontent.com/92827264/148710237-e60eb882-99ba-41fd-8a7b-e5e737b22cae.png)

I then had to make the index of the dataframe to a datetime datatype. This is so that I can use the resample function and sum up the dates into weeks.

![image](https://user-images.githubusercontent.com/92827264/148710323-ff0a29fe-fde5-4986-ad61-d2cf4f95e11d.png)

I then plot this data so we can see the breakdown of the fares by city type.

![image](https://user-images.githubusercontent.com/92827264/148710374-d961a6e3-757f-4374-b724-9512e55fcb1e.png)

As you can see the rural areas do not bring in more than $500 a week from January to May. The rural areas need to get increased access.

## Summary

One suggestion I would have to the CEO is to create an inscentive to the rural drives to reduce the amount they charge per ride so that would charge less. This would make it more affordable to use PyBer in the rural areas.
