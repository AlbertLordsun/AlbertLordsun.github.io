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
    1) TinkerCAD;(programming is one advantage, we can directly see the simulation results on the website)   
    2) Fritzing
3. Circuit connection  
4. Test  

---
## Software and programming  
    The part can be analyzed from two levels: 1) components-to-Arduino; 2) Arduino-to-Python.
1. Arduino IDE (traditional, lack the extensiveness)  
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
        
2. Python (extensible)  
    ***Necessary libraries:***  
    1) Pyfirmata protocol, the firmata protocol should be uploaded to the board at first.  
    2) Serial library  
    ***Programming:***  
    1) As part of working with the Arduino board and the Firmata protocol, you have to start by **initializing the Arduino board as a variable**. --- board = pyfirmata.Arduino(port)  
    2) Once the value of the variable is assigned, you can perform various actions such as reading a pin or sending a signal to the pin using that variable. To assign a role to a pin, the get_pin() method is used. In the following line of code, d represents the digital pin, 7 is the pin number, and i represents that the type of pin is an input pin:     
        'pirPin = board.get_pin('d:7:i')'  
    Once a pin and its role are assigned to a variable, that variable can be used to read or write values on the pin:    
        'Value = pirPin.read()'   
    One can directly write data to a specific pin, as described in following code:   
        'board.digital[pin].write(1)'   
    Here, the write(1) method sends a HIGH signal to the pin. We will be learning additional pyFirmata methods in the upcoming chapters.  
    The differences also lie in other syntax, like definition of function (in python, it's "def function():"; while in Arduino IDE, it's "type function(){}") or other commands.  
    

---
## Experimental example
1. Motion-triggered LEDs, which can be referred for robotic navigation


---
## Reference
[1] [Python programming for Arduino](https://www.amazon.com/Python-Programming-Arduino-Pratik-Desai/dp/1783285931)