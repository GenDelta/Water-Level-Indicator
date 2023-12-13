# WATER LEVEL INDICATOR

In many applications, especially those involving water storage, there is a critical need for an efficient and reliable system to monitor water levels in real-time. Traditional methods often lack accuracy, are labour-intensive, or require constant manual supervision. This poses a challenge for industries, households, and agricultural settings where maintaining an optimal water level is essential for proper functioning and resource management. 


## COMPONENTS USED AND FUNCTIONALITIES

The Water Level Detector project offers a comprehensive solution to monitor and display water levels in a tank in real-time. The key components
and functionalities of the solution include:

- Ultrasonic Distance Sensor: Utilizes an ultrasonic sensor to measure the distance between the sensor and the water surface. The time taken for the ultrasonic waves to travel to the water surface and back is used to calculate the distance.

- OLED Display: Integrates an OLED display for visualizing the water level. The display is initialized using a set of commands stored in the init_display array.

- Data Processing: Converts the measured distance into a percentage value representing the water level in the tank. The calculated water level is then mapped to discrete levels (0 to 4).

- Dynamic Display Update: The system continuously monitors the water level and updates the OLED display accordingly. Different water level categories are visually represented on the display.

- User Interface: Utilizes the serial monitor for debugging purposes and outputs the water level percentage. The user can monitor the water level through the serial interface.

- Categorization Logic: Categorizes the water level into five distinct levels (0 to 4), providing a more intuitive representation of the tank's status.

- Functionality Modularization: The code is organized into functions for better readability and maintainability. Functions like displayLevel()
handle the speccific task of updating the display based on the water level category. 

## OPERATION

- Step 1: Initialization
    The system begins by initializing the required     components and settings. This includes setting up the serial communication for debugging purposes, configuring the pins for ultrasonic distance sensing (trigPin and echoPin), and initializing the OLED display using predefined commands stored in PROGMEM.

- Step 2: Ultrasonic Distance Measurement
    In the loop() function, the ultrasonic sensor is triggered to send a pulse, and the time taken for the pulse to return (echo) is measured. This time measurement is then converted into distance (in centimetres) using the speed of sound.

- Step 3: Mapping and Tank Level Calculation
    The measured distance is mapped to a percentage representing the tank's water level. The project assumes a full tank as 100% and an empty tank as 0%. Any value outside this range is adjusted for clarity.
- Step 4: Tank Level Categorization 
    The tank level is categorized into different levels (0-4) based on predefined thresholds. These levels represent the status of the water level, from critically low to full.

- Step 5: Displaying the Water Level
    The displayLevel() function is called to visualize the water level on the OLED display. This function reads predefined bitmap data for each level and displays it on the appropriate rows of the display.

 
## IMAGES OF WORKING MODEL

![tinkerlab_1](https://github.com/GenDelta/Water-Level-Indicator-/assets/88091748/48701945-4d68-4ad0-bdff-6692c6ce9ca7)

![tinkerlab_2](https://github.com/GenDelta/Water-Level-Indicator-/assets/88091748/e7f198b6-6b61-4783-b3a1-a8cb09755e12)

## CONCLUSION

In conclusion, the water level detector project successfully addresses the challenge of monitoring and managing water levels in a tank. By employing
ultrasonic distance sensing technology, the system accurately measures the water level and translates it into a percentage, providing real-time information for users. The OLED display enhances user accessibility by presenting the water level in a clear and visually intuitive manner. The modular and versatile nature of the project ensures easy integration into various tank systems. 
