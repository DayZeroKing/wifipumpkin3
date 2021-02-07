# Settingup WifiPumpkin3 on Raspberry Pi Zero

### Tested on Raspberry Pi OS (2021-01-11-raspios-buster-armhf-lite)

#### First install Requirements for WifiPumpkin3

    $ sudo apt-get update
    $ sudo apt-get upgrade
    $ sudo apt install iptables iw net-tools wireless-tools hostapd git python3.7-dev libssl-dev libffi-dev build-essential python3.7 python3-pip -y

### PyQt5 - 5.14.2

    $ sudo apt-get update
    $ sudo apt-get install qt5-default
    $ sudo apt-get install sip-dev
    
    $ cd /usr/src
    $ sudo wget https://files.pythonhosted.org/packages/c6/7f/b0830b133e6fac3902ecea99acc99e41972d9b565cda5d68ae33ae37909c/sip-5.0.0.tar.gz
    $ sudo tar xzf sip-5.0.0.tar.gz
    $ cd sip-5.0.0
    $ sudo python3 configure.py --sip-module PyQt5.sip
    $ sudo make
    $ sudo make install
    
    $ cd /usr/src
    $ sudo wget https://files.pythonhosted.org/packages/4d/81/b9a66a28fb9a7bbeb60e266f06ebc4703e7e42b99e3609bf1b58ddd232b9/PyQt5-5.14.2.tar.gz
    $ sudo tar xzf PyQt5-5.14.2.tar.gz
    $ cd PyQt5-5.14.2
    $ sudo python3 configure.py
    $ sudo make
    $ sudo make install

Check if the pyqt5 is installed successful

    python3 -c "from PyQt5.QtCore import QSettings; print('done')"

### Cryptography 3.2.1

    $ sudo pip3 uninstall cryptography
    $ sudo pip3 install cryptography==3.2.1

### Install Wifipumpkin3

    $ git clone https://github.com/P0cL4bs/wifipumpkin3.git
    $ cd wifipumpkin3

if you see this message bellow, everything ok !

    Finished processing dependencies for wifipumpkin3==1.0.0

now, let’s execute the app:

    $ sudo  wifipumpkin3
        

  




