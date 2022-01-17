# launch bush file (Ubuntu 20.04)
./launcher

# launch docker jlink container 
docker run -it --rm --privileged -v /dev:/dev -v /home/JLink/im_ok_firmware:/im_ok_firmware fjmolinas/jlink

# inside container type the follow command
cd /opt/SEGGER/JLink

# launch JLink and connect to the microcontroller
./JLinkExe

##Jlink commander
#
connect
NRF52832_XXAA
S
4000
erase
loadfile /im_ok_firmware/s132_nrf52_7_0_1_softdevice.hex
loadfile /im_ok_firmware/ble_app_template_pca10040_s132.hex
