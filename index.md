# Arduino Air Guitar
This is an Airduino Air Guitar, consisting of two parts, a glove and a strummer. Using the glove one can choose which note to play and the strummer helps in choosing the pitch and strum the guitar, imitating a normal guitar. 

 | **Engineer**|**School** |**Area of Interest** |**Grade** | 
 |:--:|:--:|:--:|:--:|
 | Vedika S. |Cupertino High School |Electrical Engineering |Incoming Senior|


<img src="https://user-images.githubusercontent.com/72050310/180516357-11ce3a2c-c6c2-44a1-87a5-e348b9397158.jpg" width="300" height="400"/>


# Project Picture 
<img src= "https://user-images.githubusercontent.com/72050310/180518314-00cac4af-10e9-4404-a8d4-ea1087dc9ce2.jpg" width = "400" height = "200"/>

# Project Video 
https://user-images.githubusercontent.com/72050310/180522914-b6111730-d223-4188-ae10-3517eb8f7634.mp4
  
# Final Milestone
My final milestone was to  make the glove which would represent the keys of the guitar and put final piece together. Though I did not run into any major problems while doing this but a breakdown was that I accidently broke one of the accelerometer pins which brought a hault to my project for a day. Overall, I am pretty happy with the way this tunred out but in the future I would work on the wiring, improve the code to do multiple tasks at one time and maybe modify this into a Ukulele because there are 4 strings and I have 4 finger controls! 

<iframe width="560" height="315" src="https://www.youtube.com/embed/ZzfacvheviM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Second Milestone
My Second Milestone was to generate tones with the ultrasonic sensor. I wrote a piece of code that gave me the distance between the UltraSonic sensor's emitter and receiver; the shorter the distance the lower the pitch and the longer the distance the higher the pitch. When I move the breadboard which has the gyroscope in it, a sound is generated indicating a string was plucked. A major issue I had was that I did not know how to generate sounds in the first place. So, I chose a couple of notes, got the frequencies converted it into microseconds and then tested it out. Once I had got that working, I combined it with the distance sensing code. My next goal is to figure out hand controls to indicate what key is being played then assemble the final piece. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/QgOXuUpqkF0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
# First Milestone
  

My First milestone was setting up the accelerometer with the arduino. The accelerometer I used had an in-built gyroscope which gave me the position of my hands to imitate a classic guitar. I could not find a documentation for the code library I was working with, so upon doing some research I came across the command sheet of the chips manufacturer. Using that I was able to complete my code. My next step is to finish up the circuit by adding a couple other components and start assembeling the device. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/OQkpQJ_ErFA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Bill of Materials 
Here is a list of everything you need for the project!

