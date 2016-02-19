# raspberry pi

## first-time operations

If you boot up the raspberry-pi for the first time, you might want to setup and update some things. Always use `sudo` with those commands.

```bash
sudo raspi-config
sudo apt-get update
sudo apt-get upgrade
sudo rpi-update
sudo reboot
```

## tools

A fresh system might need some handy tools in the future. So think about installing the following:

* `sudo apt-get install python-pip`
* `apt-get install python-dev`
* `sudo apt-get install usb-modeswitch` 

## camera

If you are going to use the pi camera module, you might give the following libraries a shot:

* `sudo apt-get install python-picamera`

## commands
### network
```bash
ifconfig
```

```bash
ifup <interface>
ifdown <interface>
```

## settings
### audio
To use an external USB SoundCard you need to setup the right options within several places:

* `sudo raspi-config` Force Audio
* `sudo nano /etc/modprobe.d/alsa-base.conf` options snd-usb-audio index=-2
* `sudo nano /etc/modules` snd-bcm2835