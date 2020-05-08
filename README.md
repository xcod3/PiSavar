### PiSavar  - Detects PineAP module and starts deauthentication attack (for fake access points - WiFi Pineapple Activities Detection)

<p align="center">
<img src="https://github.com/besimaltnok/pineAPhunter/blob/master/pineapple.png" width="200" height="300">
</p>

<p align="center">
<img src="https://img.shields.io/badge/Python-3-yellow.svg"></a> <img src="https://img.shields.io/badge/license-GPLv3-red.svg">
<a href="http://www.blackhat.com/eu-17/arsenal/schedule/#wipi-hunter---wifi-pineapple-activities-detection-9091"><img src="https://rawgit.com/toolswatch/badges/master/arsenal/europe/2017.svg"></a>
<a href="https://www.blackhat.com/asia-18/arsenal/schedule/index.html#wipi-hunter---detects-illegal-wireless-network-activities-9854"><img src="https://rawgit.com/toolswatch/badges/master/arsenal/asia/2018.svg"></a>
<a href="https://defcon.org/html/defcon-26/dc-26-demolabs.html#WiPi-Hunter"><img src="https://hackwith.github.io/badges/defcon/26/demolabs.svg"></a>
</p>

### About Project

The goal of this project is to find out the fake access points opened by the WiFi pineapple device using the PineAP module and to prevent clients from being affected by initiating a deauthentication attack to the attacking device.


### How PineAP Module Works

* Collects SSID information
* Creates SSID pool with collected SSID information
* Creates fake access points using information in the SSID pool

<img src="images/pineap_2.png" width="100%"></img>

### Where is the problem?

- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `One MAC address, more than one SSID information .... ..- -. - . .-. `


### Features of PiSavar

* Detects PineAP activities. 
* Detects networks opened by PineAP.
* Starts deauthentication attack for PineAP.

### Features to add

* List of clients connected to fake access points
* Record activities - Logging

#### Diagram

<img src="images/info.png" width="50%"></img>

### --------------------------------------------------------------------------------

### Usage

#### Requirements

* **Hardware:** TP LINK TL-WN722N
* **Modules:** scapy, time, termcolor, argparse, commands, netifaces, logging

#### Parrot OS or Kali Linux:

Download pisavar:

`git clone https://github.com/xcod3/PiSavar.git`

Install Python librarie(s):

`pip3 install termcolor`

It's done!

Run the program with following command: 

Monitor mode:

```python
airmon-ng start interface(wlan0,wlan1) (Monitor mode)

or 

ifconfig wlan0 down
iwconfig wlan0 mode Monitor
ifconfig wlan0 up
```

Run:

```python
cd PiSavar
python3 pisavar.py -h
```

### Screenshots
<img src="images/pisavar_attack.png" width="45%"></img>
<img src="images/pisavar_detect.png" width="42%"></img>
<img src="images/pisavar_log2.png" width="39%"></img>
<img src="images/help.png" width="45%"></img>

### Demo Video

+ new: https://www.youtube.com/watch?v=zJZkPz9ZPMk
+ old: https://youtu.be/P7mfh37NZc0

### Authors
This project is coded by Besim ALTINOK
