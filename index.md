# Arduino Air Guitar
This is an Airduino Air Guitar, consisting of two parts, a glove and a strummer. Using the glove one can choose which note to play and the strummer helps in choosing the pitch and strum the guitar, imitating a normal guitar. 

 | **Engineer**|**School** |**Area of Interest** |**Grade** | 
 |:--:|:--:|:--:|:--:|
 | Vedika S. |Cupertino High School |Electrical Engineering |Incoming Senior|


<img src="https://user-images.githubusercontent.com/72050310/180516357-11ce3a2c-c6c2-44a1-87a5-e348b9397158.jpg" width="300" height="400"/>


# Project Picture 
<img src= "https://user-images.githubusercontent.com/72050310/180518314-00cac4af-10e9-4404-a8d4-ea1087dc9ce2.jpg" width = "400" height = "200"/>

# Project Video 
<video src="https://user-images.githubusercontent.com/72050310/180522914-b6111730-d223-4188-ae10-3517eb8f7634.mp4" controls="controls" style="max-width: 730px;">
</video>
  
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
| Breadboard | 1 | $2.99/count |https://tinyurl.com/yc8njk2w  |
| Wires | 20 | $0.06/count |https://tinyurl.com/4f9u42mw |
| Arduino | 1 | $27 |https://tinyurl.com/4e8n27yw |
| Speaker/Amplifier | 1 | $11.99 | https://tinyurl.com/wwpmkfcx |
| Accelerometer | 1 | $3.33/count | https://tinyurl.com/5896vvbk |
| Ultrasonic Sensor | 1 | $1.83/count | https://tinyurl.com/3c6zuk3w |
| Soldering Kit | 1 | $19.99 | https://tinyurl.com/3embv5ct |
| Glove | 1 | $5.99 | https://tinyurl.com/myjw8ejd |
| Hot Glue Gun | 1 | $14.99 | https://tinyurl.com/5c53sdv5 |
| Resistors | 4 | $1.04/count | https://tinyurl.com/5yb2psfc |
| Conductive Fabric | 1 | $15.99 |https://tinyurl.com/vr52v38t |


# Schematic 
NOTE: The pins on the Arduino Uno do not represent the actual orientation, it is simply a reference. Please refer to the Ardunino Pinout (and other pinouts) linked below. 

<img src="https://user-images.githubusercontent.com/72050310/180590632-e17755ef-0d13-4bf6-8d67-355a4af92291.png" width="400" height="200"/>


In my project, I used an external VRM for the speaker since the Ardunino can only supply 200mA, the speaker needed more than that. So, the speaker is powered by the external VRM. 

# Pinout/Useful Links 
1. Arduino - https://docs.arduino.cc/hardware/uno-rev3
3. Accelerometer to Arduino - https://howtomechatronics.com/tutorials/arduino/arduino-and-mpu6050-accelerometer-and-gyroscope-tutorial/
4. Ultrasonic to Arduino - https://create.arduino.cc/projecthub/abdularbi17/ultrasonic-sensor-hc-sr04-with-arduino-tutorial-327ff6 
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
