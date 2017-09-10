Control your Sharp Aquos television, remotely, via TCP/IP

Note: This project is not affiliated with Sharp Inc.

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

Now type in `POWR0   ` (That is `POWR0` followed by 3 spaces and the return 
key). The TV should turn off and you should read

    OKR

in your terminal window.

## Available APIs

| Programming language | Library |
|----------------------|---------|
| C | https://github.com/jdwhite/aquosctl |
| Go | https://github.com/golliher/go-sharptv |
| Go | https://github.com/tknhs/aquostv |
| Groovy | https://github.com/KristopherKubicki/device-sharp-aquos |
| Java | https://github.com/kfriede/Aquarium |
| Javascript | https://github.com/benburkhart1/sharp-aquos-remote-control |
| Python | https://github.com/sharp-aquos-remote-control/sharp_aquos_rc |
| Python | https://github.com/thehappydinoa/aquos-module-Python |
| Ruby | https://github.com/zxjinn/sharp_aquos_control |

## Resources

- pages 8-3 (101) through 8-8 (106) in the
  [sharp user manual](http://files.sharpusa.com/Downloads/ForHome/HomeEntertainment/LCDTVs/Manuals/2014_TV_OM.pdf)
- pages 58 through 59 in another
  [sharp user manual](http://www.sharp.co.uk/cps/rde/xbcr/documents/documents/om/11_lcd-tv/LC40-46LE830E-RU-LE831E-RU_OM_GB.pdf)

## Table of models and firmwares

| Model       | Firmware version | Supported | List of available commands |
|-------------|------------------|-----------|----------------------------|
| LC-40LE830E | 208E1204111      |    yes    |                            |

### How to check model name and firmware version

