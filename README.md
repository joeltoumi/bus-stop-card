# CRTM-Mobility-Card

| View                                                                               | 
|------------------------------------------------------------------------------------| 
| ![image](https://github.com/joeltoumi/crtm-mobility-card/blob/master/card.png?raw=true) | 

<br/>

**Requires a custom-component:**<br/>
This card only work with [CRTM custom integration](https://github.com/joeltoumi/sensor_crtm) to feed it.


### Issues
Read through these two resources before posting issues to GitHub.
* [@thomasloven's lovelace guide](https://github.com/thomasloven/hass-config/wiki/Lovelace-Plugins).


## Features
* Displays Madrid public transport stop information including route and next arrival times.
* Optional customization of the stop name via YAML configuration.
* Automatically updates arrival times and shows the last request time.
* Responsive design to fit various screen sizes.
* Up to three next arrival times shown for each route.
* Flexible formatting with customizable columns for route names and times.

## Installation:

* Install the custom component by following it's instructions.
* Install this card by copying `crtm-mobility-card.js` to your `www/community/` folder. If you're copy/pasting the code always copy from raw files on github (button on top right when viewing code).
* Include it in its own folder like so: `www/community/crtm-mobility-card/crtm-mobility-card.js`

This goes into ui-lovelace.yaml under "resources:"

```
resources:
- url: /local/community/crtm-mobility-card/crtm-mobility-card.js?v=0.0.1
  type: js
```

## Usage:
Create a card and add the yaml code manually:
```yaml
type: custom:crtm-mobility-card
entity: sensor.crtm_stop_xxxxx
stop_name: Custom name
```

# Main Config:
| Parameters  | Type     | Description                                                                                                               |
|:------------| :------- |:--------------------------------------------------------------------------------------------------------------------------|
| `type`      | `string` | **Required**. Type of the card                                                                                            |
| `entity`    | `string` | **Required**. Entity from the CRTM integration                                                                            |
| `stop_name` | `string` | **Optional**. Custom stop name. <br/>If not provided, the stop number will be displayed in the name.                      |

