# maicab_fullsize
A collection of notes and lessons learned from building a maimai-like home arcade cabinet. 
This is not meant as a "guide" as its unlikely your build will be the same as mine. Instead, hopefully the lessons learned here can help you in your own similar project. 

*What is MaiMai?* : 
It's like Dance Dance Revolution, but for your hands. Explanation: https://youtu.be/TCW5DejMcog?t=46

Special thanks to these guides and the help they offered:
- https://github.com/whowechina/mai_pico
- https://github.com/ir0nq/maimai-homemade-controller
- https://github.com/Syndric/maimai-controller-fullsize

## Finished Project:

Here is a look at the finished project running Majdata Play. (Majdata Play is an open-source software that allows you to play custom charts for maimai.) https://github.com/LingFeng-bbben/MajdataPlay
 
<img src="./Photos/gameplay.gif" width="600"><img src="./Photos/front_finished.jpg" width="600"><img src="./Photos/front_finished_gameplay_still.jpg" width="600">


# Materials
Check the [Materials](Materials.md) page. 


# Lessons Learned

## Buttons

I bought the buttons from a seller on Ali Baba

### Button Sensor:
I cant be sure of the EXACT model number of the sensor, but it seems to be  a **Sharp GP1A73AJ000F**. This is no longer available from places like digikey and mouser, but there is a large inventory in China. I bought replacements from aliexpress: https://de.aliexpress.com/item/1005008751424908.html?gatewayAdapt=glo2deu#nav-specification

It's easy to burn out the sensor if you dont know what you are doing, and directly wire the input to 5v. You need a current limiting resistor. I used a 220 ohm that I spliced in-line between the board and the button. Any 100-220ohm resistor is a safe bet. the 1.1v of the mai_pico pcb actually accomadates this now: 

### Spacers

I printed it with the player facing side up, and high quality settings with ironing enabled (search reddit for ironing settings). Ironing on the top made the part look and feel like excellent quality, its very smooth. I had to enable supports. 

