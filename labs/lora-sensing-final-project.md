> [Internet of Things (IoT) | Training Course](lora-sensing-final-project.md) ▸ **LoRa sensing | Final project**

# LoRa sensing | Final project

## Introduction
In this lab. we will consider the following setup:

![](https://i.imgur.com/OV1b5aH.png)

where:
* LoPys on Pysense boards will make measurements and send it over LoRa;
* then Raspberry Pi and its LoRa expansion receiving it will serve them through an API;
* last, client machine(s) will fetch measurements via the API and anlyse it (using Jupyter Notebooks).

To be clear, again, communication between IoT nodes (Lopys+expansion board) and the Raspberry used as a LoRa gateway will be ensured via LoRa. As regards, communication between the client machines will be ensured via WiFi in a LAN. 

An example use case might be a farm where you deploy dozens of sensors to monitor temperature, humidity, soi moisture, CO2, ... in agricultural fields, aggregate the measurements in a Gateway and then analyse, monitor, decide using analytical platform.

## Learning outcomes


## LoRa node setup
...

## Setting up the Raspberry LoRa Gateway

To run the LoRa Gateway, in  `/raspi-lora-gateway` folder run the following command: `sudo ./gateway`


## Setting up the Flask API
```
pip install flask
sudo apt-get install python-pandas
```
In a terminal/console, run `export FLASK_APP=api.py`

in folder `/flask-api`, run `flask run --host=0.0.0.0`

Get the Raspberry Pi IP address: `hostname -I` for instance 192.168.1.101

Open your browser, you should be able to get data dumped by the LoRa Gateway by writing this URL `http://192.168.1.101:5000/gateway/api`

## Raspberry PI 3 setup and configuration

## Required Components



