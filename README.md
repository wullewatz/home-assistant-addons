# Wullewatz Home Assistant add-on repository

Add-on documentation: <https://developers.home-assistant.io/docs/add-ons>

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fhome-assistant%2Faddons-example)

## Add-ons

This repository contains the following add-ons

### [HassPiAudio](https://github.com/wullewatz/home-assistant-addons/tree/main/haspiaudio)

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
![Supports armhf Architecture][armhf-shield]
![Supports armv7 Architecture][armv7-shield]
![Supports i386 Architecture][i386-shield]

Raspberry DLNA Server, that shares local Home Assistent Media and a DLNA Renderer on local 3.5mm Headfone out. Also Snapcast Server & Client for MultiRoomAudio!

Based on: badaix/snapcast and hzeller/gmrender-resurrect

DLNA Server -> DLNA Render -> Snapcast Server -> Snapcast -> Audio Out

It's working, and no latency on 64bit clients (Snapcast Android App)! 👍
<!--

Notes to developers after forking or using the github template feature:
- While developing comment out the 'image' key from 'example/config.yaml' to make the supervisor build the addon
  - Remember to put this back when pushing up your changes.
- When you merge to the 'main' branch of your repository a new build will be triggered.
  - Make sure you adjust the 'version' key in 'example/config.yaml' when you do that.
  - Make sure you update 'example/CHANGELOG.md' when you do that.
  - The first time this runs you might need to adjust the image configuration on github container registry to make it public
- Adjust the 'image' key in 'example/config.yaml' so it points to your username instead of 'home-assistant'.
  - This is where the build images will be published to.
- Rename the example directory.
  - The 'slug' key in 'example/config.yaml' should match the directory name.
- Adjust all keys/url's that points to 'home-assistant' to now point to your user/fork.
- Share your repository on the forums https://community.home-assistant.io/c/projects/9
- Do awesome stuff!
 -->

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg


I coul'd need some help in the structure of the addon, so thos maybe can be an Community Addon!!!


Installation:

- Copy folder into addons
- Install it from HA addons
- No Setup needed (Exept IP-Ports if needed)
- Upnp Server shares HA Media folder
- UPNP Renderer will be detect by HA DLNA
- Add Snapcast integration from HA

Screenshots:
![Screenshot_20230813-140213_Chrome](https://github.com/wullewatz/home-assistant-addons/assets/64665830/e3a094bb-a41c-4857-b612-f0128a446bdc)
![Screenshot_20230813-140307_Chrome](https://github.com/wullewatz/home-assistant-addons/assets/64665830/4ffb4c8c-9e08-454e-b6ae-67ffde9834f3)
![Screenshot_20230813-140448_Chrome](https://github.com/wullewatz/home-assistant-addons/assets/64665830/502d3dbc-47a4-4430-9b5f-8a2d82434fea)
(Sample made with HACS Mini-Media-Player)


