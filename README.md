# hd44780
Extensible hd44780 LCD library

Licensing
=========
![GPLv3Logo](https://www.gnu.org/graphics/gplv3-127x51.png)

hd44780 is an open source project for open source projects. Those wishing to create closed projects should seek an alternate solution. hd44780 is licensed under the terms of the GNU General Public License v3.0 as opposed to the more liberal licensing terms of the GNU Lesser General Public License (LGPL), MIT, modified BSD, Apache, etc..

For full details on the licensing of the hd44780 library and its components, see the included licensing file.

Library Overview
=================
hd44780 is an extensible Arduino LCD library for hd44780 based LCD displays.
The library consists of a hd44780 base class combined with one or more
i/o subclasses to perform the i/o communication between the host and the
hd44780 display interface.

The hd44780 library is not a direct drop in replacement for the the Arduino IDE LiquidCrystal library.

The API functionality provided by the hd44780 base class, when combined
with an hd44780 library i/o subclass, is compatible with the API
functionality of the Arduino LiquidCrystal library as well as compatibilty
with most of the LCD API 1.0 Specification (some of which is nearly obsolete).

The hd44780 API also provides some addtional extensions and all the API
functions provided by hd44780 are common across all i/o subclasses.
One of the most significant extensions being the ability to modify the libraries expected command execution times.

S/W requirements
================
- ### IDE versions 1.0 and later

- ### IDE versions that should be avoided:
	- IDE versions 1.5 to 1.55 (unnecessary file name restrictions, breaks many libraries)
	- IDE version 1.6.6 (has function prototyping issues that can break some sketches)
	- IDE version 1.6.8 (has serial port issues that breaks on certain boards)


H/W support
===========
Library should work on all Arduino boards.

The library currenly comes with the following i/o subclasses:

* hd44780_pinIO control LCD using direct Arduino Pin connections

* hd44780_I2Cexp control LCD using i2c i/o exapander backpack (PCF8574 or MCP23008)

* hd44780_I2Clcd control LCD with native i2c interface


Installation
============
For ease of installation it is recommended to use an IDE that supports the library mananager which was implemented in IDE version 1.6.2

### Installation using Library manager (IDE 1.6.2 and later)
In the IDE, Simply click on [Sketch]->Include Library->Manage Libraries...
Then search for "Extensible hd44780" to locate the library and install it.

### Installation using zip file (IDE 1.6.1 and earlier)
Installation requires downloading a zip image and
then, depending on the version of the IDE you can either install it from the IDEor install it manually by unziping the file into your sketchbook libraries.

1) dowload a library zip image from the github repository:
https://github.com/duinoWitchery/hd44780
Download the image by clicking the green box that says [Clone or Download].

2) Rename the downloaded and saved the zip image to hd44780.zip

#### Installation of zip file library on IDE 1.0.6 to 1.6.1
The library can be installed from the zip image using the IDE.
Install it by clicking on:
[Sketch]->Include Library->Add .ZIP library...
then, simply select the hd44780.zip image you downloaded and renamed.

#### Installation of zip file library on IDE 1.0 to 1.0.5
On these versions of the IDE the install must be done manually.
To install the library simply extract it into your sketchbook/libraries directory.
If you don't know where you sketchbook/libraries directory is simply click on:
[File]-Prefernces
or from the keyboard type: &lt;ctrl&gt;comma (hold ctrl and press comma)
The loation of your sketchbook directory will be in the text box.
The zip image must be installed in a directory called "libraries" under that directory.
