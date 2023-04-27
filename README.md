<img src="https://github.com/avenger11/Apple-HomePlay/blob/master/Repo-images/HomePlay%20Banner.png" width=60% height=60%>
My take on Apple Home Dashboard Design for Home Assistant. (Work in Progress)

I'm running Home Assistant OS Supervised VM hosted on a NAS DS920+.
The Wall Mount tablet is a FireHD 10 from amazon running Fully Kiosk Browser.



## Architecture

This is the keyplan for the layout.

The code for the custom:grid-layout can be edited within homeplay.yaml

<img src="https://user-images.githubusercontent.com/37946892/234449029-eb518f05-ca48-468b-9ef2-6d73abda07d9.png" width=40% height=40%>

![image](https://user-images.githubusercontent.com/37946892/234452580-5278f1b3-c71f-4653-8507-8d89ed29911f.png)

## TOPBAR | Quick Glance at your house state

![image](https://user-images.githubusercontent.com/37946892/234453082-ec540557-25c0-4b81-8a8f-f41089791a24.png)
![image](https://user-images.githubusercontent.com/37946892/234453091-24e6d17b-5850-47d8-91a8-15fbf390157f.png)
![image](https://user-images.githubusercontent.com/37946892/234453106-393cc3c1-20c3-412e-904e-bd4e2973acd7.png)

- Dynamic Dual Tone Icon
- Climat chips will change color based on heating or cooling
- SVG Icons can be found under button_card_template/icon-svg-dualtone.yaml
- Heavy use of template that are found in button_card_template directory
- Popup for battery level (more to come)

![image](https://user-images.githubusercontent.com/37946892/234737716-e039c402-9a8c-4b80-95f1-01bf7a79f02e.png)

These custom button are integrated in a custom:hui-element – horizontal stack center to the screen.

![image](https://user-images.githubusercontent.com/37946892/234737747-07818cf9-6d7f-4e0b-868a-2e229689eeb5.png)

## LEFT COLUMN | Weather Card

![image](https://user-images.githubusercontent.com/37946892/234737981-17ce3c72-89f2-4ca9-b6c5-e850b9f8f10f.png)

Weather background change based on condition and day/night (screenshot from weather app).
The background can be found in www/weather folder.
I’m using the weather code from the Montréal Environnement Canada Integration and a Value template in configuration.yaml to differentiate between day and night.

![image](https://user-images.githubusercontent.com/37946892/234737871-760f7af8-5c04-431c-b1f9-39ecef1b4a64.png)
![image](https://user-images.githubusercontent.com/37946892/234737875-6635c314-f8dc-4039-b1d2-f32e74d33831.png)

One example: The high and low temperature in the card use a value template as well to format properly

![image](https://user-images.githubusercontent.com/37946892/234737956-17515b79-dc90-40e7-80e6-8176586b4da1.png)


## LEFT COLUMN | Calendar Card

- Calendar Card from Atomic Calendar.
- Heavily modified with Card Mod.

![image](https://user-images.githubusercontent.com/37946892/234738068-32f7286f-703f-482f-bf3a-a0db17d7f365.png)


## CENTER COLUMN | Home view map

- Multiple floor by swaping or using the level button
- Image change based on day and night

![image](https://user-images.githubusercontent.com/37946892/234738924-f882810a-8815-49fa-81af-027dd9f8f43a.png)
![image](https://user-images.githubusercontent.com/37946892/234738933-a550a9d3-363b-4ca0-bcc4-7f905b726a5b.png)


## RIGHT SIDE | highlight card 


![image](https://user-images.githubusercontent.com/37946892/234738123-c75fea94-f189-471d-bfbd-1b83dba82e6d.png)
![image](https://user-images.githubusercontent.com/37946892/234738133-73cd420a-1eea-4935-8576-96744aae5348.png)

## TASK BAR | 

![image](https://user-images.githubusercontent.com/37946892/234738185-5866cfe7-f777-47d0-a140-66f442b4f126.png)
![image](https://user-images.githubusercontent.com/37946892/234738193-1ec31a2c-2f42-4527-a433-ca20ed0d7d8a.png)


## Feature

- Day & Night theme support (NB: automation based on sun location)
- Support multiple floor by swaping between card
- Calendar integration
- "apps" support notification


The floor plan have been designed in [Sweet Home 3D](https://www.sweethome3d.com/) and edited.



## Custom Cards from HACS
Ensure to install those custom card before using this configuration via HACS

- [Lovelace-Layout-Card](https://github.com/thomasloven/lovelace-layout-card) by Thomas loven.
- [Swipe-card](https://github.com/bramkragten/swipe-card) by Bram Kragten.
- [Button-card](https://github.com/custom-cards/button-card) by RomRider.
- [Lovelace-Card-mod](https://github.com/thomasloven/lovelace-card-mod) by Thomas loven
- [Atomic Calendar Revive](https://github.com/totaldebug/atomic-calendar-revive) by marksie1988
- [Kiosk Mode](https://github.com/NemesisRE/kiosk-mode) by NemesisRE
- [Clock weather card](https://github.com/pkissling/clock-weather-card) by pkissling

## Custom integration from HACS
- [Fontawesome](https://github.com/thomasloven/hass-fontawesome) by Thomas loven.
- [Browser_mod](https://github.com/thomasloven/hass-browser_mod) by Thomas loven.

## TODO List
- [ ] FIll the empty space on the left, potentially light on count, climat etc..
- [ ] Remove transition weather background and code
- [ ] Improve all popups
- [ ] Integrate Washer & Dryer Card
- [ ] Solve all resizing issues

## Credit

- inspired by the great work of [Mattias Persson](https://github.com/matt8707/hass-config) & [lukevink](https://github.com/lukevink/hass-config-lajv) 


If you'd like to support me and future projects:

:star2: Star my repo, if you like what you see :)

<a href="https://www.buymeacoffee.com/sebhome" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>


## Resource

Apple Icon
https://www.figma.com/file/PwWaGiMaSyrktcQRh7MxAD/SF-Symbols-4.0---SVG-Icons-(Community)?node-id=1498-49395&t=8xsPmha2AmVoMsAg-0
