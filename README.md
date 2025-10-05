# maicab_fullsize
A collection of notes and lessons learned from building a maimai-like home arcade cabinet. 
This is not meant as a "guide" as its unlikely your build will be the same as mine. Instead, hopefully the lessons learned here can help you in your own similar project. 

Special thanks to these guides and the help they offered:
- https://github.com/whowechina/mai_pico
- https://github.com/ir0nq/maimai-homemade-controller
- https://github.com/Syndric/maimai-controller-fullsize

## Finished Project:

Here is a look at the finished project running Majdata Play. (Majdata Play is an open-source software that allows you to play custom charts for maimai.) https://github.com/LingFeng-bbben/MajdataPlay
 
<img src="/Photos/gameplay.gif" width="600"><img src="/Photos/front_finished.jpg" width="600"><img src="/Photos/front_finished_gameplay_still.jpg" width="600">


## Materials:

### Display:
https://www.elotouch.de/open-frame-touchscreens-4363l.html

<img src="https://marvel-b1-cdn.bc0a.com/f00000000296536/www.elotouch.de/media/wysiwyg/3263L-new/Designed-for-easy-integration.png" width="300">

This is a somewhat controversial choice. 

Latency/Accuracy; Most guides suggest a touch screen display is not suitable for high level play. So far this option has been totally sufficient for around level 10-11 play. it might be that on higher levels of play that its not good enough. I'm not there yet so I cant say. I will say the touch responsiveness and latency so far have been great. Perfect timing taps are super easy. It supports 10 point touch. I do suspect that "circular slides" on the touch screen may cause some trouble.

Cost; Brand new options are far too expensive. I was able to find it on offer for around $500. You might be able to find a similar option.

One last note that made this display a working option compared to other touch displays, is that only skin touch is registering as a touch. The front faceplate of my build sits directly above the screen with a small foam cushion between the board and display. This foam cushion does not register a touch and doesnt interfere with the touch screen. 


### Buttons (8x):

There is a variety of button options for the project, including 3d printing your own. 

I bought 8 of these:

<img src="/Photos/button.png" width="300"> 


https://www.alibaba.com/product-detail/Arcade-Machines-Video-Games-Coin-Operated_1600995755848.html?spm=a2756.trade-carp.valid-supplier.3.184a3192s4dIyb

The quality is great and I am happy with it. This was one of the bigger purchases; 8x $12.50  + shipping + tax = $166

### Spacers (8x)
<img src="/Photos/spacer.jpg" width="600">
I printed at home (ender 3 s1 pro printer) the file from Syndric's github: https://github.com/Syndric/maimai-controller-fullsize/blob/master/cad/Spacer/Maispacer_blank%20v12.stl

I printed it with the player facing side up, and high quality settings with ironing enabled (search reddit for ironing settings). Ironing on the top made the part look and feel like excellent quality, its very smooth. I had to enable supports. 

### Extra Buttons:
I used the red and blue button from this set for the "Insert Coin" and "1P Select" button: 
https://www.amazon.de/-/en/dp/B01N11BDX9?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_1





# Lessons Learned

## Buttons
### Button Sensor:
I cant be sure of the EXACT model number of the sensor, but it seems to be  a **Sharp GP1A73AJ000F**. This is no longer available from places like digikey and mouser, but there is a large inventory in China. I bought replacements from aliexpress: https://de.aliexpress.com/item/1005008751424908.html?gatewayAdapt=glo2deu#nav-specification

It's easy to burn out the sensor if you dont know what you are doing, and directly wire the input to 5v. You need a current limiting resistor. I used a 220 ohm that I spliced in-line between the board and the button. Any 100-220ohm resistor is a safe bet. the 1.1v of the mai_pico pcb actually accomadates this now: 


