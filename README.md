
Indoor Air Quality Monitoring System Using ESP32
This project is an indoor air quality monitoring system built using an ESP32 microcontroller, multiple environmental sensors, and the Blynk IoT platform for remote data monitoring.

  //Features
-ESP32-Based System: Handles data processing and Wi-Fi connectivity for remote access.
-Integrated Sensors:
+AHT20: Measures temperature and humidity.
+MQ135: Detects air quality, including gases like CO2, NH3, and VOCs.
+ZH03B PM Sensor: Monitors PM2.5 particulate matter.
+ML8511: Measures UV intensity.
  
  //Blynk IoT Platform:
-Displays real-time data on a customizable dashboard.
-Monitors air quality, oxygen levels, temperature, humidity, and risk notifications.
-OpenWeatherMap API: Fetches outdoor UV data to enhance context and accuracy.
-WiFiManager: Automatically connects to Wi-Fi or creates an AP if no connection is found.
   
   //Code Overview
readSensorData(): Collects data from connected sensors.
pushtoBlynk(): Sends processed data to the Blynk dashboard.
GetAPI(): Retrieves UV index data from OpenWeatherMap for comparison with indoor conditions.
   
   //Setup Instructions
Hardware Setup:
Connect the sensors to the ESP32 according to the specified pin configurations.
Software Requirements:
Arduino Libraries: Install the following libraries:
WiFi, WiFiManager, BlynkSimpleEsp32, MQ135, AHT20, Arduino_JSON
Blynk Setup: Create a Blynk project and configure virtual pins (V0 - V6) for data display.


   //Configuration:
After uploading the code to your ESP32, the device will automatically connect to Wi-Fi (or create an access point if no saved networks are found) and begin monitoring indoor air quality. Data will be sent to Blynk and updated in real-time, with additional notifications for any detected health risks.
