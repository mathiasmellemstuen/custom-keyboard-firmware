# keyboard_qmk_firmware
Firmware for my custom splitted keyboard with nordic design.

# Installation
- Install qmk (for macOS: `brew install qmk/qmk/qmk`)
- Setup qmk with `qmk setup`
- Clone this repository to `{qmk install directory}/keyboards/sofle/keymaps`
- Compile firmware with `qmk compile -kb sofle -km CustomNordicMathias`
- Disconnect the TRSS cable between the splitted keyboard parts
- Connnect one of the halves to USB and run `qmk flash -kb Sofle -km CustomNordicMathias`
- Click on reset button on keyboard 4 times and wait for flash to complete
- Connect the other half to USB and again run `qmk flash -kb Sofle -km CustomNordicMathias`
Again click on the reset button 4 times and wait for flash to complete, disconnect when done
- First connect TRSS cable and then USB cable on the left part