| **Item** | **Quantity** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Breadboard | 1 | $2.99/count |https://www.amazon.com/Breadboards-Solderless-Breadboard-Distribution-Connecting/dp/B07DL13RZH/ref=sr_1_3?crid=2KWZHQGUK88W&keywords=breadboard&qid=1658521720&sprefix=breadboar%2Caps%2C149&sr=8-3  |
| Wires | 20 | $0.06/count |https://www.amazon.com/EDGELEC-Breadboard-Optional-Assorted-Multicolored/dp/B07GD2BWPY/ref=sr_1_1_sspa?keywords=jumper+wires&qid=1658521821&sprefix=jumper%2Caps%2C152&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUFVNVA2TjBUVFNJQjkmZW5jcnlwdGVkSWQ9QTA5Mjk0MDMzSTRGUVhYOU1KSkRBJmVuY3J5cHRlZEFkSWQ9QTA5NDU0MzYxSkE3VExKQkZEQUxaJndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ== |
| Arduino | 1 | $27 |https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/ref=sr_1_3?crid=87ZRJM3HZ5ZI&keywords=arduino&qid=1658521866&sprefix=arduino%2Caps%2C140&sr=8-3 |
| Speaker/Amplifier | 1 | $11.99 | https://www.amazon.com/Degraw-DIY-Speaker-Kit-Amplifier/dp/B07CRVRG83/ref=sr_1_10?keywords=arduino+speaker&qid=1658521901&sprefix=arduino+spea%2Caps%2C146&sr=8-10 |
| Accelerometer | 1 | $3.33/count | https://www.amazon.com/HiLetgo-MPU-6050-Accelerometer-Gyroscope-Converter/dp/B00LP25V1A/ref=sr_1_1_sspa?keywords=accelerometer&qid=1658521935&sprefix=acceler%2Caps%2C145&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExVDVTMzIxRzc3WFBHJmVuY3J5cHRlZElkPUEwMjY5Mjc4MVUyVzVOMFlQQ0tPWiZlbmNyeXB0ZWRBZElkPUEwNzcxMjIxMU9JSTA4S001Wk40MiZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU=  |
| Ultrasonic Sensor | 1 | $2.29/count | https://www.amazon.com/HiLetgo-MPU-6050-Accelerometer-Gyroscope-Converter/dp/B00LP25V1A/ref=sr_1_1_sspa?keywords=accelerometer&qid=1658521935&sprefix=acceler%2Caps%2C145&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExVDVTMzIxRzc3WFBHJmVuY3J5cHRlZElkPUEwMjY5Mjc4MVUyVzVOMFlQQ0tPWiZlbmNyeXB0ZWRBZElkPUEwNzcxMjIxMU9JSTA4S001Wk40MiZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU= |
| Soldering Kit | 1 | $19.99 | https://www.amazon.com/Soldering-Iron-Kit-Temperature-Desoldering/dp/B07S61WT16/ref=sr_1_1_sspa?crid=1EKZA334X4MH&keywords=soldering+kit&qid=1658522013&sprefix=soldering+kir%2Caps%2C142&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExSEpKVUtBU1BQUEdSJmVuY3J5cHRlZElkPUEwODkwNDQ2M0s5QjU4Wk0yVlhJSiZlbmNyeXB0ZWRBZElkPUEwNTExNjg2MjFFSzAyMTdSTDk0UiZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU= |
| Glove | 1 | $5.99 | https://www.amazon.com/Moisturizing-Serving-Archival-Cleaning-Inspection/dp/B07PY639YJ/ref=sr_1_4_sspa?crid=2KYDL04NVQEVS&keywords=fabric+gloves&qid=1658522096&sprefix=fabric+glove%2Caps%2C143&sr=8-4-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEyRFgyNjc0Rk9LRTZVJmVuY3J5cHRlZElkPUEwMzE4OTIwMzRaSDI1QVdUOFNXNCZlbmNyeXB0ZWRBZElkPUEwOTYzMDQ0MkZFTzhFUlhaQUNIUSZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU= |
| Hot Glue Gun | 1 | $14.99 | https://www.amazon.com/Gorilla-8401509-Hot-Glue-Sticks/dp/B07K791YRP/ref=sr_1_1_sspa?keywords=hot+glue+gun&qid=1658522128&sprefix=Hot+glue+%2Caps%2C140&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExTzRQU0o3UzFPUUZQJmVuY3J5cHRlZElkPUEwMzg1NTI3M1JTMzhKNUNKWVJBMyZlbmNyeXB0ZWRBZElkPUEwODEzNzI2MTZUQVhZRjVWMDJFOCZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU= |
| Resistors | 4 | $1.04/count | https://www.amazon.com/AUKENIEN-1250pcs-Resistor-Assortment-Resistors/dp/B0967TG6XR/ref=sr_1_1_sspa?keywords=resistor+330+ohm&qid=1658522150&sprefix=resistors+330%2Caps%2C142&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEyV1c2RDEwME1BTkZDJmVuY3J5cHRlZElkPUEwODk1ODQxMTFXNDdCTjAxQzBFJmVuY3J5cHRlZEFkSWQ9QTAxNTkzMzNOVkYzOUc3VjA2M0Qmd2lkZ2V0TmFtZT1zcF9hdGYmYWN0aW9uPWNsaWNrUmVkaXJlY3QmZG9Ob3RMb2dDbGljaz10cnVl |
| Conductive Fabric | 1 | $15.99 |https://www.amazon.com/Enclosures-Military-Conductive-Material-Bluetooth%EF%BC%891/dp/B09S36QP4P/ref=sr_1_1_sspa?crid=3EM1Q0GSLPD9J&keywords=conductive+fabric&qid=1658522179&sprefix=conductive+fabri%2Caps%2C139&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExTlBWUERWMVM3NDUxJmVuY3J5cHRlZElkPUEwODA3MTk3MTBOUzJDNkpWVDBIVyZlbmNyeXB0ZWRBZElkPUEwMDc1OTE4MUxGMEg1Q0VTRjg3SCZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU= |


# Schematic 
NOTE: The pins on the Arduino Uno do not represent the actual orientation, it is simply a reference. Please refer to the Ardunino Pinout (and other pinouts) linked below. 

<img src="https://user-images.githubusercontent.com/72050310/180590632-e17755ef-0d13-4bf6-8d67-355a4af92291.png" width="400" height="200"/>

In my project, I used an external VRM for the speaker since the Ardunino can only supply 200mA, the speaker needed more than that. So, the speaker is powered by the external VRM. 

# Pinout/Useful Links 
1. Arduino 
https://docs.arduino.cc/hardware/uno-rev3
3. Accelerometer to Arduino 
https://howtomechatronics.com/tutorials/arduino/arduino-and-mpu6050-accelerometer-and-gyroscope-tutorial/
4. Ultrasonic to Arduino 
https://create.arduino.cc/projecthub/abdularbi17/ultrasonic-sensor-hc-sr04-with-arduino-tutorial-327ff6 
5. Voltage Regulator Module (VRM) - pinout for this is in the product on amazon, you can find the link in the bill of materials. 




# Code 

