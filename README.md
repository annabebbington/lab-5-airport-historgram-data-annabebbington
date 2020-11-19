# Airport Histogram Data

This script explores airport and flight data from the [OpenFlights Project](https://openflights.org/data.html) through 4 coding challenge. All of the data is in csv format. It was uplaoded to Google Colab and read using `csv.reader().`

### Challenge 1
This script uses a for loop to iterate through the airports data, and prints all the airports located in the United Kingdom. 

### Challenge 2
This script creates 2 dictionaries from the airports data. The first dictionary (`DictLat`) includes the aiport ID number and the latitude of the airport, the second(`DictLon`) includes the aiport ID number and the longitude. The script does this my iterating through the airports data to first create three lists (`ListID, ListLat, ListLon`), and then uses `dict(zip())` to zip together the aiport ID and Lat/Lon to create key value pairs in the dictionary. 

### Challenge 3
This script uses the routes data to create a list of distances of the flights. This script imports the geo_distance.py file which includes the function geo_distance which can be used to measure 'great circle distance'. A for loop iterates through the the routes data, and accesses the values included in `DictLat` and `DictLon` based on Airport ID. The script identifies the latitudes and longitudes associated with the departure and destination airports, and those values are converted to floats and input into the `geo_distance` function. The values calculated by `geo_distance()` are added to the `distances` list. 

This script ONLY calculates the distances of flights that are also in `DictLat` and `DictLon`. 

### Challenge 4
This short script creates a histogram based on the data in the `distances` list. The histogram uses the library `numpy` and `matplotlib.pyplot`

![](https://github.com/IDCE-MSGIS/lab-5-airport-historgram-data-annabebbington/blob/main/Flight%20Distance%20Histogram.png)

One issue I ran into in challenge 4 is that above the histogram I get a text output `Text(0.5, 1.0, 'Flight Distance Frequency')`. The last part of this message changes, depending what the last line of code is. 
