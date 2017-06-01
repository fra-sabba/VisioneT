# VisioneT
<img align="left" src="/img/logo.png" width="70px">The web is changing our life style. Neverthless, the older people can't benefit from this technology because required new methods of interation that are not usual for them. To overcome this obstacle, we create **VisioneT**, a *new concept* of *Internet*. 

## Description
**VisioneT** is an innovative *platform* that you can combine with every type of TV. It lets you *zapping* through web pages using a standard *remote control*. Each of these web pages is a *channel* created with contents selected from Internet depending on the user *profile*, his *emotions* and his *preferences*. In this way we developed a *modular* and *custom* system.

## Platform Layout
This picture shows the platform layout that was realized and tested.

<img align="center" src="/layout/platform-layout.jpg" width="600px">

The Raspberry/TJBot is connected to the TV with an HDMI cable and It is placed near the monitor. An IR transmitter (**1**) and an IR receiver (**2**) are wired to the Raspberry/TJBot. The *remote control* of the *TV* is *put aside* and an *another standard remote control is taken* (**3**, we called It *VisioneT controller*). The commands from the *VisioneT controller* are received by the Raspberry/TJBot and It makes a choose:
-	**If the VisioneT system is OFF**, the commands are transmitted to the TV by the IR transmitter, so you can *control* the *TV* as *usual* (If TV has the support for the CEC protocol, the commands could be sent through the HDMI cable, but this instance is not implemented now);
-	**If the VisioneT system is ON**, the commands are not transmitted to the TV and they are used to *control* the *system* and *zap* trough the *VisioneT’s channels*.

A *button* of the *VisioneT controller* is selected to turn ON/OFF the VisioneT system.

## Requirements
| Hardware      | Software    |
| :-------------: |:-------------:|
| [Raspberry Pi 3](https://www.amazon.com/dp/B01C6Q2GSY/ref=wl_it_dp_o_pC_nS_ttl?_encoding=UTF8&colid=1BLM6IHU3K1MA&coliid=I1WPZOVL411972)<br>|[Raspbian Jessie](https://www.raspberrypi.org/downloads/raspbian/)|
| [IBM TJBot](http://ibm.biz/mytjbot): <br>you can 3D print or laser cut the robot |[Node RED](https://nodered.org/)|   
| USB 2.0 microphone | [LIRC](http://www.lirc.org/)|
| IR receiver |[IBM Watson](https://www.ibm.com/watson/developercloud/) services: <br> Text To Speech, Speech To Text and Tone Analyzer|
| IR emitter|

## Setup Prototype
### Step 0 Prepare Raspberry/TJBot
- Follow the step-by-step instructions on [Instructables](http://www.instructables.com/member/TJBot/instructables/) to assemble and prepare your RaspberryPi/TJBot to run the code.

### Step 1 Setup Node RED
- Follow the instructions on [Node RED site](https://nodered.org/docs/hardware/raspberrypi) to install Node RED on the Raspberry Pi 3. 
- Install the required Node-RED nodes:
    - [IBM Watson Services](https://flows.nodered.org/node/node-red-node-watson) (node-red-node-watson)
    - [Dashboard](node-red-dashboard) (node-red-dashboard)
    - [Feed Parser](node-red-node-feedparser) (node-red-node-feedparser)
    - [Weather report](https://flows.nodered.org/node/node-red-node-openweathermap) (node-red-node-openweathermap)
    - [Chat bot](https://flows.nodered.org/node/node-red-contrib-chatbot) (node-red-contrib-chatbot)
    - [Inter Process Comunication](https://flows.nodered.org/node/node-red-contrib-ipc)   (node-red-contrib-ipc)
    - [Youtube Data API](https://flows.nodered.org/node/node-red-node-youtube) (node-red-node-youtube)

You will then need to restart Node-RED. To start Node-RED, run the command `node-red-start`. To stop Node-RED, run the command `node-red-stop`.

### Step 2 Setup and configure LIRC
- Follow the steps 8 and 9 of the this [guide](http://www.instructables.com/id/How-To-Useemulate-remotes-with-Arduino-and-Raspber/#step8) to wire the hardware(IR receiver and trasmitter) and configure LIRC on Raspberry Pi.

*more details soon!*

### Step 3 Setup USB microphone
*details soon!*

### Step 4 Download flow
*details soon!*

## License
This project is licensed under Apache 2.0.  
