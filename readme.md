# Arduino Interface with FT205EV Ultrasonic Anemometer
​
The FT205EV is the first in a new generation of lightweight ultrasonic wind sensors. It is low weight(100g) and a wind speed range up to 75m/s. It has a graphite and nylon composite body. The light weight of the FT205EV together with the proven FT Acu-Res technology make it ideal for use on aerial drones and other weight critical applications. The FT205EV allows configurable RS422 (full-duplex), RS485 (half-duplex) or buffered UART (full-duplex) communication outputs.  
​
The following instructions guide the reader to setting up the circuit connections between a Raspberry Pi, Arduino, and a FT205EV ultrasonic anemometer. 
​
## Hardware Requirements
​
- FT205EV Ultrasonic Anemometer
- Ardunio Uno
- Raspberry Pi
- Power supply 6-30VDC
​
​
​
## Circuit Diagram
​
The circuit diagram to connect the Arduino with the ultrasonic anemometer is shown here
​
![1576040723463](C:\Users\deepa\AppData\Roaming\Typora\typora-user-images\1576040723463.png)
​
The circuit diagram to connect the RaspberryPi to the arduino and anemometer is as follows
​
![1576040792218](C:\Users\deepa\AppData\Roaming\Typora\typora-user-images\1576040792218.png)
​
​
​
## Getting Started
​
Setup the circuit according to the given circuit diagram. Compile and upload the Arduino file SoftwareSerial_windSensor.ino  under the folder UART_to_WindSensor, to the Arduino. This example is used to test that the ultrasonic anemometer is functioning and the Arduino is able to read the data from the sensor. 
​
The Arduino is used to send commands to the sensor using UART interface. The data sent by the sensor is displayed on the serial monitor on the computer. We make pins 10 and 11 software serial pins to communicate with the sensor since the Arduino serial pins 0 and 1 (hardware serial) are used to display data on the serial monitor on the computer. We give enough delay between the commands since the sensor takes minimum 400ms to process a command. The Arduino sends a command to the sensor to set the communication interface to UART and then we send a Query to check if the communication interface has been set. We then send a query to the sensor for the wind speed and direction every 1 second. The sensor responds with ASCII messages in the format as discussed in the Tutorial-WindSensor-Arduino.pdf.   
​
### Break down into end to end tests
​
Explain what these tests test and why
​
```
​
```
​
### And coding style tests
​
Explain what these tests test and why
​
```
Give an example
```
​
## Deployment
​
Add additional notes about how to deploy this on a live system
​
## Built With
​
* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds
​
## Contributing
​
Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.
​
## Versioning
​
We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 
​
## Authors
​
* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)
​
See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.
​
## License
​
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
​
## Acknowledgments
​
* Hat tip to anyone whose code was used
* Inspiration
* etc
​
