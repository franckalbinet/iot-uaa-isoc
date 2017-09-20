
> [Internet of Things (IoT) | Training Course](setting-up-a-raspberry.md) ▸ **Setting up a Raspberry PI 3**

## Setting up a Raspberry PI 3
This tutorial is optional and will outline the installation required steps including:

[1. copying an Ubuntu Mate image to an SD card](#copying-the-ubuntu-mate-image)

[2. installing Ubuntu Mate]()

[3. enabling SSH]()

[4. identifying IP address]()

[5. installing Mosquitto MQTT (clients, publishers and broker)]()

[6. setting up a LoRa Gateway (with LoRa expansion board)]()

[7. setting up a Flask API]()

## Copying the Ubuntu Mate image

Ubuntu Mate can be downloaded here: https://ubuntu-mate.org/raspberry-pi/ This link also includes guidance on how to extract and copy the image to an SD card using for instance Win32 Disk Imager if you are using a Windows OS. This video shows how to use Win32 Disk Imager: https://www.youtube.com/watch?v=WCrNIyhPXcs

The steps below outline how to do so under MAC OSX (http://terraltech.com/copying-an-image-to-the-sd-card-in-mac-os-x/):

```console
# Install .xz unarchiver
brew install xz

# Unarchive
xz -d ubuntu-mate-16.04.2-desktop-armhf-raspberry-pi.img.xz

# Displays disk usage information based on file system (ie: entire drives, attached media, etc)
# First without connecting the SD card to USB, list devices
df -h

# Connect your SD card and noticed the added device in the list: for instance: "/dev/disk1s1"
df -h

# Unmount the partition so that you will be allowed to overwrite the disk
sudo diskutil unmount /dev/disk1s1

# Write image on the raw device: if the mounted identifier is "disk1s1", 
# we will write to the raw device identifier "rdisk1"

# Using the device name of the partition work out the raw device name for the entire disk, by omitting the final “s1” and replacing “disk” # with “rdisk”. Exemple: /dev/disk1s1 -> /dev/rdisk1
sudo dd bs=1m if=ubuntu-mate-16.04.2-desktop-armhf-raspberry-pi.img of=/dev/rdisk1

# After the dd command finishes, eject the card

# Eject the card
sudo diskutil eject /dev/rdisk1
```






