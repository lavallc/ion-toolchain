#ION Toolchain

This project contains everything needed to build for the NRF51822 on OSX and Linux

##Usage

This nrf51 lava toolpack is meant to be used with the ion source code repository, located at https://github.com/lavallc/ion.

##Installation

1. install ubuntu 14.04
2. install all updates
3. sudo apt-get install lib32gcc1
4. place this ion-toolchain folder into /opt
5. clone https://github.com/lavallc/ionode into /opt and follow installation instructions in the ionode README
6. ensure that ionode is working to control your ION
7. clone https://github.com/lavallc/ion somewhere and cd into the dir
8. cd embedded/firmware/gcc/
9. make
10. make flash (ION must be in DFU mode by tapping 3 times on powerup)

##Contents

This is merely information regarding how this repo was built. Please ignore if you are just concerned with setting up your environment.

####gcc/
This is the latest [gcc-arm-none-eabi toolchain](https://launchpad.net/gcc-arm-embedded/+download) from launchpad (not the same as codesourcery)


````
billy@mba:/opt/nrf-toolchain(master⚡) » gcc/bin/arm-none-eabi-gcc --version                  1 ↵
arm-none-eabi-gcc (GNU Tools for ARM Embedded Processors) 4.7.4 20130613 (release) [ARM/embedded-4_7-branch revision 200083]
````


####jlink/
This is the latest JLink OSX Tools download from [Segger](http://http://www.segger.com/debug-probes.html)

It contains the JLink flasher as well as the JLinkGDBServer