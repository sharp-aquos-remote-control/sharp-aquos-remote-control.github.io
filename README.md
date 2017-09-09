# Sharp aquos remote control

Control your Sharp Aquos television, remotely, via TCP/IP

## Quick start

### Enable the remote control

The first thing to do is to connect your television to your
LAN. Then:

1. MENU -> Initial Setup -> AQUOS Remote Control
2. Enable
3. Set the login and password

OR

1. MENU -> Settings -> Network settings -> Ip Control Settings
2. Enable 
3. Set the login and password

### Test

Make sure the television is turned on and connected to the local network.

Run the following command:

    $ telnet IP_ADDRESS_OF_THE_TV REMOTE_CONTROL_PORT

where `REMOTE_CONTROL_PORT` is by default `10002`, unless you've changed it 
before. You should get:

    Trying IP_ADDRESS_OF_THE_TV...
    Connected to IP_ADDRESS_OF_THE_TV.
    Escape character is '^]'.

Now type in `POWR0   ` (That is `POWR0` followed by 3 spaces and the return key)
The TV should turn off and you should read

    OKR

in your terminal window.

## Installing the Python API

...

## Resources

- pages 8-3 (101) through 8-8 (106) in the
  [sharp user manual](http://files.sharpusa.com/Downloads/ForHome/HomeEntertainment/LCDTVs/Manuals/2014_TV_OM.pdf)
- pages 58 through 59 in another
  [sharp user manual](http://www.sharp.co.uk/cps/rde/xbcr/documents/documents/om/11_lcd-tv/LC40-46LE830E-RU-LE831E-RU_OM_GB.pdf)

## Table of supported models

...
