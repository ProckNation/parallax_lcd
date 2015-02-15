[![Stories in Ready](https://badge.waffle.io/iamthechad/parallax_lcd.png?label=ready&title=Ready)](https://waffle.io/iamthechad/parallax_lcd)

# ProckNation.com Fork Update 02-15-2015
As of 2-15-2015 I am going to make changes to the library to enable the use of hardware serial ports Serial, Serial1, Serial2, and Serial3.  Most of the Arduino hardware has at least one hardware serial UART named Serial.  The Mega 2560 has three more serial UART ports named Serial1, Serial2, and Serial3.

Adapting this library for use with these hardware serial ports will allow you to have an Arduino with hardware serial ports for debug terminal/code uploading, GPS, OpenLog data logger, and a Parallax Serial 20x4 LCD all at the same time with no interferance between the four.

Thanks, Jason



# Parallax LCD

The Parallax LCD library allows for writing to Parallax three wire LCDs.
It is known to work with Parallax LCD's (27976, 27977, 27979).

For more information about Parallax LCDs, see [http://www.parallax.com](http://www.parallax.com)	

## Functions

The library offers the following functions:

* setup
* on
* off
* scrollLeft
* scrollRight
* empty
* cursorUnderline
* cursorBlock
* cursorOff
* cursorOnChrBlink
* cr
* lf
* backLightOn
* backLightOff
* playTone
* setCustomCharacter
* printCustomCharacter
* pos
* at

## Example

Using the library is simple. See the included example for more.

    #include <SoftwareSerial.h>
    #include <ParallaxLCD.h>

    ParallaxLCD lcd(2,2,16); // desired pin, rows, cols

    void setup () {
      lcd.setup();
      delay(1000); // Wait for the LCD to start up
      lcd.at(1,3,"Hello World!");
    }

## Installing

* Clone this repository or select the "Zip" button above to download the code. 
* Place the directory into `libraries` within your Arduino Sketches folder. (You may have to create the `libraries` folder.) 
* Restart the Arduino IDE if it's running.
* Go to `File`->`Examples`. There should now be an entry for `parallax_lcd` in the list. Select it to see the example.
* Using the example as a guide, write your own code!

# License

This library is provided under the MIT license. You can obtain a copy of this license at http://opensource.org/licenses/MIT.

##### Misc     
Original Work done by:
[Douglas Farrell](cyberblob59@yahoo.com)
		  
Based on SparkFunSerLCD.h from:
[allen joslin](allen@joslin.net)

Tone/Custom character support added by:
[Martin C. Stoufer](mcstoufer@speakeasy.net)
