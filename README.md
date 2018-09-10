# AirPlayPi
Eine Sammlung aller erforderlichen Hinweise, um einen AirPlay Lautsprecher mit Hilfe eine Pi Zero W zu basteln.

Verwendet habe ich einen Raspberry Pi Zero W, sowie das Adafruit I2S Stereo Decoder - UDA1334A Breakout Board.


>  wpasupplicant.conf

Diese Datei auf der Boot Partition des Pi erzeugen, um direkt nach dem Booten Zugang zum Netzwerk zu haben.

>  ssh

Diese Datei (ohne Erweiterung auf der Boot Partition des Pi erzeugen, um nach dem Booten ssh Zugang zu haben.

> curl https://get.pimoroni.com/phatdac | bash

Dieses Script nimmt alle Einstellungen vor, um den DAC zu verwenden

Installation von shairport: (https://thepi.io/how-to-set-up-a-raspberry-pi-airplay-receiver/)

> sudo apt-get update

> sudo apt-get upgrade

> sudo apt-get install autoconf automake avahi-daemon build-essential git libasound2-dev libavahi-client-dev libconfig-dev libdaemon-dev libpopt-dev libssl-dev libtool xmltoman

> sudo git clone https://github.com/mikebrady/shairport-sync.git

> cd shairport-sync

> sudo autoreconf -i -f

> sudo ./configure --with-alsa --with-avahi --with-ssl=openssl --with-systemd --with-metadata

> sudo make

> sudo make install

> sudo systemctl enable shairport-sync


Manuell starten

> sudo service shairport-sync start