```cp
<#include <MPU6050.h>
#include <Wire.h>

const int MPU_ADDR = 0x68; 
float lastAccX=0.0f,lastAccY=0.0f,lastAccZ=0.0f;
/*PINS*/
#define SPEAKER_PIN 7
#define TRIG_PIN 3
#define ECHO_PIN 2
#define G_PIN 12
#define D_PIN 11
#define A_PIN 10
#define E_PIN 9
/*Supported strings*/
#define STRING_G 0
#define STRING_D 1
#define STRING_A 2
#define STRING_E 3
/*Ultrasonic sensor constants*/
#define MAX_DISTANCE_CMS 70

/*Define note frequencies*/
unsigned int frequency_table[4][5] ={
  {220,262,329,392,440}, //G
  {156,185,208,233,277}, //D
  {123,147,175,196,220}, //A
  {92,104,117,139,156} //E
};

float previous_pitch=0.0;

void setup() {
  Serial.begin(9600);
  pinMode(TRIG_PIN, OUTPUT);
  pinMode(ECHO_PIN, INPUT);
  
  pinMode(G_PIN, INPUT);
  pinMode(D_PIN, INPUT);
  pinMode(A_PIN, INPUT);
  pinMode(E_PIN, INPUT);
  
  //Setup MPU6050
  Wire.begin();
  Wire.beginTransmission(MPU_ADDR);
  Wire.write(0x6B); //Talk to register 6B
  Wire.write(0x00); //Reset MPU
  Wire.endTransmission(true);
  delay(20);//allow reset
}
/**
 * The main loop
 */
void loop() {
  if(is_string_plucked() == true){
    int string_pressed = get_string_pressed();
    if(string_pressed == -1) return;
    int pluck_index = get_pluck_distance_index();
    int frequency_to_play = frequency_table[string_pressed][pluck_index];

    Serial.print("P=");Serial.print(string_pressed);Serial.print(",D=");Serial.print(pluck_index);Serial.print(",F="); Serial.println(frequency_to_play);
    play_note(frequency_to_play*10);  
  }
}

/*Function to check which note is pressed*/
int get_string_pressed(){
  int gPin = digitalRead(G_PIN);
  int dPin = digitalRead(D_PIN);
  int aPin = digitalRead(A_PIN);
  int ePin = digitalRead(E_PIN);

  if(gPin == LOW) return STRING_G;
  if(dPin == LOW) return STRING_D;
  if(aPin == LOW) return STRING_A;
  if(ePin == LOW) return STRING_E;

  return -1;
}

/*
 * Function to check the distance index of the pluck. 
 * Untrasonic sensor returns distance between 0-1183 cm. We divide this whole length into
 * 20 equal units (because, our frequency table has 20 steps per string).
*/
int get_pluck_distance_index(){
  /*Read ultrasonic sensor*/
  float distance = read_distance();
  int index = distance / (MAX_DISTANCE_CMS / 20);
  return index;
}


/*Function to check if the guitar string is plucked*/
boolean is_string_plucked(){
  //Read accelerometer
  Wire.beginTransmission(MPU_ADDR);
  Wire.write(0x3B);// Start with register 0x3B (ACCEL_XOUT_H)
  Wire.endTransmission(false);
  Wire.requestFrom(MPU_ADDR, 6, true);
  //For a range of +-2g, we need to divide the raw values by 16384, according to the datasheet
  float accX = (Wire.read() << 8 | Wire.read()) / 16384.0;
  float accY = (Wire.read() << 8 | Wire.read()) / 16384.0;
  float accZ = (Wire.read() << 8 | Wire.read()) / 16384.0;

  float diffX = fabs(lastAccX - accX);
  float diffY = fabs(lastAccY - accY);
  float diffZ = fabs(lastAccZ - accZ);
  //TODO::For now, we are using breadboard, therefore, we will check acc in Y direction only
  //Serial.print("diffX=");Serial.print(diffX);Serial.print(",diffY=");Serial.print(diffY);Serial.print(",diffZ=");Serial.println(diffZ);
  return( diffY >= 0.1);
}
/*PLay a note based on the pluck distance and the string pressed*/
void play_note(int frequency){

  /*int start_time = millis();
  int end_time = start_time;

  while ((end_time-start_time) <= 100){
    
    int time_period = 1/frequency;
    int on_time = time_period / 2;
    int off_time= time_period / 2;
    digitalWrite(SPEAKER_PIN,HIGH);
    delayMicroseconds(on_time);
    digitalWrite(SPEAKER_PIN,LOW);
    delayMicroseconds(off_time);

    end_time = millis();
  }*/
  noTone(SPEAKER_PIN);
  tone(SPEAKER_PIN,frequency,10);
}

/*Reads the distance between the transmitter and the reciever of the ultrasonic sensor*/
float read_distance(){
  // Clears the trigPin condition
  digitalWrite(TRIG_PIN, LOW);
  delayMicroseconds(2);

  //turning on TRIG_PIN 
  digitalWrite(TRIG_PIN, HIGH);
  delayMicroseconds(10);
  digitalWrite(TRIG_PIN, LOW);

  // Reads the echoPin, returns the sound wave travel time in microseconds
  int duration = pulseIn(ECHO_PIN, HIGH);
  
  // Calculating the distance
  float distance = duration * 0.034 / 2; // Speed of sound wave divided by 2 (go and back)

  //Serial.print("Distance= "); Serial.println(distance); 
  return distance; 
    
}>
```
