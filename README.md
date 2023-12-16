**Internet of Cows**

**Credentials**

InfluxDb:	
	- username: weot
	- password: internetofcows

Grafana:	
	- username: admin
 	- password: admin
  
InfluxDb token for Node-RED:
tfg7A3pr7Y2obvYNsSikeYXtHJk9R3z_yvSRm6os_T_6WaXziGDRiEPY4vk9xBy6eA7ErRX6hjRM49Y8rAjifQ==

**Steps for setting up the system**
1) Clone the repository: https://github.com/hieuhuynh1752/WEoT-Internet-Of-Cows/tree/main
2) docker compose build
3) docker compose up
4) Open Node-RED on http://localhost:1880
5) Open InfluxDb on http://localhost:8086 
  5.1) Login with the credentials
6) Open Grafana on http://localhost:3000
  6.1) Login with the credentials
7) Open Wokwi project on [Cow 1](https://wokwi.com/projects/384205732803068929), [Cow 2](https://wokwi.com/projects/384255363186361345), [Cow 5](https://wokwi.com/projects/384255396139962369)
  7.1) Start the device simulation by pressing the play button ▶️
  7.2) The device will be simulating only if it’s on the active screen (if you have another tab open it will go idle, and continue when you are back at it, you can counter this by splitting your browsers screen and looking at the multiple tabs at the same time)
  7.3) Wait for the device to connect to Wifi and MQTT server
  7.4) You can adjust the sensor values by clicking on each of the sensors
    7.4.1) Remember that the LED is only for showing the beats (you can influence beats through Node-RED’s True/False flow)
8) Watch changes happening in your InfluxDb and Grafana Dashboards
9) Play with True/False flow on Node-RED to make cow start or stop running  
    NOTE: This is simulation of cow’s will, so the idea is that the cow decided to start doing a demanding activity which will increase its heartbeats in return. So don’t expect to get an increase in speed measurements, but only in heartbeats/pulse. Speed is collected through sensor, so the values are not simulated but the idea is that they would be collected from the reality. 
