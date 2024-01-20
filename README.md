# jank_comma_key
Just a cheap DIY comma key

Searching sites like aliexpress for "usb c test board" you can find test boards like this.
![image](https://github.com/danielzmod/jank_comma_key/assets/33908198/2da8c933-7ba8-46c3-854e-ae1c7f7764bd)

Cutting some traces and adding a ON/OFF button and a push button will be the same as comma key but for a lot less.
![image](https://github.com/danielzmod/jank_comma_key/assets/33908198/904b5ff7-0ced-4130-9844-62d0d0f31efd)

There are even some boards which have usb c female/male to solder pads. Which makes it even easier to put in ON/OFF button in series.
Here is a description of what i did to manufacturer my own "diy comma key".

TODO: add guide....

Other methods:
If anyone accidentally tries to run recover_h7 on your red panda via SSH while it is connected to the C3, you may soft brick your internal Panda. That will result in Camera Malfunction error when you turn on your car with the RP connected. If this did indeed happen, you should also see a "No Panda" in red on OP when your RP is disconnected. 

Copied from Comma Support email:
To fix the internal black Panda, run the following lines one at a time when connected to the device via SSH. You can ignore any output about the device resource being busy.
 
echo 124 > /sys/class/gpio/export
echo "out" > /sys/class/gpio/gpio124/direction
echo 1 > /sys/class/gpio/gpio124/value
 
echo 134 > /sys/class/gpio/export
echo "out" > /sys/class/gpio/gpio134/direction
echo 1 > /sys/class/gpio/gpio134/value
 
echo 124 > /sys/class/gpio/export
echo "out" > /sys/class/gpio/gpio124/direction
echo 0 > /sys/class/gpio/gpio124/value
 
With these done you should see "STM Device in DFU mode" or something similar when you run lsusb. If you do you should be able to run the recover.sh script in the panda folder. It may still be held in DFU after the flash, in which case run the following to get it out of DFU.
 
echo 124 > /sys/class/gpio/export
echo "out" > /sys/class/gpio/gpio124/direction
echo 1 > /sys/class/gpio/gpio124/value
 
echo 134 > /sys/class/gpio/export
echo "out" > /sys/class/gpio/gpio134/direction
echo 0 > /sys/class/gpio/gpio134/value
 
echo 124 > /sys/class/gpio/export
echo "out" > /sys/class/gpio/gpio124/direction
echo 0 > /sys/class/gpio/gpio124/value
