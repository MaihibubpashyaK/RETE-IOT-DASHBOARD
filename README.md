# RETE-IOT-DASHBOARD


https://www.myelectronicslab.com/iot/esp8266-mqtt-iot-device-control-rete-iot-dashboard-tutorial/

https://www.youtube.com/watch?v=-bzQ87t4Ev0

Rete #1 Control Your Home From Any where using ESP8266 – MQTT IOT Dashboard
Posted by: satya sankar sahoo Posted date: July 11, 2017 In: IOT, Tutorial




Hello Friends,

I know , I am writing this post after a long time, I am really sorry for posting after a long time. As I am busy with my new job and shifting my home, I could not write. But from now onward I will try to like at least 2 blogs per month.

If you have watch above video, this article is just the written explanation for that video.

In this article we will learn  MQTT, Control ESP8266 from web using MQTT protocol.

 

If you are new to MQTT , I will strongly request you to study MQTT basics here. This is a really nice tutorial.

MQTT have three thing
MQTT Broker – who receive and distribute messages – in our case “mqtt://io.reteiot.com“
MQTT Topic – Topic is the channel where client/server can send or receive messages. “EmailID/Light”
MQTT client – Client can publish(send)/subscribe(Receive) messages to/From other client via broker. “ESP8266”
Try to understand the below image , How publish and subscribe works.

mqtt-explanation

 

For this experiment You need.
ESP8266 board – Node MCU or Wemos
LED
USB Cable
Jumper
Breadboard
 

Circuit Diagram.
wemos-d1-r2-mini-circuit-diagram-rete-iot

Connect Positive Pin(Anode) of LED to the D0 pin of wemos (ESP8266) and other pin of led to GND. This is a simple circuit and I think it don’t need any explanation.

Code:
Download the complete code here.

The Zip contains one arduino library called “pubsubclient.zip”. This is the MQTT library. You need to install this arduino  library.

Once you have install the arduino library. Open the rete-lightSwitch.ino file.

 

Rete IOT Dashboard:
Now Go to browser. and open http://reteiot.com and click on login.  You have to create one account.

Once you have created the account Login to the dashboard. The dashboard seems something like this.

rete-iot-dashboard

This dashboard have so many features. But we will only focus on “Switch Control” .  To control switch, the MQTT topic name will be your emailid/Light. Let say your email id is xyz@gmail.com then topic name will be “xyz@gmail.com/Light” .

 

In arduino IDE, change the topic name to “YouremailID/Light”, also change your wifi SSID and password.

Compile and upload the code.

Open console log of Arduino IDE. and go to Rete IOT dashboard. You can now control your LED from the dashboard.

Conclusion:
Now your turn. Put some thought process and make something cool using MQTT dashboard. You can add one relay in place of LED and control your home appliances. If you are new to electronics and don’t know how to interface relay, you can follow my video tutorial on relay control.
