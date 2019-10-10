# Paper Puppets

*A lab report by Michael Chan*



## Part A. Actuating DC motors

**Link to a video of your virbation motor**

[Vibration Motor](https://youtu.be/EyhNSQXMc8k)

## Part B. Actuating Servo motors

### Part 1. Connect the Servo to your breadboard

**a. Which color wires correspond to power, ground and signal?**

Red is the power, brown is the ground and ornage is the signal.

### Part 2. Connect the Servo to your Arduino

**a. Which Arduino pin should the signal line of the servo be attached to?**

It should be on pin 9 per the myservo.attach line of code.

**b. What aspects of the Servo code control angle or speed?**

The angle is controlled by the intialization of the for loops.  The 180 to 0 tells the servo to rotate from 0 to 180 degrees.  The steps in the for loop indicate how fast it should change angle, in this case it is set at 1 degree.  

## Part C. Integrating input and output

**Include a photo/movie of your raw circuit in action.**

[Raw Circuit](https://youtu.be/lWXs9B64lwE)

## Part D. Paper puppet

**a. Make a video of your proto puppet.**

[Paper Puppet](https://youtu.be/k30X19Ruazs )

## Part E. Make it your own

**a. Make a video of your final design.**

![Countdown](https://github.com/mkc233/IDD-Fa19-Lab4/blob/master/Countdown.jpg)

I attempted to assemble the countdown paper puppet, however i was unable to get good enough contact with the screw and paper to make the paper actually rotate around and coutndown.

```
/* Sweep
 by BARRAGAN <http://barraganstudio.com>
 This example code is in the public domain.

 modified 8 Nov 2013
 by Scott Fitzgerald
 http://www.arduino.cc/en/Tutorial/Sweep
*/

#include <Servo.h>

Servo myservo;  // create servo object to control a servo
// twelve servo objects can be created on most boards

int pos = 0;    // variable to store the servo position

void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
}

void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
}

```
 
