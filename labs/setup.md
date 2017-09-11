> [Internet of Things (IoT) | Training Course](setup.md) ▸ **Setup**

# Course setup

[1. Installing Atom editor](#installing-atom-editor)

[2. Installing Atom Pymakr plugin](#installing-atom-pymakr-plugin)

[3. Upgrading Pycom boards firmwares](#upgrading-pycom-boards-firmwares)

[4. Installing Filezilla](#installing-filezilla)

[5. Troubleshooting](#troubleshooting)

## Installing Atom editor
Atom is an Integrated Development Environment (**IDE**), providing convenient features to edit Python code (among many others): syntax highlighting, completion, auto-indentation, integration with Git, bash, ...

We will use Atom to write Python code during the labs sessions. 

To install it, download the installation file for your Operating System here: [https://atom.io/](https://atom.io/)

## Installing Atom Pymakr plugin
The Python code written will not be executed in your local machine. Instead, you need to transfer it to your IoT device (in our case Pycom Lopy). To do so, [Pycom](https://www.pycom.io/) developed a plugin named **Pymakr** that will facilitate the execution and syncing of Python to the device.

To install the plugin in Atom:

1. Open Atom
2. In top menu: Atom ► Preferences...
3. And write `pymkr` in the input box under the `Install tab` (followed by `Enter`):

![img/install-pymkr.png](http://i.imgur.com/Of2NTPR.png)

## Installing FileZilla
FileZilla will be used occasionnaly to synchronize or retrieve file from IoT device via ftp and Wifi of the device itself.

Download the FileZilla ftp client here: https://filezilla-project.org/


## Troubleshooting
### USB-serial drivers

