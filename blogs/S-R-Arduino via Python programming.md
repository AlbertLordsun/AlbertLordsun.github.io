---
layout: page
title: Arduino via Python programming
---

---
## Hardware system design
   Designing a diagram for your software flow helps you to write the program and also assists you in identifying actions and events for the project. The process of hardware system design includes circuit connections, schematic design, simulation, verification, and testing.  
1. Schematic design  
    ***software:***    
    1) 立创EDA  
    2) Altium Designer  
    3) Fritzing    
2. Simulation and verification  
    ***software:***  
    1) TinkerCAD;(programming is one advantage, we can directly see the simulation results on the website; the drawback is few hardware lists)   
    2) Fritzing (unprogrammable, while with many hardwares)  
3. Circuit connection   
4. Test  

---
## Software and programming  
   The part can be analyzed from two levels: 1) components-to-Arduino; 2) Arduino-to-Python. The first part includes digital (some support PWM) or analog pins, **I2C and serial peripheral interface (SPI)** communication. The second part includes the communication protocols between Python and Arduino, like Firmata and serial one.  
### *Arduino IDE (traditional, lack the extensiveness)*
   (The firmata protocol provides full access of the Arduino board to the software and host computer.)  
   Arduino IDE mainly uses C/C++ language in the Arduino sketch. The sketch includes the setup() function and loop() function. Users can design the custom functions, like:  
    '''  
    return-type function_name (parameters){  
    #Action to be performed  
    Action_1;  
    Action_2;   
    Return expression;
    }  
    '''       
### *Python (extensible)*  
   ***Necessary libraries:***  
   1) Pyfirmata protocol, the firmata protocol should be uploaded to the board at first. (Pyfirmata libraries for Python: pyfirmata or pymata)  
   2) Serial library  
   3) Pymata library(replaced by pymata_aio): for quick I2C communication. Implementation: 'from pymata_aio.pymata3 import PyMata3'   
   
#### *1. Programming via firmata protocol* 
   1) As part of working with the Arduino board and the Firmata protocol, you have to start by **initializing the Arduino board as a variable**. --- board = pyfirmata.Arduino(port)  
   2) Configure Arduino pins: We first assign their modes (INPUT, OUTPUT, PWM SERVO)(here two ways are available), then read/write their information. Once the value of the variable is assigned, you can perform various actions such as reading a pin or sending a signal to the pin using that variable. To assign a role to a pin, the get_pin() method is used. In the following line of code, d represents the digital pin, 7 is the pin number, and i represents that the type of pin is an input pin:     
       'pirPin = board.get_pin('d:7:i')'  
   Once a pin and its role are assigned to a variable, that variable can be used to read or write values on the pin:    
       'Value = pirPin.read()'   
   One can directly write data to a specific pin, as described in following code:  
       'board.digital[pin].write(1)'   
   Here, the write(1) method sends a HIGH signal to the pin. We will be learning additional pyFirmata methods in the upcoming chapters.  
   The differences also lie in other syntax, like definition of function (in python, it's "def function():"; while in Arduino IDE, it's "type function(){}") or other commands. 
   3) Working with pins: Two different types of methods are supported while working with pins: **reporting methods and I/O operation methods**.  
        i) Iterator(): handle the data over the port to avoid serial overflow.   
        ii) Write and read the pins:  write() for the ouput pins, and read() for the input pins. Read() is under the Iterator() class to avoid overflow. ***The output value is different vai pyfirmata.(voltage value at analog pin(0-5V)--value Arduino measured(0-1023)--Pyfirmata's read(0-1))***  
        **Other communication methods: I2C- or SPI bus-based methods.** Most intergrated circuit (IC) support I2C, which can be checked with SDA and SCL pins. I2C uses the concept of master-slave devices, where the microcontroller is the master and the peripherals are the slave devices. The I2C protocol connects the microcontroller or the CPU to a large number of low-speed peripheral devices using just two wires (**Serial Data Line (SDA) and Serial Clock Line (SCL)**). The peripheral sensors that are working as slaves connect to these lines, which are also supported by the pull resistors. The master device is responsible for generating the clock signal on the SCL and initializing communication with the slaves. The slave devices receive the clock and respond to the commands sent by the master device.  
   4) Adding sleep time: to avoid any issues related to the serial port buffering.--- (from time import sleep, the sleep parameter are in second scale.)  
   5) free the serial port: board.exit()  
   
