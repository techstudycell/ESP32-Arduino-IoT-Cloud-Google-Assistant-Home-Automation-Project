# ESP32-Arduino-IoT-Cloud-Google-Assistant-Home-Automation-Project
In this IoT project, I have shown how to make an IoT-based Home Automation with Arduino IoT Cloud & Google Assistant using ESP32 to control 4 home appliances with voice commands.

You can manually control the home appliances with switches and an IR remote if the internet is unavailable. During the article, I have shown all the steps to make this smart home system.

## Tutorial Video on this ESP32 IoT Project
Tutorial video link: [https://youtu.be/gpoO7kYXzm4](https://youtu.be/UlT72MMbPu8)

This IoT-based Home Automation system has the following features:

1. Control appliances with Google Home and Arduino IoT Cloud Dashboard.
2. Control the relays with the IR remote.
3. Control appliances manually with switches.
4. Control home appliances manually without the internet.
5. Monitor real-time feedback and room temperature in the Amazon Alexa app.
6. All resources used for this project are FREE.

## Required Components:
So, you can easily make this home automation project at home just by using an ESP32, DHT11 sensor, 1838 IR receiver, and relay module. Or you can also use a custom-designed PCB for this project.

## Required Components for PCB:
1. ESP32 DEVKIT V1
2. DHT11 sensor
3. 1838 IR receiver (with metallic case)
4. Relays 5v (SPDT) (4 no)
5. BC547 Transistors (5 no)
6. PC817 Optocuplors (4 no)
7. 510-ohm 0.25-watt Resistor (5 no) (R1 - R5)
8. 1k 0.25-watt Resistors (7 no) (R6 -- R12)
9. Hi-Link HLK-5M05 AC to DC converter.
10. LED 5-mm (7 no)
11. 1N4007 Diodes (4 no) (D1 - D4)
12. Push Buttons (1 no)
13. Terminal Connectors
14. 5V DC supply

## Circuit Diagram of the ESP32 Home Automation Project
The circuit is very simple, I have used the GPIO pins D23, D19, D18 & D5 to control the 4 relays.

And the GPIO pins D13, D12, D14 & D27 are connected with switches to control the 4 relays manually.

I have used the INPUT_PULLUP function in Arduino IDE instead of using the pull-up resistors.

IR remote receiver (TSOP1838) connected with D35. And the DHT11 sensor connected with D4.

I have used a 5V mobile charger to supply the smart relay module.

Please take proper safety precautions while working with high voltage.

## Google Assistant Control Relay Using ESP32
You can control the home appliances from the Google Home App or Google Assistant with voice commands and also monitor the room temperature if the ESP32 is connected to Wi-Fi.

You can also ask Google Assistant to turn on and off the appliances from anywhere in the world.

## ESP32 Control Relays With Arduino IoT Cloud Dashboard
You can also monitor the room temperature and control the home appliances from the Arduino IoT Cloud web dashboard and Arduino IoT Cloud Remote mobile app if the ESP32 is connected to WiFi.

In this project, I have used the FREE plan of Arduino IoT Cloud. In the FREE plan, you can control maximum of 5 relays or sensors.

When you control the relays from the Arduino IoT Cloud Remote mobile app the current state of the relay is also updated in the Google Home app.

## Control Relays With IR Remote & Switches
You can always control the relays with IR remote and switches.

I will explain how to get the IR codes (HEX codes) from any remote in the following steps.

If the ESP32 is connected to Wi-Fi, then you can also monitor the real-time feedback in the Google Home App & Arduino cloud dashboard.

When the WiFi is available, the ESP32 will automatically reconnect with the WiFi.

## Design the PCB for This Smart Home System
To make the circuit compact and give it a professional look, I designed the PCB after testing all the features of the smart relay module.

You can download the PCB Gerber file of this home automation project from the following link:
https://github.com/techstudycell/ESP32-Arduino-IoT-Cloud-Google-Assistant-Home-Automation-Project/tree/main/PCB_Gerber

## Why you should order from JLCPCB?
On JLCPCB's one-stop online platform, customers enjoy low-cost & high-quality & fast SMT service at an $8.00 setup fee($0.0017 per joint).

New User coupons & SMT coupons every month.
Visit [https://jlcpcb.com](https://jlcpcb.com/RNA)

Currently, on JLCPCB, we have launched several promotions for multilayer PCB prototyping. We no longer have extra charges for via-in-pad on 6-20 layer PCBs.
https://jlcpcb.com/blog/42-special-offer-for-6-8-layer-high-precision-pcbs

How does JLC Via-in-pad optimize routing efficiency? https://jlcpcb.com/6-layer-pcb

JLCPCB's newly launched Multi-color Silkscreen service, allows you to incorporate any image design you like onto your PCB.
https://jlcpcb.com/blog/653-multi-color-silkscreen-pcb

## Steps to Order the PCB from JLCPCB
1. Visit [https://jlcpcb.com](https://jlcpcb.com/RNA) and **Sign in / Sign up.**
2. Click on the **QUOTE NOW** button.
3. Click on the "**Add your Gerber file**" button. Then browse and select the Gerber file you have downloaded.
4. Set the required parameters like **Quantity, PCB masking color**, etc.
5. Select the **Assemble side** and SMT Quantity (For PCB Assembly service only).
6. Now upload the **BOM and PickAndPlace files** (For PCB Assembly service only).
7. Now **confirm all the components** that you want to be soldered by SMT services (For PCB Assembly service only).
8. Click on the "**SAVE TO CART** button.
9. Type the **Shipping Address**.
10. Select the **Shipping Method** suitable for you.
11. Submit the order and proceed with the **payment**.

## Create Arduino IoT Cloud FREE Account
For this smart house project, I have used the Arduino IoT Cloud Free plan.

Click on the following link to create an Arduino IoT Cloud account.
https://cloud.arduino.cc/

1. Click on "GET STARTED FOR FREE".
2. Enter the email ID, user name, set password. Then click on "Sign Up".
3. Click on "Create New", and select "Thing".
4. Give a name, then click on "Rename".
5. Click on the Configure button under Smart Home Integration. Then select Google Home.

## Add ESP32 Device in the Arduino IoT Cloud
1. Click on the Select Device on the right
2. Select "Set up New device".
3. Select "Third Party device",
4. You will get a Device ID and Secret Key which will be required in the code.
5. Click on "Continue", You will find the device added.

## Add Variables Under Thing in Arduino IoT Cloud
Now to control 4 relays, and get reading from the DHT11 sensor, you have to add 5 variables.

1. Click on the "ADD" button.
2. Enter a name, then select Google-compatible light type. Variable Permission will be "Read & Write" and Variable Update Policy will be "On Change".
3. Similarly, you have to add the next 3 variables.
4. For the room temperature, reading select Google compatible Temperature Sensor. Variable Update Policy will be "Periodically", and mention the interval time.

## Set Up Arduino IoT Cloud Dashboard

1. Now click on Dashboard on the top to set up the Arduino cloud dashboard.
2. Then click on Build Dashboard. After that click on the EDIT icon.
3. Then click on ADD and select Switch.
4. Give a name to this Switch, then link a variable with this switch widget.
5. Then click on Done.
6. Similarly, you have to add total 4 Switch widgets to control 4 relays.
7. For the temperature, select Gauge widgets and link the Temperature variable. You can also set the MIN and MAX limits.

## Get the IR Codes (HEX Code) From the IR Remote
Now, to get the HEX codes from the remote, first, we have to connect the IR receiver output pin with GPIO D35.

And give the 5V across the VCC and GND. The IR receiver must have a metallic casing, otherwise, you may face issues. Then follow the following steps to get the HEX codes.

1. Install the IRremote library in Arduino IDE.
2. Download the attached code, and upload it to ESP32. (Check below)
3. Open Serial Monitor with Baud rate 9600.
4. Now, press the IR remote button.
5. The respective HEX code will populate in the serial monitor.
6. Save all the HEX codes in a text file.

### Code for Getting HEX code from IR remote: 
https://github.com/techstudycell/ESP32-Arduino-IoT-Cloud-Google-Assistant-Home-Automation-Project/blob/main/Code/Code_IR_Button_HEX_Code/Code_IR_Button_HEX_Code.ino

### Main sketch for the ESP32 IOT Project
https://github.com/techstudycell/ESP32-Arduino-IoT-Cloud-Google-Assistant-Home-Automation-Project/blob/main/Code/Code_ESP32_ArduinoIotCloud_Google_IR_4Relays_Switch/Code_ESP32_ArduinoIotCloud_Google_IR_4Relays_Switch.ino

## Program the ESP32 With Arduino IDE
To program the ESP32, I have used Arduino IDE.

Download the attached code.

First, you have to install the ArduinoIoTCloud library. During installation, it may ask to install other dependencies. Then click on Install All.

In the code, enter the following details.

const char DEVICE_LOGIN_NAME[] = ""; //Enter DEVICE ID
const char SSID[]        = "";  //Enter WiFi SSID (name)
const char PASS[]        = "";  //Enter WiFi password
const char DEVICE_KEY[]     = "";  //Enter Secret device password (Secret Key)
The DEVICE_LOGIN_NAME[] and DEVICE_KEY[] from the PDF that you have downloaded while adding the device to the Arduino IoT cloud.

Then update the HEX codes to control the relays from the IR remote.

switch(results.value){
          case 0x80BF49B6:  relayOnOff(1); light1 = toggleState_1; break; //update the HEX-code
          case 0x80BFC936:  relayOnOff(2); light2 = toggleState_2; break; //update the HEX-code
          case 0x80BF33CC:  relayOnOff(3); light3 = toggleState_3; break; //update the HEX-code
          case 0x80BF718E:  relayOnOff(4); light4 = toggleState_4; break; //update the HEX-code
          default : break;         
        }

I have shown all the steps in the tutorial video. After making all these changes, you can upload the code to ESP32.

## Configure the Google Home App for Arduino IoT Cloud
First, download and install the Google Home App. then follow the steps:

1. Open the Google Home app and create a Home.
2. Then click on "+" and select "Set up device", the " works with Google".
3. Now search for "Arduino", and log in to the Arduino IoT Cloud account.
4. All the devices from Arduino IoT Cloud will be added to Google Home.

Now you can also control the appliances with voice commands using Google Assistant.

## Finally!! the Arduino Cloud Smart Home System Is Ready
Connect the 4 home appliances with the relay module as per the circuit diagram.

Please take proper safety precautions while working with high voltage.

Now you can smartly control your home appliances.

I hope you have liked this Arduino IoT and Google Assistant home automation project. I have shared all the required information for this project.

I would appreciate it if you share your valuable feedback. Also if you have any queries please write in the comment section.

Thank you & Happy Learning.
