# ut1s's Flipper firmware

<img src="https://user-images.githubusercontent.com/110339660/187163324-7ad7edc7-107e-424d-9450-58408a90e4ee.png" width="200" />

*This is a very cute image, isnt't it?* Generated with [DALL·E 2](https://openai.com/dall-e-2/)


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

I hope I can do releashes for this repo so you can easily just download the .dfu file and install with qFlipper but until then you can still use `fbt` command to build it!

# Fork changes
*An always updating part of the ReadMe*

The parts from firmwares:

##BadUSB thing

A great user [dummy-decoy](https://github.com/dummy-decoy) made a program for PC and for Flipper so you can easily add any kind of keyboard layouts by copying the dummy-decoy's program created .kl files to the SD card and then just simply select it. Due to this `DUCKY_LANG` is not aviable for the scripts. (Just simply delete it form the first line :sweat_smile:) His repo for this is there: [the best way for this](https://github.com/dummy-decoy/flipperzero_badusb_kl)
This part is from the [__UNLEASHED__ firmware](https://github.com/Eng1n33r/flipperzero-firmware/tree/dev/applications/bad_usb)

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
