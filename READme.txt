# launch bush file (Ubuntu 20.04)
./launcher

# launch docker jlink container 
docker run -it --rm --privileged -v /dev:/dev -v /JLink/project_watch:/project_watch fjmolinas/jlink

# inside container type the follow command
cd /opt/SEGGER/JLink

# launch JLink and connect to the microcontroller
./JLinkExe
