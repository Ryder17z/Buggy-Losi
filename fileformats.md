# File format descriptions

* TIM: (standard PS1 texture format)
  - Is present in the PC release(s)
  - Only the first slot of each section is ever used, leaving 15 slots always filled with black (0x000000)
  - Animation sequences seem to be stored with the frames sorted backwards
 
* r_pvr2.dll
  Seems to be PowerVR stuff, due to "PCX1" and "PCX2" strings being present in this file
  https://vintage3d.org/pcx2.php
