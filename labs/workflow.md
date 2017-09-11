> [Internet of Things (IoT) | Training Course](workflow.md) ▸ **Workflow**

# Workflow

[1. Pycom typical workflow](#pycom-typical-workflow)
[2. Resetting your device](#resetting)

## Pycom typical workflow

A typical workflow is the following:
1. Open Atom
2. Add a project folder: `top menu ► File ► Add Project Folder...`
3. Plug your device into your USB port
4. Update Pymakr settings (connection via USB or WiFi)
5. Connect
6. Write your code
7. Run your code for debugging
8. Sync your code once done

These steps are illustrated in the following YouTube video: 

https://www.youtube.com/watch?v=L1CmWsZlCeU

Instead you might want to connect to your device via WiFi

1. Simply connect your computer to device's WiFi:

![img/lopy-wifi.png](http://i.imgur.com/7GbsuFk.png)

2. Reset Pymakr settings to default (no usb device address)

And that's all.

## Resetting
They are different ways to reset your device:

1. Soft reset

`ctrl+D` in Pymarkr plugin console.

2. Formating device's `/flash` folder
```python
import os
os.mkfs('/flash')
```
then reboot.

## Fetching data from the Lopy with Filezilla

> Warning: Your device's WiFi should be in Acces Point mode.

To establish a connection with your device:

1. Connect to device's WiFi


![img/filezilla-settings.png](http://i.imgur.com/SAN02Pa.png)
