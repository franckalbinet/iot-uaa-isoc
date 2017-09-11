> [Internet of Things (IoT) | Training Course](workflow.md) ▸ **Workflow**

# Workflow

[1. Pycom typical workflow](#pycom-typical-workflow)

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

These steps are illustrated in the following YouTube video: https://www.youtube.com/timedtext_video?v=L1CmWsZlCeU


1. Open Atom

2. Add a project folder: `top menu ► File ► Add Project Folder...`

![](https://i.imgur.com/Sae3Vrs.png?1)

Select for instance the `src/LED` folder. Make sure that's the only one

3. Plug your device into your USB port

4. Update Pymakr settings (connection via USB or WiFi)
You need to update Pymakr settings every time you want to connect to a new device or you want to change your connection mode (USB serial or WiFi):

Open the `Global Settings` tab: click on `Settings ► Global Settings` in Pymakr console

![](https://i.imgur.com/itJeytO.png?1)

Then identify your USB port: click on `More ► Get serial ports` in Pymakr console
  
![](https://i.imgur.com/UkUaDPx.png?1)
    
By now you should be able to:

5. Connect

6. Write your code

7. Run your code for debugging

8. Sync your code once done

### Updating Pymakr settings



* **Connect via USB serial**

See Pycom official documentation: https://docs.pycom.io/pycom_esp32/pycom_esp32/toolsandfeatures.html

To connect via USB serial you need to know to determine the serial address in which your Pycom device is connected, you will need to scan for connected devices on your computer.

For Mac user, you can simply run in a terminal the following command: `ls /dev/cu.*`

Alternatively, you can use directly the Pymakr console to get a list of devices: click on the `More` button and `Get Serial ports`.

Once identified your serial device you need to update Pymakr settings. In Pymakr console: 
`Settings ► Global settings`



> Note in screenshot above that you can specify a subfolder of your Atom project containing your code (will be seen in lab sessions).

* **Connect via WiFi**
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
