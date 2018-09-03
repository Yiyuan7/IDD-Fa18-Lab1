# IDD-Fa18-Lab1: Blink!

## Part A. Set Up a Breadboard

[insert a photo of your breadboard setup here]


## Part B. Manually Blink a LED

**a. What color stripes are on a 220 Ohm resistor?**

The resistance is bule with two black, two black and one brown strips
 
**b. What do you have to do to light your LED?**

Press the button

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**

Change the pinmode line

**b. What line(s) of code do you need to change to change the rate of blinking?**

Change delay()

**c. What circuit element would you want to add to protect the board and external LED?**
 
Use resistance

**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**

0.013s

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**

void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);   
  delay(500);                      
  digitalWrite(13, LOW);    
  delay(100);                     
}

### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[link to your video here; feel free to upload to youtube and just paste in a link here]


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**

Yes I can.
In the whole turning rage, there will always have current through the led.

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

Change the led form pin 9 to pin 11

**b. What is analogWrite()? How is that different than digitalWrite()?**

Analogwrite can support a range of the voltage and can generate a steady square wave of the specified duty cycle 
while digitalwrite can only support two voltage of low and high.

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

Yes . It's in the PCB. It's a logit curcit.

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

yes it's a pressure sensor. So when you press the key on th calculator, it will work. It will changed the resistance and then change the current to convey information.

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

By battery. I don't think there is a tranformation. The calculator will use 5v voltage.

**d. Is information stored in your device? Where? How?**

Yes. In calculator's memory. By being tranfered to number 0 and 1 and then stored in memory.

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

I think the pin on LCD screen module are good hijack points because the pins connected to LCED screen are exposed. I opened the calculator and found those pins. Then I tested the pins by connecting them to LED's positive pin and negative pin to find the high voltage and low voltage pins. After that, I connected my LED to these 2 pins so when I pressed the 'ON' key on the calculator, the screen had a high voltage input and also the LED will have a high voltage input. It will light up. When I pressed 'shift+AC' to power off the calculator, the screen has no high voltage input so does the LED. So the LED will be off. By this connection, I can control the LED by the 'ON' and 'shift+AC' keys on the calculator.

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
