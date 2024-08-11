# ver 3

  ## goal 
 Make the PCB smaller and cheaper based on the previous version (using ESP32, bluetooth)

  ## choose IC 

  ### NRF24L01P-R 
This time, I want to try using an RF module for communication (to reduce costs). After consulting ChatGPT and considering the amount of reference material available online, I decided to use this IC.

  ### DRV8837DSGR 
Although using this IC will require two separate ICs to drive the motors, I suspect this might make routing and layout easier. Even with two ICs, the cost is only a quarter of the old solution (though there might be unforeseen issues during     
                   implementation :) ).

  ### ATTINY1616-MNR
I'm not entirely sure which MCU to choose. I decided on the ATTINY1616 because I often see people using the ATTINY series MCUs to make remote control cars on YouTube. So I looked up ATTINY models with more than 10 GPIOs and eventually chose the       
                     ATTINY1616. After deciding, I started searching for relevant information to draw the schematic, but there was much less information available than I expected. Luckily, I found someone who had made a development board with the ATTINY1616, complete with                       a schematic!
 ![plan](https://github.com/user-attachments/assets/1aefb075-60f7-43f3-a199-f7a33e822fd3)

 # ver 4
 ## goal
 Make the PCB smaller (antenna)
 ## antenna knowledge
 Frequency Range: the antenna desired frequency band (2.4 GHz).

Gain: Measure of how much the antenna amplifies the signal, typically in dBi. Higher gain means stronger signal in specific directions.

Impedance: Usually 50Ω to match the RF circuitry and minimize signal reflection.

Bandwidth: The range of frequencies over which the antenna can operate effectively.

Efficiency: Represents how well the antenna converts input power into RF energy. Higher efficiency is better.

Radiation Pattern: The distribution of radiated power in space, which determines how the antenna transmits and receives signals.

Polarization: Orientation of the electromagnetic wave.

ref:https://www.johansontechnology.com/understanding-chip-antennas-handbook

## pcb layout
The first layer is for the antenna signal circuit and the signal transmission circuits between the MCU and RF IC. 
The second layer is the ground plane. 
The third layer is for power (3.3V, 3.7V, 5V).
The fourth layer is for signal routing. 

The antenna is placed at the edge.
The motor driver is positioned away from the RF area. 
The ground plane should be continuous and uninterrupted to provide a stable reference plane and signal return path. 
Use vias to connect the power layer to the ground plane to provide decoupling and reduce power noise.

ref:
https://resources.altium.com/p/digital-engineers-guide-rf-pcb-layout-and-routing
https://resources.altium.com/p/follow-your-multilayer-ground-return-path-to-prevent-emi#ground-return-path-vs-reference-planes
https://resources.altium.com/p/changing-pcb-reference-planes-during-routing-multilayer-boards
https://resources.altium.com/p/what-rf-circuit-design
