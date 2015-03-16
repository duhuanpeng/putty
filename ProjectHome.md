
# PuTTY with modifications #
## Changes ##

### change serial default settings ###
Options controlling local serial lines
  * Serial line to connect to: COM3
  * Speed(baud): 115200
  * Flow control: None

### add a feature to disable `AltGr` key, (enable right `Alt` key) ###
Options controlling the terminal emulation
Terminal -> Keyboard -> Enable extra keyboard features
  * [ ] Enable `AltGr` key

## Building ##
```
git clone https://code.google.com/p/putty/
cd putty\WINDOWS
NMAKE -f MAKEFILE.VC
```