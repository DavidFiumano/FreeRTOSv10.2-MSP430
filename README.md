# FreeRTOSv10.2-MSP430
This is a port of FreeRTOS for the MSP430. It has been tested on the MSP430FR5994 and MSP430FR5969. It is meant to be used with TI's Code Composer Studio. It's taken and modified slightly from the official FreeRTOS demo for the MSP430FR5969.

To use, download the files, add them manually to your project, then put FreeRTOS/include into your include directory.
You still need to configure the clocks. In FreeRTOSMissingPortFuncs.cpp I have the code which sets up the timer. If you want to use a timer clocked by something other than the 32 kHz LXFT on the launchpads, then you need to change usCLK_Frequency_Hz in FreeRTOSMissingPortFuncs.cpp.

# IMPORTANT NOTES:
I don't currently make any effort to support dynamic memory allocation. If you'd like to, take the heap file you want from the MSP430FR5969 demo in the official FreeRTOS source. I use this for code which needs to be fairly reliable, so I avoid dynamic memory allocation when possible. Due to this, I do not think I will ever be supporting dynamic memory allocation on this repo.

If you have any questions email me at dfiumano@gmu.edu.
