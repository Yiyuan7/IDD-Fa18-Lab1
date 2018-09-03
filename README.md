# IDD-Fa18-Lab1: Blink!

**A lab report by John Q. Student**

**Fork** this repository to get a template for Lab 1 for *Developing and Designing Interactive Devices* at Cornell Tech, Fall 2018. You should modify this `README.md` file to delete this paragraph and update below. As the lab asks:

> Include your responses to the bold questions on your own fork of the lab activities. Include snippets of code that explain what you did. Deliverables are due next Tuesday. Post your lab reports as `README.md` pages on your GitHub, and post a link to that on your main class hub page.

We've copied the questions from the lab here. Answer them below!

## Part A. Set Up a Breadboard

[insert a photo of your breadboard setup here]


## Part B. Manually Blink a LED

**a. What color stripes are on a 220 Ohm resistor?**
 bule with two black, two black and one brown strip
**b. What do you have to do to light your LED?**
press the button

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**
pinmode
**b. What line(s) of code do you need to change to change the rate of blinking?**
delay
**c. What circuit element would you want to add to protect the board and external LED?**
 resistance
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**
0.013s
**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(13, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(13, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(500);                       // wait for a second
  digitalWrite(13, LOW);    // turn the LED off by making the voltage LOW
  delay(100);                       // wait for a second
}

### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[link to your video here; feel free to upload to youtube and just paste in a link here]


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**
yes
there will always have current through the led
## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
the led form pin 9 to pin 11
**b. What is analogWrite()? How is that different than digitalWrite()?**
analogwrite can support a rangeof the voltage and can generat a steady square wave of the specified duty cycle 
while digitalwrite can only make support low and high two voltage.
## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**
yes . in the pcb. It's a logit curcit
**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**
yes it's a pressure sensor. So when you press th key on th calculator, it will work. it will changed the resistance and then change the current to convey.
**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**
by battery. I don't think so. The calculator will use 5 volte voltage.
**d. Is information stored in your device? Where? How?**
yes. In calculator's memory. By bing tranfered to 0 and 1 and then stored in memory.
### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
