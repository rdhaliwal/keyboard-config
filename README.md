# Configuring the keyboard

- Configure the keymap on the website tool: 
  - https://drop.com/mechanical-keyboards/configurator
  <!-- - https://drop.com/mechanical-keyboards/configurator/config/16907 -->
- Hit the compile and download in the top right
  - This will be a download named something like `massdrop_ctrl_config_ctrl__default_16907.bin`
- Download the latest loader files:
  - https://github.com/Massdrop/mdloader/releases
  - Get both `applet-mdflash.bin` and `mdloader_mac` (or whatever OS)
  - Don't use Safari to download it, it does weird things
- Run `chmod u+x mdloader_mac` to make it executable
- Get all 3 files in the same directory:
  - `applet-mdflash.bin`  
  - `mdloader_mac` 
  - `massdrop_ctrl_config_ctrl__default_16907.bin`
- To load the custom firmware, run `./mdloader_mac --first --download massdrop_ctrl_config_ctrl__default_16907.bin --restart`
  - Hit the reset button in the back of the keyboard, 
  - This should turn off the LEDs on the keyboard
  - Hit `fn + b` on the keyboard
  - The program should pick up the keyboard and load it
  - The LEDs should return and the keyboard should be working again.
- DO NOT RUN `./mdloader_mac --first --download applet-mdflash.bin --restart`. 
  - **THIS WILL BRICK IT**, despite the console saying it was successful
  - https://drop.com/talk/9382/how-to-configure-your-ctrl-keyboard
- The keyboard should be working with the custom keyboard config.
