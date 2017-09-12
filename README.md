Control your Sharp Aquos television, remotely, via TCP/IP

Note: This project is not affiliated with Sharp Inc.

## List of contents

- [Reasons](index.html#reasons)
  - [Assets](index.html#assets)
  - [Liabilities](index.html#liabilities)
- [Quick start](index.html#quick-start)
  - [Enable the remote control](index.html#enable-the-remote-control)
  - [Probing](index.html#probing)
- [Available APIs](index.html#available-apis)
- [Resources](index.html#resources)
- [Table of models and firmwares](index.html#table-of-models-and-firmwares)
  - [How to check model name and firmware version](index.html#how-to-check-model-name-and-firmware-version)
- [Contributors](index.html#contributors)
- [License of this document](index.html#license-of-this-document)

## Reasons

You may want to use this feature for:

- home automation
- external action triggering
- as an alternative to the phisical IR remote
  through a vocal, textual, touch and other types of interfaces
- etc...

### Assets

- Protocol is simple

### Liabilities

- Connection to and from the tv is not encrypted.
- It is unclear which models are supported and what commands each of them 
  supports.

## Quick start

To enable the remote control you must follow the next steps in sequential 
order.

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

### Probing

Make sure the television is turned on and connected to the local network.

Run the following command:

```shell
$ telnet IP_ADDRESS_OF_THE_TV REMOTE_CONTROL_PORT
```

where `REMOTE_CONTROL_PORT` is by default `10002`, unless you've changed it 
before. You should get:

    Trying IP_ADDRESS_OF_THE_TV...
    Connected to IP_ADDRESS_OF_THE_TV.
    Escape character is '^]'.

Now type in `POWR0   ` (That is `POWR0` followed by 3 spaces and the return 
key). The TV should turn off and you should read

    OKR

in your terminal.

## Available APIs

There are a series of APIs, each one of them in a different stage of 
development 

| Programming language | Library |
|----------------------|---------|
| C | [aquosctl](https://github.com/jdwhite/aquosctl) |
| Go | [go-sharptv](https://github.com/golliher/go-sharptv),  [aquostv](https://github.com/tknhs/aquostv) |
| Groovy | [device-sharp-aquos](https://github.com/KristopherKubicki/device-sharp-aquos) |
| Java | [Aquarium](https://github.com/kfriede/Aquarium) |
| Javascript | [sharp-aquos-remote-control](https://github.com/benburkhart1/sharp-aquos-remote-control) |
| Python | [sharp_aquos_rc](https://github.com/sharp-aquos-remote-control/sharp_aquos_rc),  [aquos-module-Python](https://github.com/thehappydinoa/aquos-module-Python) |
| Ruby | [sharp_aquos_control](https://github.com/zxjinn/sharp_aquos_control) |

## Resources

| Link | Page(s) |
|------|---------|
| [sharp user manual 1](http://files.sharpusa.com/Downloads/ForHome/HomeEntertainment/LCDTVs/Manuals/2014_TV_OM.pdf) | 8-3 (101) through 8-8 (106) |
| [sharp user manual 2](http://www.sharp.co.uk/cps/rde/xbcr/documents/documents/om/11_lcd-tv/LC40-46LE830E-RU-LE831E-RU_OM_GB.pdf) | pages 58 through 59 |

## Table of models and firmwares

| Model       | Firmware version | Supported | List of available commands |
|-------------|------------------|-----------|----------------------------|
| LC-40LE830E | 208E1204111      |    yes    |                            |

### How to check model name and firmware version

## Contributors

## License of this document

CC0
