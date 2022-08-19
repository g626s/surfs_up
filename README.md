# Surfs_Up
# Overview of the analysis:
In this project, our objective consisted of using tools such as Jupyter Notebook, SQLite and SQLAlchemy in analyzing weather data as well as temperature trends in the desired area of Oahu, Hawaii to help give insight and recommendations to support our client's surf and ice-cream shop business. Our client reviewed our previous analysis and has requested more information about temperature trends before opening the surf shop. Specifically, our client wants temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round instead of being a season staple of operation. In addition, we also used the tool Flask that allowed us to create a Python application and then share the results of those applications with the board of investors others via a webpage, making it a powerful tool for our project's data analysis and visualization.

# Resources:
Data resources:
- hawaii.sqlite

Sotfware application and tools:
- Python
- Jupypter Notebook
- SQLite
- SQLAlchemy 
- Flask 

# Results: 
For the results, methodology, and application used for our project, we used Python, Pandas functions and methods, and SQLAlchemy, to filter the date column of the Measurements table in the hawaii.sqlite database to retrieve all the temperatures for the desirable months of June and December. We then converted those temperatures to a list, created a DataFrame from the list, and generate the summary statistics of those two months to display the statstical results.
- ![Screen Shot 2022-08-18 at 8 38 46 AM](https://user-images.githubusercontent.com/107281474/185442354-1539b159-e560-41da-bddd-34d2b94221eb.png) 
- ![Screen Shot 2022-08-18 at 8 39 17 AM](https://user-images.githubusercontent.com/107281474/185442430-f1e443f5-6874-4dee-87af-2ab697bb1d40.png)
- ![Screen Shot 2022-08-18 at 8 39 00 AM](https://user-images.githubusercontent.com/107281474/185442972-20cf8df2-667b-4d61-a7c0-b25047de2578.png)
- ![Screen Shot 2022-08-18 at 8 39 29 AM](https://user-images.githubusercontent.com/107281474/185443028-fc59360f-b513-42f2-8741-39b8cb601d1e.png)

From the statistical results of the temperature of the the selected months of June and December, both are considered to be desirable weather conditions from the mean of June being 75°F and December being 71°F. Even though June has a higher count in recorded temperatures than December, from the summary statistics it can be inferred that June has a more evenly normal distribution indicated by the standard deviation compared to December's standard deviation. Lastly, comparing the min and max as well as quartile range between the two months, December has a wider range that could potentially the operation of the business whereas June has more consistent temperature weather.  

# Summary:
From the analysis and recommendations to our client, even though from the results that December appears to flucuate more compared to June, December would still provide ideal weather and temperature conditions for the business and only differ by nearly 5 degrees from the mean. In addition we provided two additional queries with the pd.concat function:
    
    additional_query_stats = pd.concat([june_df.describe(), dec_df.describe()],
         axis=1, join='inner')
         
    additional_query_temps = pd.concat([june_df, dec_df],
         axis=1, join='inner')
         
 that combined the two temp and summary statistics that can be visually put together to clearly see and indicate key differences while also at the same time positioning future further analysis to potential new locations being opened within the region. Additionally these two queries can be also be merged with the recorded stations to help determine geographically where in the region to build future locations. Another consideration for analysis in correlation to the geographical surroundings is optimal wind condition and earthquake patterns that in turn can affect wave activity. 

- ![Screen Shot 2022-08-18 at 8 39 41 AM](https://user-images.githubusercontent.com/107281474/185519298-c5a4ce04-b83e-42f9-80c1-1d5401488a95.png)
- ![Screen Shot 2022-08-18 at 8 39 52 AM](https://user-images.githubusercontent.com/107281474/185519315-adc6777b-a30b-456a-9102-b7100ae0694c.png)
