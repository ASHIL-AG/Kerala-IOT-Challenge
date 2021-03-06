# Kerala-IOT-Challenge
Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala is launching our prestigious program “Kerala IoT Challenge 2021”, with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation
# About Me
Hi everyone! I'm Ashil George P G.I'm currently pursuing BTech in Electrical and Electronics Engineering from ALBERTIAN INSTITUTE OF SCIENCE AND TECHNOLOGY [AISAT], ERNAKULAM. My major area of interests are IOT,Aeromodelling ,Drones and RC planes piloting,programming etc.
# Experiment 1 : Hello World LED Blinking
A basic program similar to printing "Hello World" in any programming language. The aim is to blink an LED using Arduino Uno Board.

Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Components Required  
* Arduino Uno Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos

## Circuit Diagram
![IMG_20211219_003753](https://user-images.githubusercontent.com/95869156/146653882-325b2538-eec4-43a2-8bfd-78dc7d49bf1b.jpg)
![5h7X9_3102_1627394356](https://user-images.githubusercontent.com/91405741/137279765-8a82a34f-1dc0-4afc-9bd3-a31d7f62c428.png)


## Code

```
int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}
```

## Output
> The LED is blinked with a time interval of 1 second
<iframe width="560" height="315"
src=
        
 https://user-images.githubusercontent.com/95869156/146654302-7499a267-e699-4476-86a8-3204b2d5c383.mp4
       
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 
# Experiment 2 : Traffic Light

> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.
## Components Required 

* Arduino board *1
* USB cable *1
* Red M5 LED*1
* Yellow M5 LED*1
* Green M5 LED*1
* 220Ω resistor *3

## Circuit Diagram

![yiU1x_3102_1627566759](https://user-images.githubusercontent.com/91405741/137288387-e85f8db9-ae97-49d0-888d-a2fc15e4c496.png)
![IMG_20211219_005436](https://user-images.githubusercontent.com/95869156/147391612-79d898e9-72c9-4457-863b-f08a46fd0677.jpg)


## Code

```
int redled =10; // initialize digital pin 10.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds
digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}
```

## Output

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.

> The LED is blinked with a time interval of 1 second
<iframe width="560" height="315"
src=
        
 https://user-images.githubusercontent.com/95869156/147391852-4ac6fe15-21fc-4571-a6a6-41080ab51cce.mp4

       
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 
# Experiment 3 : LED Chasing Effect

> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side; short lead is negative.
## Components Required

* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

## Circuit Diagram

![s5yR0_3102_1627567167](https://user-images.githubusercontent.com/91405741/137292096-feb60c91-1a9a-474b-a596-300285f7b011.png)
![IMG_20211219_011146](https://user-images.githubusercontent.com/95869156/147391633-f745bbe7-3aed-429d-b505-3bc8ce6f7524.jpg)

## Code

```
int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(400);        // delay
   }  
}
```

## Output


<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/95869156/147391911-bc3ae628-15ec-4a16-b65a-de079a646fcc.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 4 : Button Controlled LED

> An experiment to light an LED using a Push Button.
## Components Required 

* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

## Circuit Diagrams

![wQGca_3102_1628160139](https://user-images.githubusercontent.com/91405741/137344321-3e662dee-cb00-421d-a34d-848c2ffd1a6f.png)

![IMG_20211231_000054](https://user-images.githubusercontent.com/95869156/147783707-f4af71d9-ca86-401a-ba0b-cb73360d6ee1.jpg)
## Code

```
int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}
```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.
<iframe width="560" height="315"
src=


https://user-images.githubusercontent.com/95869156/147783915-ff390cb5-625e-48bd-8ccb-b578c90629de.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.
## Components Required

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

## Circuit Diagrams

![BBr05_3102_1628160460](https://user-images.githubusercontent.com/91405741/137346830-1fa2408c-2a1d-4fdf-a049-5736aeb803ec.png)

![e9Pdc_3102_1628160446](https://user-images.githubusercontent.com/91405741/137346912-0f871dbf-8e86-4734-a337-fceeff454e33.png)
![IMG_20211231_000540](https://user-images.githubusercontent.com/95869156/147783760-0cd71094-c9da-48f7-a630-693c814f329e.jpg)


## Code

```
int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}
```

## Output

> The Buzzer makes beep sound.
<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/95869156/147783940-03ee47a1-cac0-42e9-bd27-b81fb6b48179.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.
## Components Required

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams
![xX9cw_3102_1628160649](https://user-images.githubusercontent.com/91405741/137347719-6966c0b1-021d-471c-b0a7-48d0441752d0.png)

![A8a40_3102_1628160631](https://user-images.githubusercontent.com/91405741/137347782-e0a8a008-8706-4b7c-ba31-38ef0ab6ca72.png)

![TefdI_3102_1628167200](https://user-images.githubusercontent.com/91405741/137347822-228ccf9c-3a89-45ba-bb24-c3b0ee587818.png)
![IMG_20211231_001727](https://user-images.githubusercontent.com/95869156/147783842-52738376-a9c3-4612-8eec-d67cc0b08d5a.jpg)

## Code

```
int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}
```

## Output

> The RGB LED blinks.
<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/95869156/147783968-7e6f1a33-a312-44d9-b7cb-fac464fc960c.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 7 : LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.
### LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.
## Circuit Diagrams


![L5Iw9_3102_1628755894](https://user-images.githubusercontent.com/91405741/138436746-d1cfb008-0d90-4754-b4c4-fe133329c8b5.png)
![IMG_20211231_005943](https://user-images.githubusercontent.com/95869156/147783874-b2e4e58e-b164-4542-9276-fe35254b3221.jpg)

## Components Required

* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*7
* USB cable*1

## Circuit Diagrams
![schema_Myt5vqqplZ](https://user-images.githubusercontent.com/91405741/138436635-60cb2ec4-091d-4f24-bf96-b0289e06fa00.png)

## Procedure

* Connect the 3.3v output of the Arduino to the positive rail of the breadboard
* Connect the ground to the negative rail of the breadboard
* Place the LDR on the breadboard
* Attach the 10K resistor to one of the legs of the LDR
* Connect the A0 pin of the Arduino to the same column where the LDR and resistor is connected (Since the LDR gives out an analog voltage, it is connected to the analog input pin on the Arduino. The Arduino, with its built-in ADC (Analog to Digital Converter), then converts the analog voltage from 0-5V into a digital value in the range of 0-1023). - Now connect the other end of the 10K resistor to the negative rail
* And the the second (free) leg of the LDR to the positive rail
Pretty much this is what we need for the light sensing. Basic circuits like this can be done without an Arduino aswell. However, if you want to log the values and use it to create charts, run other logics etc. I will recomend an Arduino or ESP8266 or may be a ESP32 for this.
Now, as we want our circuit to do something in the real world other than just displaying the values on the computer screen we will be attaching a LED to the circuit. The LED will turn on when its dark and will go off when its bright. To achieve this we will:
* Place the LED on the breadboard
* Connect the 220ohm resistor to the long leg (+ve) of the LED
* Then we will connect the other leg of the resistor to pin number 13 (digital pin) of the Arduino
* and the shorter leg of the LED to the negative rail of the breadboard

## Code

```

const int ledPin = 10;
const int ldrPin = A0;
void setup() {
Serial.begin(9600);
pinMode(ledPin, OUTPUT);
pinMode(ldrPin, INPUT);
}
void loop() {
int ldrStatus = analogRead(ldrPin);
if (ldrStatus >= 500) {
digitalWrite(ledPin, HIGH);
Serial.print("Its DARK, Turn on the LED : ");
Serial.println(ldrStatus);
} else {
digitalWrite(ledPin, LOW);
Serial.print("Its BRIGHT, Turn off the LED : ");
Serial.println(ldrStatus);
}
}
```

## Output

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/95869156/147783995-b962eab1-095c-4c26-8885-e16e8e354f0e.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 8 : Flame Sensor

> We are using Infrared Receiver (IR)for detecting Flame 
## Components Required
* Arduino Uno Board*1
* Flame Sensor *1
* Buzzer *1
* LED *2
* Breadboard 
* Jumper Wire*6
* USB cable*1

## Circuit Diagram
![WhatsApp Image 2022-01-24 at 11 07 38 PM](https://user-images.githubusercontent.com/95869156/150840688-7b4f3d23-8023-4d2c-a54b-492f74e215b3.jpeg)
![IMG_20220124_233756](https://user-images.githubusercontent.com/95869156/150840786-0973c347-33bd-45fd-95f4-5a306ed01660.jpg)
## Code

```
int flame=0;
int buzzer=9;
int val=0;
void setup() {
 
pinMode(buzzer,OUTPUT);
pinMode(flame,INPUT);
Serial.begin(9600);

}

void loop() {
  val=analogRead(flame);
  Serial.println(val);
  if(val>=600)
  {
    digitalWrite(buzzer,HIGH);
  }else
{digitalWrite(buzzer,LOW);
}
delay(500);
}

  
```

## Output

> The buzzer produces a beep noise along with red LED lighting up when the IR Reciever is exposed to flames.



<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/95869156/150840841-115f0792-a462-4f1d-92aa-a5a4177c1986.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 9 : LM35 Temperature Sensor

> LM35 is a common and easy-to-use temperature sensor.


## Components Required 

> LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing.
> LM35 temperature sensor can produce different voltage by different temperature
When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.
The output temperature is 0℃～100℃, the conversion formula is as follows:
![image](https://user-images.githubusercontent.com/56971600/138460051-cbde66eb-988b-4f15-b350-fb4c29fafa99.png)

## Components Required

* Arduino Uno  Board*1
* LM35*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

## Circuit Diagram 
![IMG_20220124_235906](https://user-images.githubusercontent.com/95869156/151691060-7b9df1b2-72c9-4e96-ba85-9de1c86efb59.jpg)

## Code

```
int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Tep");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(500);// wait for 0.5 second
}
```

## Output

> Temperature values read by LM35 sensor can be seen in the Serial Moniter.


<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/95869156/151691100-484606ef-2b94-422e-b81b-5841db2f9d08.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
# Experiment 10:IR Remote Control Using TSOP

> An experiment to understand the working of IR Remote Control using TSOP.
## Components Required

* Arduino Uno Board*1
* Infrared Remote Controller(You can use TV Remote or any other remote) *1
* Infrared Receiver *1
* LED *6
* 220ΩResistor *6
* Breadboard Wire 
* USB cable*1


## Components Required

* Arduino Uno Board*1
* Infrared Remote Controller(You can use TV Remote or any other remote) *1
* Infrared Receiver *1
* LED *6
* 220ΩResistor *6
* Breadboard Wire 
* USB cable*1

## Circuit Diagrams

![IMG_20220131_003811](https://user-images.githubusercontent.com/95869156/151714264-08be574a-d22f-4612-8075-dedc689ebd85.jpg)



## Code

```
#include <IRremote.h> 
int RECV_PIN = 3;              
int c=0;                      
IRrecv irrecv(RECV_PIN);
decode_results results;
void setup()
{
   pinMode(8, OUTPUT);
   pinMode(9, OUTPUT);
   pinMode(10, OUTPUT);
   pinMode(11, OUTPUT);
   Serial.begin(9600);
  irrecv.enableIRIn();                     
}
void loop() {
  if (irrecv.decode(&results)) {
    Serial.println(results.value);
    irrecv.resume();                        
  if(results.value==350984295)      //Up                            
  {
             digitalWrite(8,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(8,LOW);
  }
   if(results.value==350949615)  //Down                                     
  {
             digitalWrite(9,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(9,LOW);
  }
    if(results.value==350994495) //left                                       
  {
             digitalWrite(10,HIGH);
  }
  else if(results.value==4294967295) 
  {
             digitalWrite(10,LOW);
  }
    if(results.value==350992455) //right                                       
  {
             digitalWrite(11,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(11,LOW);
  }
   
  }
  }

```

## Output

<iframe width="560" height="315"
src=
   

https://user-images.githubusercontent.com/95869156/151714270-0206f987-2175-43d4-99d4-566a71c3920b.mp4

   
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 


# Experiment 11 :Potentiometer analog Value Reading

> An experiment to understand the working of Potentiometer.
## Components Required

* Arduino Uno Board*1
* 10K Potentiometer *1
* Breadboard*1
* Breadboard Jumper Wire*3
* USB cable*1

## Circuit Diagrams

![IMG_20220130_105040](https://user-images.githubusercontent.com/95869156/151691070-8ab3589f-6392-442e-831c-0a603847bbae.jpg)

## Code

```
int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}
```

## Output

<iframe width="560" height="315"
src=
        
https://user-images.githubusercontent.com/95869156/151691107-960faf81-cb8f-42fa-b659-6dbbd7a47fb9.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 


# Experiment 12 : 7 Segment Display
        
> An experiment to understand the working of 7 Segment Display.
## Components Required

* Arduino Uno Board*1
* digit LED Segment Display*1
* 220Ω Resistor*8
* Breadboard*1
* Breadboard Jumper Wires *several
* USB cable*1

## Circuit Diagrams

![IMG_20220130_112332](https://user-images.githubusercontent.com/95869156/151691074-6525700f-b706-4e79-b48c-d8cd1ecadf80.jpg)


```
int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}
}
```

## Output

<iframe width="560" height="315"
src=
        

https://user-images.githubusercontent.com/95869156/151691111-04f586c0-e6d7-436e-bee1-298980983416.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 

# Assignment 1 : Automatic Night Lamp

> An experiment to create automatic night lamp model using LDR and LED.
## Components Required

* Arduino Uno Board
* Photo Resistor*1
* LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire
* USB cable*1

## Circuit Diagrams 

![L5Iw9_3102_1628755894](https://user-images.githubusercontent.com/91405741/138436746-d1cfb008-0d90-4754-b4c4-fe133329c8b5.png)
![IMG_20211231_005943](https://user-images.githubusercontent.com/95869156/147783874-b2e4e58e-b164-4542-9276-fe35254b3221.jpg)
![schema_Myt5vqqplZ](https://user-images.githubusercontent.com/91405741/138436635-60cb2ec4-091d-4f24-bf96-b0289e06fa00.png)


## Code
```

const int ledPin = 10;
const int ldrPin = A0;
void setup() {
Serial.begin(9600);
pinMode(ledPin, OUTPUT);
pinMode(ldrPin, INPUT);
}
void loop() {
int ldrStatus = analogRead(ldrPin);
if (ldrStatus >= 500) {
digitalWrite(ledPin, HIGH);
Serial.print("Its DARK, Turn on the LED : ");
Serial.println(ldrStatus);
} else {
digitalWrite(ledPin, LOW);
Serial.print("Its BRIGHT, Turn off the LED : ");
Serial.println(ldrStatus);
}
}
```



## Output

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/95869156/147783995-b962eab1-095c-4c26-8885-e16e8e354f0e.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 

                                                  
# Assignment 2 : Digital Dice using 7 segmemt display 

> An experiment to create a Digital Dice using 6 LEDs and 1 Push Button
## Components Required

* Arduino Uno Board*1
* Breadboard*1
* Breadboard Jumper Wire
* USB cable*1
* 7 segment display
* Push Button*1
* 1KΩ Resistor*1
* 220Ω Resistor*6

## Circuit Diagrams 

![IMG_20220130_124216](https://user-images.githubusercontent.com/95869156/151691085-bc3c017e-68b2-47f6-b877-7c742f6d2a59.jpg)

                                                                             
## Code

```
int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
int COUNT=0;//count integer for 0-6 increment
int dice=12;
void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”               
pinMode(dice, INPUT);
digitalWrite(dice, HIGH);
}

void loop()
{
                COUNT = random(1, 7);
                  if(digitalRead(dice)==0)
                {
                  roll(COUNT);
                  delay(4000);                  
                  
                }

                  roll(COUNT);
                  delay(80);      
}


void roll(int COUNT)
{
switch (COUNT)

                {

                case 0://when count value is zero show”0” on disp
                 digital_0();

                break;

                case 1:// when count value is 1 show”1” on disp

                 digital_1();
                break;

                case 2:// when count value is 2 show”2” on disp

                 digital_2();

                break;

                case 3:// when count value is 3 show”3” on disp

                  digital_3();

                break;

                case 4:// when count value is 4 show”4” on disp

                 digital_4();
                break;

                case 5:// when count value is 5 show”5” on disp

                 digital_5();

                break;

                case 6:// when count value is 6 show”6” on disp

                 digital_6();
                 break;

                 break;

                }  
}
```

## Output


<iframe width="560" height="315"
src=


https://user-images.githubusercontent.com/95869156/151691131-21b6832b-66cd-416d-82ce-8ca9ab97fa48.mp4



frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 

