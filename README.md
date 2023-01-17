# New-York-Citibike Dataset
Using JOIN in SQL to query a Citibike station table and trips table
<br></br><br>BigQuery Public Dataset: 
<ul>bigquery-public-data.new_york_citibike.citibike_stations</ul>
<ul>bigquery-public-data.new_york_citibike.citibike_trips</br></ul>
<pre>SELECT name, MAX(tripduration) AS longest_triplength, usertype, gender, birth_year, is_returning AS bike_return, num_bikes_available
FROM `bigquery-public-data.new_york_citibike.citibike_stations` stations
JOIN `bigquery-public-data.new_york_citibike.citibike_trips` trips
ON stations.station_id = trips.start_station_id
GROUP BY name, tripduration, usertype, gender, birth_year, bike_return, num_bikes_available
ORDER BY tripduration DESC 
LIMIT 10
</pre>

<h2>Results</h2>
<table>
  <tr>
    <th>Row</th>
    <th>name</th>
    <th>longest_tripduration</th>
    <th>usertype</th>
    <th>gender</th>
    <th>birth_year</th>
    <th>bike_return</th>
    <th>num_bikes_available</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Hope St & Union Ave</td>
    <td>19510049</td>
    <td>Customer</td>
    <td>male</td>
    <td>1953</td>
    <td>true</td>
    <td>6</td>
   </tr>
   
   <td>2</td>
   <td>Grand Army Plaza & Plaza St West</td>
    <td>15962256</td>
    <td>Customer</td>
    <td>male</td>
    <td>1988</td>
    <td>true</td>
    <td>1</td>
   </tr>
   
   <td>3</td>
   <td>Kingston Ave & Herkimer St</td>
    <td>15020934</td>
    <td>Customer</td>
    <td>female</td>
    <td>1984</td>
    <td>true</td>
    <td>0</td>
   </tr>
   
   <td>4</td>
   <td>Fulton St & Utica Ave</td>
    <td>13931824</td>
    <td>Customer</td>
    <td>male</td>
    <td>1988</td>
    <td>true</td>
    <td>1</td>
   </tr>
   
   <td>5</td>
   <td>Fulton St & Utica Ave</td>
    <td>13586276</td>
    <td>Subscriber</td>
    <td>female</td>
    <td>1993</td>
    <td>true</td>
    <td>1</td>
   </tr>
   
   <td>6</td>
   <td>Cathedral Pkwy & Broadway</td>
    <td>12479323</td>
    <td>Customer</td>
    <td>female</td>
    <td>1972</td>
    <td>true</td>
    <td>1</td>
   </tr>
   
   <td>7</td>
   <td>Myrtle Ave & Lewis Ave</td>
    <td>11749576</td>
    <td>Customer</td>
    <td>unknown</td>
    <td>1969</td>
    <td>true</td>
    <td>3</td>
   </tr>
   
   <td>8</td>
   <td>Carlton Ave & Dean St</td>
    <td>11699746</td>
    <td>Customer</td>
    <td>unknown</td>
    <td>1969</td>
    <td>true</td>
    <td>17</td>
   </tr>
   
   <td>9</td>
   <td>FDR Drive & E 35 St</td>
    <td>11138807</td>
    <td>Customer</td>
    <td>unknown</td>
    <td>1969</td>
    <td>true</td>
    <td>52</td>
   </tr>
   
   <td>10</td>
   <td>Clinton Ave & Flushing Ave</td>
    <td>10283682</td>
    <td>Customer</td>
    <td>unknown</td>
    <td>1969</td>
    <td>true</td>
    <td>18</td>
   </tr>
</table>
