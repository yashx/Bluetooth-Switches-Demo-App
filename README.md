# Bluetooth Switches Demo App
This is a basic Arduino Demo project for my Android app in Play Store.
[Bluetooth Switches: Arduino 26 Relay Controller](https://play.google.com/store/apps/details?id=com.github.yashx.arduinobluetoothswitcheshc_05andhc_06)
The aim is to explain how to interact with the app

## Video of the project 
[![Youtube Video](http://img.youtube.com/vi/SfY806KR6qE/0.jpg)](http://www.youtube.com/watch?v=SfY806KR6qE "Youtube Video")

## How to get it working
   
1. First Upload this Code to Arduino

   ```C
   char ch;
   int LED_1 = 3;
   int LED_2 = 4;
   int LED_3 = 5;
   int LED_4 = 6;
   int LED_5 = 7;
   int LED_6 = 8;
   int LED_7 = 9;
   int LED_8 = 10;
   int LED_9 = 11;
   int LED_10 = 12;



   void setup() {
     // put your setup code here, to run once:
    Serial.begin(9600);
    pinMode(LED_1,OUTPUT);
    pinMode(LED_2,OUTPUT);
    pinMode(LED_3,OUTPUT);
    pinMode(LED_4,OUTPUT);
    pinMode(LED_5,OUTPUT);
    pinMode(LED_6,OUTPUT);
    pinMode(LED_7,OUTPUT);
    pinMode(LED_8,OUTPUT);
    pinMode(LED_9,OUTPUT);
    pinMode(LED_10,OUTPUT);
 
   }

   void loop() {
     // put your main code here, to run repeatedly:

   if(Serial.available()){
       ch = Serial.read();
       Serial.write(ch);
       doWork(ch);
     }
   }

   void doWork(char ch){
     switch(ch){
       case 'A': //code for switch 1 turned on
                 digitalWrite(LED_1,HIGH);
                 break;
       case 'a': //code for switch 1 turned off
                 digitalWrite(LED_1,LOW);
                 break;
       case 'B': //code for switch 2 turned on
                 digitalWrite(LED_2,HIGH);
                 break;
       case 'b': //code for switch 2 turned off
                 digitalWrite(LED_2,LOW);
                 break;
       case 'C': //code for switch 3 turned on
                 digitalWrite(LED_3,HIGH);
                 break;
       case 'c': //code for switch 3 turned off
                 digitalWrite(LED_3,LOW);
                 break;
       case 'D': //code for switch 4 turned on
                 digitalWrite(LED_4,HIGH);
                 break;
       case 'd': //code for switch 4 turned off
                 digitalWrite(LED_4,LOW);
                 break;      
       case 'E': //code for switch 5 turned on
                 digitalWrite(LED_5,HIGH);
                 break;
       case 'e': //code for switch 5 turned off
                 digitalWrite(LED_5,LOW);
                 break;
       case 'F': //code for switch 6 turned on
                 digitalWrite(LED_6,HIGH);
                 break;
      case 'f':  //code for switch 6 turned off
                 digitalWrite(LED_6,LOW);
                 break;
      case 'G':  //code for switch 7 turned on
                 digitalWrite(LED_7,HIGH);
                 break;
      case 'g':  //code for switch 7 turned off
                 digitalWrite(LED_7,LOW);
                 break;
      case 'H':  //code for switch 8 turned on
                 digitalWrite(LED_8,HIGH);
                 break;
      case 'h':  //code for switch 8 turned off
                 digitalWrite(LED_8,LOW);
                 break;
      case 'I':  //code for switch 9 turned on
                 digitalWrite(LED_9,HIGH);
                 break;
       case 'i': //code for switch 9 turned off
                 digitalWrite(LED_9,LOW);
                 break;
      case 'J':  //code for switch 10 turned on
                 digitalWrite(LED_10,HIGH);
                 break;
      case 'j':  //code for switch 10 turned off
                 digitalWrite(LED_10,LOW);
                 break;
      // Similarly for others
     }
   }
   ```
   

2. Then make the circuit as shown here

   ![Circuit Diagram](/led%20demo_bb.png?raw=true)
   
   **Don't connect HC 05 when you are uploading code to Arduino as you may get errors**
   
3. Pair the module with your phone

   The pairing code will be 1234 or 0000
   
4. Download and Use the App

   [Play Store Link](https://play.google.com/store/apps/details?id=com.github.yashx.arduinobluetoothswitcheshc_05andhc_06 "Bluetooth Switches: Arduino 26 Relay Controller")
   
