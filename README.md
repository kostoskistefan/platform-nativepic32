# PlatformIO NativePIC32 Platform

A PIC32 PlatformIO platform, which is heavily based on the [platform-microchippic32](https://github.com/platformio/platform-microchippic32), except it does not use any frameworks (like Arduino).
Everything needs to be set up manually, but it gives more control and freedom over what is happening inside the MCU.

The main purpose of this platform is to use a open source PIC32 compiler and have more control over the compiler and linker flags, compared to the free version of the XC32 compiler provided by Microchip.

This platform uses heavy size optimizations in the compiler (`-Os` flag) by default. Of course, this can be overwritten as needed.

The generated `firmware.hex` file can be uploaded either through MPLAB IPE, or the open source `pic32prog` tool, but the latter might need additional configuration (a.k.a. firmware update) of your programmer tool (ex. PICKIT 3).