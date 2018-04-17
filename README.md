## SERIAL LCD LIBRARY FROM ARDUINO

I put this up on github just to make it easy to use it with Platormio.  This library came from Arduino so I had nothing to do with its creation.  It is very handy if you want to use it with SparkFuns's 20 columnt Serial LCD screen (LCD-09568.)  It should also work with other serial enabled displays, but I have not tried any of them.

![LCD-09568](/doc/readme-assets/LCD-09568.jpg)]

Here is a couple of things that are useful to know about this library.

1. To create an instance of lcd object

    `#define LCD_RX_PIN 8 // RX pin` <br>
    `serLCD lcd = ser(LCD_RX_PIN); // lcd will be the name of the instance`

2. To setup the display, you will need to call the setType method twice.  This method can be called with the following parameters:

    3 sets up display with 20 columns <br>
    4 sets up display with 16 columns <br>
    5 sets up display with 4 rows <br>
    6 sets up display with 2 rows <br>

    so for LCD-09568 you would call

    `lcd.setType(3);`<br>
    `lcd.setType(5);`

3. Outputting text to display is simple:<br>

    `lcd.print("Some text");`

4. To move to specific row (setting cursor to column 1):<br>

    `lcd.select(1) // Line 1 in this case`

5. To put cursor into a specific locations, lets say row 2 column 5: <br>

    `lcd.setCursor(2, 5);  // format is (row, col)`

6. You can clear the display:<br>

    `lcd.clear();`
