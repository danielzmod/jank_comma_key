# jank_comma_key
Just a cheap DIY comma key

Searching sites like aliexpress for "usb c test board" you can find test boards like this.
![image](https://github.com/danielzmod/jank_comma_key/assets/33908198/2da8c933-7ba8-46c3-854e-ae1c7f7764bd)

Cutting some traces and adding a ON/OFF button and a push button will be the same as comma key but for a lot less.
![image](https://github.com/danielzmod/jank_comma_key/assets/33908198/904b5ff7-0ced-4130-9844-62d0d0f31efd)

There are even some boards which have usb c female/male to solder pads. Which makes it even easier to put in ON/OFF button in series.
Here is a description of what i did to manufacturer my own "diy comma key".

#TODO: add guide....

# More info
The processor mounted in a black panda is a STM32F413 in a LQFP64 package.
Information from __STM32F413 datasheet__ and application note __AN2606 STM32 microcontroller system memory boot mode__
STM32F413 datasheet
![STM32F413, Boot Modes](https://github.com/danielzmod/jank_comma_key/assets/33908198/3ad95301-3527-41f4-a008-b18ed87e15a3)

![AN2606, Bootloader activation patterns, Pattern 1 is valid for STM32F413](https://github.com/danielzmod/jank_comma_key/assets/33908198/73a9b2d3-c2b2-4fcb-b013-6ff56acfbead)

![STM32F413, Pinout Boot1 pin](https://github.com/danielzmod/jank_comma_key/assets/33908198/1a49f4f9-f75f-4eaa-a77d-2e813b1a7097)

![STM32F413, Pin 1 identifier on package, is in the corner left of ST logo](https://github.com/danielzmod/jank_comma_key/assets/33908198/365306b5-2629-430a-947d-d7664d8275dc)

![STM32F413, LQFP64 pinout](https://github.com/danielzmod/jank_comma_key/assets/33908198/e3ad839e-01db-495c-8fd3-814ac585c9a0)

