## 2.3-1
- MQTT Port moved fron address input to its own input box
- Event Topic input move from TARGET to EVENT
- Moved descriptions to ABOUT
- Updated VMS event proxy
	- Subscription topic can now be changed for event and state
	- State is no longer controlled in topic, it is control in payload
- Ability to set transparancey in text overlay
- Added ability to set transparancy level for background in text overlay

## 2.2-6
- Update the GUI pages and navigation.
  - Added menu on left side
  - More helpful instructions 
- New features/options
  - Ability to set video text overlay with MQTT messages (display e.g. sensor data).  Only available for  armv7hf.
  - Change recurring device status on MQTT
  - MQTT to VMS event proxy.  Ability to reach a VMS action rules with MQTT messaging
  - New target server "Axis Device".  Ability to send HTTP POST to a sibling Axis Device

## 2.1-2
- Fixed bug that could prevent publishing VMD if profile name did not have default value
- Added property localTime in payload
- Added ability to adjust status update using an API call.
  - Changing the time period requires restart of Publisher.
  - Setting retained will append the serial number to the topic
  - http://<ip>/local/publisher/settings?set=status&json={"seconds":300,"retained":true,"topic":"my/own/topic"}
- Added timestamp and localTime in status update

## 2.1-1
- Topic is now shown correctly in GUI
- Cleaned up GUI
- Removed the selection of JSON struction in GUI
- Cleaned up payload of MQTT message axis/status

## 2.0-4
- Fixed a UI bug that made event state send MQTT messages on both high and low states when selecting "Only when high" after changing to "High & Low"
 
## 2.0-3
- Fixed certificate page
- Removed subscription QOS 2 that prevented connection to AWS broker

## 2.0-2
- Support for TLS w/o client certificates
- User interface restructure
- Added supports for MQTT Subscriptions that generates ONVIF events.  Typically used to trigger Camera/VMS actions.
- Auto publishing device status on MQTT every 15 minutes on topic "axis/status"

## 1.2-1
- Fixed a bug introduced in 1.2-0 that prevented images to be included in selected events

## 1.2-0
- Replaced generic device ents with slelected common device events such as IO, virtual input and PTZ
  This also fixed the occasional crash/respawn when selecting Device Events

## 1.1-0
- Added support for generic ACAP events
- Added support for generic device event (I/O, Temperture, etc..)
- Enhanced UI
- Changed sata structure tags:name to tags:client

## 1.0-0
First commit
