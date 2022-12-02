# ESP32_ThingSpeak_Database_Proj
This project contains three files. 
1) The DHTToWebServer.cpp file.
  - This file is running directly on the ESP8266 device. 
  - We provide this file with a path to our POST php file via a POST HTTP request ex: servername= "http://___0.0.21/post-esp-data.php"
  - This POST request will also contain an API Key for communicating with the php file for Posting the data. 
  - The file will connect to local wifi, read the DHT sensors output, string together an HTTP POST requests with the DHT data and API Key, and then POST the data to the next file. 
  
2) The post-esp-data.php file. 
  - This file is run on the local web server using XAMPP and Apache. 
  - We provide this fle with our Database information and the API Key previously used in the Arduino's Code. 
  - This file reads the POST HTTP request from the esp, connects to our database, then inserts data into the database.
  
3) The temp.php file. 
  - This file is for displaying the results of the database. 
