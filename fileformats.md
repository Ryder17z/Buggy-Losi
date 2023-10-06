# File format descriptions

* TIM: (standard PS1 texture format)
  - Is present in the PC release(s)
  - Only the first slot of each index is ever used, leaving 15 slots always filled with black (0x000000)
  - Animation sequences seem to be stored with the frames sorted backwards
  - Font that should be yellow, orange-brown or greyscale is blue.
  - Location of sprite masks and etc is currently unknown*

Example: MAPS\E_MAPS\MAP9\PIMS\TIMS.PIM

| Slot 0 content | Description |
| -------------- | ----------- |
| [92][00]       | Frame 7     |
| [93][00]       | Frame 6     |
| [94][00]       | Frame 5     |
| [95][00]       | Frame 4     |
| [96][00]       | Frame 3     |
| [97][00]       | Frame 2     |
| [98][00]       | Frame 1     |
| [99][00]       | Frame 0     |

![buggy_waterfall](https://github.com/Ryder17z/Buggy-Losi/assets/2000703/34bc1451-4f2c-49a8-a744-4da92ba92007)

Note: GIF animation speed has been roughly estimated.

* r_pvr2.dll
  Seems to be PowerVR stuff, due to "PCX1" and "PCX2" strings being present in this file
  https://vintage3d.org/pcx2.php
