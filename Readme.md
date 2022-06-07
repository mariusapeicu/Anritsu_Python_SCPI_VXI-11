# Anritsu SCPI VXI-11 Python SCPI Commands example  

## 1.Overview
The present scripts are Python3 based methods to command Anritsu devices.
It exemplifies how to do perform the 4 actions in software communication :
* Connect
* Write
* Query
* Disconnect (Close connection)

Programming language and dependency: Python3 ("PyVISA" Python package) \
Software version Tested: Python 3.10.2, PyVISA 1.11.3 \


Script Revision: 1.0 \
Original Release Date: 6/7/2022 \
Current Revision Date: 6/7/2022

## 2.Required Software
Some software components need to be installed before using these scripts. The current versions of these components are listed below, and can be downloaded from their respective website.

[Python3](https://www.python.org/downloads/) \
[PyVISA](https://pyvisa.readthedocs.io/en/latest/introduction/getting.html)

Refer to the relevant Software Developers resources for more information about software requirements.

## 3.Installation
Refer to the above-mentioned relevant Software Developer resources for more information on required Software installation. \

## 4.Running

>  **Keep in mind that the ShockLine software has to be running during the execution of this script.**

The example covers the method of sending SCPI commands via a VXI-11 connection.

### 4.0. Instrument connection

The instrument connection is instantiated as an object using the resource name of the device.

    * TCPIP0::127.0.0.1::inst0::INSTR

> **Important Note:**
>> The script examples use the localhost address 127.0.0.1 for a device connected directly to the computer running the script; __don't forget to change the instrument address on the line calling the *main()* function__ for devices connected to another computer in the network. The relevant script line is mentioned in the 2nd comment at the begining of each script-file example, right after the import statemens.

If the connection fails for any reason, the error message is displayed in the terminal, and the script stops running completely.

### 4.1. Read Instrument type - *IDN? Query
Simple example of a query command; \
Returns information about the device manufacturer, model, serial, and firmware revision number.

### 4.2. System preset - *RST
Simple example of a write command; \
The instrument is returned to its factory as-shipped configuration.

### 4.3. Instrument connection closing
The connection object will end the relevant connection method depending on the type it instantiated at step 0.

## 5.Revision History
The latest version of these Python scripts, and examples for other programming languages, can be downloaded at [this location (to be determined)]. \
REV 1.0, 6/7/2022 \
Modified by: Voicu Bogdan, Bucharest, Romania \
Original Release. 