#### *2. Programming via serial*    
   Compared with Programmig via firmata, this method would be better for product design.  
   1) Connect the serial port:   
       'import serial'  
       'port = serial.Serial('COM5',9600, timeout=1)'   
       In addition to port name and baud rate, you can also specify a number of serial port parameters such as timeout, bytesize, parity, stopbits, and so on using Serial(). It is necessary to initialize the serial port before executing any other command from the pySerial library.  
   2) Read a line from the port:  
      'line = port.readline()'  
      The readline() function will process each line from the port that is terminated with the end line character \n.  
   3) Flush the port to avoid buffer overflow:   
      'port.flushInput()'  
   4) Closing the port:   
      'port.close()'

#### 3. Working with Python GUI

#### 4. Storing and Plotting Arduino data  
   Instead of using the string format, if the data is printed as a plot or graph, it will provide useful information for us to rapidly understand it and derive conclusions. Plots are even more useful for real-time applications as they can provide information regarding the system’s behavior for better understanding of the data.  
   1) Storing the Arduino sensor data  
      The 'with' statement is widely used in Python to deal with files, since it executes the wrapped code while automatically taking care of closing the file.   
   2) Plotting the data (via matplotlib)  
   3) Integrate the matplotlib with the tkinter window    
* Data Visualization  
   1) All data are saved, then plotted
   2) Plot real-time data
   3) Integrate plots in Tkinter window
   
#### 5) Arduino and the network
   In this section, we will cover the basics of networking and hardware components that enable networking in Arduino.  
* Network fundamentals
   1) Network classifications  
   2) Protocols for communication between network nodes  
     * Protocols
     * MAC (Media access control) address: the identifier for the network nodes
     * IP (Internet protocol) address: which is assigned to the nodes by the router.  
* Network extensions for Arduino  
   The most popular extensions used to enable networking are the Arduino Ethernet Shield and Arduino WiFi Shield.
   

---
## Comparison between different programming methods
### *Disadvantages for Firmata-based projects:*
   1) **Delay in real-time execution**: Firmata-based approaches require a series of serial communication messages to receive and send data, which adds additional delay and reduces the speed of execution.   
   2) **Unwanted space**: The Firmata protocol contains a large amount of additional code to support various other Arduino functions. In a well-defined project, you don’t really need the complete set of functions.   
   3) **Limited support**: Although a version of Firmata includes I2C support, it is quite difficult to implement complex I2C functions without adding delay.  
   In summary, you can always use Firmata-based approaches to quickly prototype your projects, but when you are working on **production-level or advanced projects**, you can use alternative methods. ***In these scenarios, you can use custom Arduino code that is supported by Python’s serial library, pySerial, to enable communication for very specific functionalities***. In this section, we are going to cover a few helpful pySerial methods that you can use if you have to utilize the library directly.


---
## Experimental example
1. Prototyping

---
## Ideas  
1. Motion-triggered LEDs, which can be referred for robotic navigation ---(via PIR sensor)

---
## Reference
[1] [Python programming for Arduino](https://www.amazon.com/Python-Programming-Arduino-Pratik-Desai/dp/1783285931)  
[2] [Arduino with Python](https://www.youtube.com/watch?v=95w4sx_zoB8): video tutorial  
[3] [Arduino with Python: how to get started](https://realpython.com/arduino-python/)   
[4] [Python GUI Programming With Tkinter](https://realpython.com/python-gui-tkinter/)  