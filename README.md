# VisioneT
![logo](../img/logo.png) The web is changing our life style. Neverthless, the older people can't benefit from this technology because required new methods of interation that are not usual for them. To overcome this obstacle, we create **VisioneT**, a *new concept* of *Internet*. 

## Description
**VisioneT** is an innovative *platform* that you can combine with every type of TV. It lets you *zapping* through web pages using a standard *remote control*. Each of these web pages is a *channel* created with contents selected from Internet depending on the user *profile*, his *emotions* and his *preferences*. In this way we developed a *modular* and *custom* system.

## Requirements
### Hardware
- [Raspberry Pi 3](https://www.amazon.com/dp/B01C6Q2GSY/ref=wl_it_dp_o_pC_nS_ttl?_encoding=UTF8&colid=1BLM6IHU3K1MA&coliid=I1WPZOVL411972)
- [IBM TJBot](http://ibm.biz/mytjbot): You can 3D print or laser cut the robot
- USB 2.0 microphone 
- IR receiver
- IR emitter
### Software
- [Raspbian Jessie](https://www.raspberrypi.org/downloads/raspbian/)
- [Node RED](https://nodered.org/)
- [LIRC](http://www.lirc.org/)
- [IBM Watson](https://www.ibm.com/watson/developercloud/) services: Text To Speech, Speech To Text and Tone Analyzer

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