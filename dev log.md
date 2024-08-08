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
