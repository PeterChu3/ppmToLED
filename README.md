# ppmToLED
## Story
![Schematic View rev1](https://github.com/chuy4ever/ppmToLED/blob/main/Images/riding.gif?raw=true)

I ride with my friend Brendan Bassett on our electric skateboards around Atlanta. However, there is a slight problem with Brendan's build. Under high speed the board seems to cutout with no fault recorded. We are assuming that the motor controller is fine and Brendan's hand controller/reciever is briefly not outputing the correct ppm signal. We had issues with the remote before, but we had to design and make our solution to test our theory. 

## Our solution
We will tap into the PPM signal and decode it using a microcontroller. 

Then we will output to some addressable LEDs. We will code a map function that intensifies the brightness based on the magnitude of the PPM signal. 

Full brake would result in full brightness red.

Full acceleration would result in full brightness green.

A neutral signal would result in off LEDs or display a neutral color.

## Explanation
The board uses a ATtiny85 to decode the PPM signal and output to a few addressable LEDs.

We chose the ATtiny85 because of it's simplicty and compact package. Also, Georgia Tech's makerspace provides them for free.

The input is 5v and provided by the motor controller.

The outputs are also 5v on all connectors. There is a connector for both PPM and LED out.

## Pinout

Pin 2 is an input pin for the PPM signal. 

Pin 4 is an OUTPUT pin for the address LEDs. 
Library to drive Pin 4 TBD.


## Schematic and Board layout

Schematic view
![Schematic View rev1](https://github.com/chuy4ever/ppmToLED/blob/main/Images/Schematic.png?raw=true)


Layout view
![Layout View rev1](https://github.com/chuy4ever/ppmToLED/blob/main/Images/Board.png?raw=true)


Board view
![Board View rev1](https://github.com/chuy4ever/ppmToLED/blob/main/Images/PPMCapture.png?raw=true)
