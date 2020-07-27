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
