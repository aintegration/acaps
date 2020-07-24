![target](pictures/publisher2.png)

### Prerequisites
1. Axis Camera
2. An Influx server, HTTP server or MQTT Broker

### Supported platforms
- [MIPS](https://github.com/aintegration/acaps/raw/master/Publisher/files/Axis_Publisher_mips.eap)
- [ARMv7hf](https://github.com/aintegration/acaps/raw/master/Publisher/files/Axis_Publisher_armv7hf.eap)
- [AARCH64](https://github.com/aintegration/acaps/raw/master/Publisher/files/Axis_Publisher_aarch64.eap)


# Configuration

## Server
### Type
The server type that will recive data.

### Address:port
Examples
```
  mqtt.server.com:1883
  http://12.23.34.45/some/end/point
  influx.server.com:8086
```
### MQTT
#### Client ID
Set a name for the device used primaruly for MQTT.  This will also be added in the data payload.
#### Topic
If leaving blank the topic will be axis/event/...
#### User/Password
Leave blank if broker does not require authentication.

### HTTP
#### User/Password
Leave blank if broker does not require authentication.

### Influx
#### Database
Set the database name
#### Collection
Set the collection where data will be stored
#### User/Password

### TLS
Encrypts traffic and verify server authenticity.  If needed, add client certificate by clicking "Set TLS certificates"


## Data
### Event
Select that event that will trigger and set payload.
### State
Some events are statful (high/low).  Us this to only recive data when the event goes high or recive messages when if goes either high or low.
### Additional tags
Add additional tags that wil be included as properties in payload.
Examples
```
location=New-York
country=France,city=Paris,store=some-id
```
### Image Capture
If setting image, a JPEG image will be included (base64 encoded)

### Test connection
This will publish test data to the target and display a success/failure message.  On failure, check the log for hints.
