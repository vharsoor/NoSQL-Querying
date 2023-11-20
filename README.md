**# NoSQL-Querying**

Performing NoSQL queries in Python on a key-value pair database within a Jupyter Notebook environment.

In this project, I had to implement 2 functions after reading a sample.db.

A. **FindBusinessBasedOnCity(cityToSearch, saveLocation1, collection)** – This function searches the ‘collection’ given to find all the business present in the city provided in ‘cityToSearch’ and save it to ‘saveLocation1’. For each business you found, you should store the name, full address, city, and state of the business in the following format. Each line of the saved file will contain: Name$FullAddress$City$State. ($ is the separator and must be present.)

B. **FindBusinessBasedOnLocation(categoriesToSearch, myLocation, maxDistance, saveLocation2, collection)** – This function searches the ‘collection’ given to find the name of all the businesses present in the ‘maxDistance’ from the given ‘myLocation’ (please use the distance algorithm given below) and save them to ‘saveLocation2’. Each line of the output file will contain the name of the business only.

I was also given the distance algorithm/formula to calculate the distance between 2 spatial co-ordinates(latitude,latitude) as:<br/>
DistanceFunction(lat2, lon2, lat1, lon1):
var R = 3959; // miles <br/>
var φ1 = lat1.toRadians(); <br/>
var φ2 = lat2.toRadians(); <br/>
var Δφ = (lat2-lat1).toRadians(); <br/>
var Δλ = (lon2-lon1).toRadians(); <br/>
var a = Math.sin(Δφ/2) * Math.sin(Δφ/2) + Math.cos(φ1) * Math.cos(φ2) * Math.sin(Δλ/2) * Math.sin(Δλ/2); <br/>
var c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1-a));<br/>
var d = R * c; <br/>
