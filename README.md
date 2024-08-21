### forked from goodtft/LCD-show/
### these are my changes for the MHS35 to make it work correctly for the Pi 5 on Raspberry Pi OS Bookworm
## use at your own risk, check upstream first.


```sudo rm -rf LCD-show```<br>
```git clone https://github.com/mariusquabeck/LCD-show.git```<br>
```chmod -R 755 LCD-show```<br>
```cd LCD-show/```<br>
  
# MHS-3.5” RPi Display(MHS3528):
### Driver install:
sudo ./MHS35-show-pi5
### WIKI:
CN: http://www.lcdwiki.com/zh/MHS-3.5inch_RPi_Display  <br>
EN:http://www.lcdwiki.com/MHS-3.5inch_RPi_Display

# How to rotate the display direction

This method only applies to the Raspberry Pi series of display screens, other display screens do not apply.

### Method 1, If the driver is not installed, execute the following command (Raspberry Pi needs to connected to the Internet):

sudo rm -rf LCD-show<br>
git clone https://github.com/goodtft/LCD-show.git<br>
chmod -R 755 LCD-show<br>
cd LCD-show/<br>
sudo ./XXX-show 90<br>

After execution, the driver will be installed. The system will automatically restart, and the display screen will rotate 90 degrees to display and touch normally.<br>
( ' XXX-show ' can be changed to the corresponding driver, and ' 90 ' can be changed to 0, 90, 180 and 270, respectively representing rotation angles of 0 degrees, 90 degrees, 180 degrees, 270 degrees)<br>

### Method 2, If the driver is already installed, execute the following command:

cd LCD-show/<br>
sudo ./rotate.sh 90<br>

After execution, the system will automatically restart, and the display screen will rotate 90 degrees to display and touch normally.<br>
( ' 90 ' can be changed to 0, 90, 180 and 270, respectively representing rotation angles of 0 degrees, 90 degrees, 180 degrees, 270 degrees)<br>
(If the rotate.sh prompt cannot be found, use Method 1 to install the latest drivers)



