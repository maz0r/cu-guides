# Capsunlocked Guide to QMK, VIA and Vial firmware

- All CU keyboards run QMK

- VIA enabled firmware is available for the CU7,CU65 and CU80

- VIAL specific firmware is available for the CU7

## What is [QMK](https://qmk.fm/)

QMK or Quantum Mechanical Keyboard Firmware is a an open source keyboard firmware offering customisation across a wide range of compatible keyboards.

The QMK firmware loaded on your keyboard on arrival is running the default keymaps, if you wish to customise these on a QMK firmware, you can do so using the [QMK Configurator](https://config.qmk.fm/).

##### Basic customisation offered by the QMK Configurator

- Layers
- Layer Toggle (Momentary & Switch)

 - Mapping Keys
 - Compiling and Saving the Firmware



##### Advanced customisation with QMK Configurator

QMK is VERY configurable offering macros, tap codes and toggles, so rather than try to cover everything here I've compiled a short list of links which should help with most things.

- A full list of [QMK keycodes can be found here](https://docs.qmk.fm/#/keycodes).

  - [Language specific](https://docs.qmk.fm/#/reference_keymap_extras)

- Full expanded explanation of [Layers](https://docs.qmk.fm/#/feature_layers) and how to use/structure them within your custom endeavours.

- [Mod-Tap](https://docs.qmk.fm/#/mod_tap) - acts like a modifier when held, and a regular keycode when tapped. In other words, you can have a key that sends Escape when you tap it, but functions as a Control or Shift key when you hold it down.

  

##### Macros and the QMK Configurator

At present it's not possible to create/edit macros this way, if this is a feature you require you should check out VIA/VIAL below, or delve into the world of compiling your own [QMK custom firmware](https://docs.qmk.fm/#/newbs_getting_started).





## What is [VIA](https://caniusevia.com/)

VIA is a semi-open GUI application for Linux, Mac and Windows

## What is [Vial](https://get.vial.today/)

VIAL is a fully open source alternative to VIA, while it can be used on VIA enabled firmware's, this requires manual sideloading and is not recommended for most users.

VIAL is fully supported on the CU7, with plans to support other boards.

















### QMK Configurator

https://config.qmk.fm/

###### Select your Caps-Unlocked board!

- Select your board from the Top dropdown
- Select your default layout from the second dropdown 
- Give your custom map a name!

![qmk_config](Images\qmk_config.gif)



###### Switching/ Creating Layers

- Simply click the layer number to edit the layer
  - If you add a key to a blank layer it will add become darker indicating it has keys present.

![qmk_layer_switch](Images\qmk_layer_switch.gif)



###### Drag, Press or Type Keys

![qmk_drag_keys](Images\qmk_drag_keys.gif)











### Flashing

Flashing is the process of updating your keyboard, it can be used to return to a previous working condition or enable new features & customisations.

It's recommended to use [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases) for this, as it's the easiest method for most people who aren't used to microcontrollers.

You may need drivers to enable flashing more about that [here](https://docs.qmk.fm/#/driver_installation_zadig)





#### Got your hex ready?

Launch QMK Toolbox

1. If you downloaded your Hex then choose the file file using the open button.

![qmk_open](Images\qmk_open.gif)



2. If you just want a default firmware from the QMK configurator you can use the dropdown to select it then hit load to download and prep the file.

![qmk_load](Images\qmk_load.gif)







#### Lets do this!

Confirm your board is in bootloader mode

##### First time flasher?

Get that back panel off and press the reset while connected to your PC/Mac to enter bootloader mode!

##### Already flashed a custom hex?

Check your default keymap (or custom keymap) for your [Reset] Key which will put your board in bootloader mode!

##### Prefer Bootmagic/Command

Hold your boards magic key while connecting the USB to enter bootloader mode!

​	CU80 - ESC
​	CU65 - ?
​	CU7 - ?



#### Flash!

![qmk_flash](Images\qmk_flash.gif)



#### Test your changes!

Load up QMK Configurator, VIA or VIAL and test your input!

