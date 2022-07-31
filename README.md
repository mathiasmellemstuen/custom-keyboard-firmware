# Custom keyboard firmware
![Image of the keyboard](https://github.com/mathiasmellemstuen/keyboard_qmk_firmware/blob/main/soflekeyboard-image.jpg)
This repository contains firmware for my custom splitted keyboard with nordic design. The keyboard I'm using is a <a href="https://github.com/josefadamcik/SofleKeyboard" target="_blank">Sofle by Josef Adamchik</a>. This firmware is based on the <a href="https://qmk.fm/" target="_blank">QMK</a> firmware.

## Keyboard layout
This layout consists of multiple layers. The layout have different layer keys that changes the layout to another layer when it's pressed. The layer keys are marked as `LAYER` on the layer keys in the illustration below.

![Layout of the keyboard](https://github.com/mathiasmellemstuen/keyboard_qmk_firmware/blob/main/soflekeyboard-custom-nordic-design.png)

### Layer 1
Layer 1 is almost a standard nordic keyboard layout with a few exceptions. Layer 2 will activate if holding the yellow button on this layer.

### Layer 2
Layer 2 has arrow keys at the WASD keys. Layer 3 will activate if the SHIFT key is pressed in this layer. Layer 4 will activate if the F key is pressed in this layer. Layer 5 will activate if the G key is pressed in this layer. This layer does also contain a macro record and macro play key. The layer has backslash at the 7 key. 

### Layer 3
Layer 3 contains the pipe key at the 7 key.

### Layer 4
This layer contains all the function keys.

### Layer 5
This layer is a layer dedicated to setting the keyboard in gaming mode. It's only changing one key at the moment, adding an extra spacebar instead of the left return key. This is to prevent moving the wrist during gaming. 

### Rotors
The illustration does not show the rotors on the keyboard. The keyboard consists of two rotors. The rotor on the right side controls the volume on the system. When this rotor is pressed, it mutes the audio. The left rotor controls media. You can use this rotor to fast forward / rewind media on the system. When rotor is pressed, it pauses/resumes media on the system.

## How do I flash the firmware on the keyboard?
- Install qmk (for macOS: `brew install qmk/qmk/qmk`)
- Setup qmk with `qmk setup`
- Move the `CustomNordicMathias` folder to `{qmk install directory}/keyboards/sofle/keymaps`
- Compile firmware with `qmk compile -kb sofle -km CustomNordicMathias`
- Disconnect the TRSS cable between the splitted keyboard parts
- Connnect one of the halves to USB and run `qmk flash -kb Sofle -km CustomNordicMathias`
- Click on reset button on keyboard 4 times and wait for flash to complete
- Connect the other half to USB and again run `qmk flash -kb Sofle -km CustomNordicMathias`
Again click on the reset button 4 times and wait for flash to complete, disconnect when done
- First connect TRSS cable and then connect USB cable on the left part. The keyboard should now be flashed.
