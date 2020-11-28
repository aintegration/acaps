## Description
Node-Red (see https://nodered.org) is a Node.JS application and can be installed on a variety of different computers, 
servers and virtual machines.  The Node-Red ACAP packages Node.JS and NPM with Node-Red Modules to be installed in an 
Axis camera.  The primary use case is to simplify adding integration, logic and notification services to the camera.
It is a visual scripting (low-coding) alternative compared to ACAP development that requires embedded C development skills.

Note that Axis cameras are not generic computers so there may be limitations on what you can do with Node-Red in the camera.

## Prerequisites
1. An Axis Camera based on ARMv7hf (ARTPEC-6 & ARTPEC-7)
2. A mounted SD Card in the camera.  Node.JS, NPM and modules are big and camera flash memory is limited.  The SD card is used to store nodes and flows. 

## Limitations
- Different cameras may have different amount of availabel resources.  This means the Node-Red may not work on some models.
- Node-Red will consume substantial FLASH and RAM memory.  It may not be possible to combine with other ACAP that also consumes a lot of FLASH and RAM.
- Some 3:rd party nodes may require components (e.g. Python) that is not avaialbel in the cameras.

## Download
[Change log](https://github.com/aintegration/acaps/blob/master/Node-Red/files/changelog.md)

- [ARMv7hf](https://github.com/aintegration/acaps/raw/master/Node-Red/files/Node-Red_1_0_0_armv7hf.eap)
- MIPS (Not avaialble)
- AARCH64 (Not avaialble)

## Installation
After installation and starting the ACAP it may take a couple of minutes for Node-Red to be initializied.
If you are not able to access Node-Red with 3-4 minutes, check the system log as the installation may have failed. 


## Security
As Node.JS will have access to the underlying camera platform it is recommeded secure the inerfaces. 
By default, Node-Red does not require any authentication.  You need to add user and password for both the flows view and the dashboard view (if used).
In order to simplify this configuration you can use the example flow "Securing Node-Red".


## Example flows
- [Securing Node-Red](examples/Securing%20Node-Red) provides a dashboard interface that simplifies editin Node-Red settings file and also generate pashword hashes.
- [Local MQTT Broker](examples/Securing%20Node-Red) shows how to run a local MQTT broker in the camera.
