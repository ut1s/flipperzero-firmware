# ut1s's Flipper Zero firmware

<img src="https://user-images.githubusercontent.com/110339660/187163324-7ad7edc7-107e-424d-9450-58408a90e4ee.png" width="200" />

*This is a very cute image, isnt't it?* Generated with [__DALL·E 2__](https://openai.com/dall-e-2/)


Welcome to my fork of the official FlipperZero repo!
It's a flipperzero-firmware repository by me but with some changes like plugins, with own graphics and more! (I hope :sweat_smile:)

This repo will be merged from the official and from the non official firmwares to make an ultimate firmware including games and plugins.
So in the most of the time I'll not really write codes but I'll **always** mention the creator of that part of the code. Soo if there is an issue then -I hope- most of the time it'll not be due to my code :sweat_smile:

I hope it will be a weekly ~~(or sometimes montly)~~ updated firmware and I will the include those cool changes which made on that week ~~(/in that month)~~

In the next days (or weeks) I'll update this ReadMe file to make it more ut1sish but til that I'll not change it very and just delete the for this non nessecary things.

# Clone the Repository

You should clone with 
```shell
$ git clone --recursive https://github.com/ut1s/flipperzero-firmware.git
```

# Update firmware

I hope I can do releases for this repo so you can easily just download the .dfu file and install with qFlipper but until then you can still use `fbt` command to build it!

# Fork changes
*An always updating part of the ReadMe*

The parts from firmwares and from another places:

## Apps

### BadUSB

A great user [dummy-decoy](https://github.com/dummy-decoy) made a program for PC and for Flipper so you can easily add any kind of keyboard layouts by copying the dummy-decoy's program created .kl files to the SD card and then just simply select it. Due to this `DUCKY_LANG` is not aviable for the scripts. (Just simply delete it form the first line :sweat_smile:) His repo for this is there (download it to generate your keyboard layout file): [the best way for this](https://github.com/dummy-decoy/flipperzero_badusb_kl)
This part is from the [Unleashed firmware](https://github.com/Eng1n33r/flipperzero-firmware/tree/dev/applications/bad_usb)

### SubGHz

This part is from the [Unleashed firmware](https://github.com/Eng1n33r/flipperzero-firmware/tree/dev/applications/subghz) too. It means there is support for many rolling code protocols but the region restrictions are still there (btw I'm not sure about that :sweat_smile:)

### Infrared

Now you can use universal remote not just to TVs but also to ACs, projectors, fans and audio bars! The original is from the [Unleashed firmware](https://github.com/Eng1n33r/flipperzero-firmware/tree/dev/applications/infrared)


## Plugins

- Count Down Timer ([by 0w0mewo](https://github.com/0w0mewo/fpz_cntdown_timer))
- DAP Link ([by DrZlo13)[OFW]](https://github.com/flipperdevices/flipperzero-firmware/pull/1897))
- DTMF Dolphin ([by litui](https://github.com/litui/dtmf_dolphin))
- Intravelometer ([by theageoflove](https://github.com/theageoflove/flipperzero-zeitraffer))
- Simple Clock (from [Unleashed firmware (fixed](https://github.com/Eng1n33r/flipperzero-firmware) ([Original by CompaqDisk](https://gist.github.com/CompaqDisc/4e329c501bd03c1e801849b81f48ea61))
- Metronome ([by panki27](https://github.com/panki27/Metronome))
- Morse Code ([by wh00hw](https://github.com/DarkFlippers/unleashed-firmware/pull/144))
- Mouse Jacker ([by mothball187](https://github.com/mothball187/flipperzero-nrf24/tree/main/mousejacker))
- Mouse Jiggler ([by Jacob-Tate](https://github.com/Jacob-Tate/flipperzero-firmware/blob/dev/applications/mouse_jiggler/mouse_jiggler.c)))
- MultiConverter plugin ([by theisolinearchip](https://github.com/theisolinearchip/flipperzero_stuff))
- Paint by ([n-o-T-I-n-s-a-n-e](https://github.com/n-o-T-I-n-s-a-n-e))
- Password Generator ([by anakod](https://github.com/anakod/flipper_passgen))
- Pomodoro Timer ([by sbrin](https://github.com/sbrin/flipperzero_pomodoro))
- Spectrum Analyzer ([by jolcese](https://github.com/jolcese/flipperzero-firmware/tree/spectrum/applications/spectrum_analyzer))
- Sub-GHz Bruteforcer ([by Ganapati & xMasterX](https://github.com/DarkFlippers/unleashed-firmware/pull/57))
- Sub-GHz Playlist ([by darmiel](https://github.com/darmiel/flipper-playlist))
- UPC-A Barcode generator plugin ([by McAzzaMan](https://github.com/McAzzaMan/flipperzero-firmware/tree/UPC-A_Barcode_Generator/applications/barcode_generator))
- USB HID Autofire ([by pbek](https://github.com/pbek/usb_hid_autofire))
- USB Keyboard ([by huuck](https://github.com/huuck/FlipperZeroUSBKeyboard))
- WAV player plugin (fixed) ([OFW: DrZlo13](https://github.com/flipperdevices/flipperzero-firmware/tree/zlo/wav-player))

## Games

- Arkanoid (with fixes) ([by gotnull](https://github.com/gotnull/flipperzero-firmware-wPlugins))
- Dice ([by RogueMaster](https://github.com/RogueMaster/flipperzero-firmware-wPlugins/tree/420/applications/plugins/dice))
- Dice 2 ([by Ka3u6y6a](https://github.com/Ka3u6y6a/flipper-zero-dice))
- Doom ([(by p4nic4ttack](https://github.com/p4nic4ttack/doom-flipper-zero/))
- Solitaire ([by teeebor](https://github.com/teeebor/flipper_games)]
- Tetris (with fixes) ([by jeffplang](https://github.com/jeffplang/flipperzero-firmware/tree/tetris_game/applications/tetris_game))
- Tic Tac Toe (with fixes) ([by gotnull](https://github.com/gotnull/flipperzero-firmware-wPlugins))
- ...and Snake of course :sweat_smile:

## Some little changes

### The added assets

- Added my very own Flipper DJ animation. Very rare cool and cute. Check it out!
- Added some infared assets to controll with universal remotes projectors, acs, audios and fans

### Change the animation

- Added a [change](https://github.com/ut1s/flipperzero-firmware/commit/8f0b139bd1f07d82ff94ad449cd1219183427a87) to the firmware that changes to a new idle animation. This is from [RogueMaster's firmware](https://github.com/RogueMaster/flipperzero-firmware-wPlugins/commit/67646a04818d794707624609073704d8ce66921d)

<!---
This is a comment. It won't seen on the page. I hope. You can prewrite the text here and after just get out of this comment.
--->

# Links

~~under construction~~

# Project structure
*(I kept this part lol)*

- `applications`    - Applications and services used in firmware
- `assets`          - Assets used by applications and services
- `furi`            - Furi Core: os level primitives and helpers
- `debug`           - Debug tool: GDB-plugins, SVD-file and etc
- `documentation`   - Documentation generation system configs and input files
- `firmware`        - Firmware source code
- `lib`             - Our and 3rd party libraries, drivers and etc...
- `scripts`         - Supplementary scripts and python libraries home

Also pay attention to `ReadMe.md` files inside of those directories.
