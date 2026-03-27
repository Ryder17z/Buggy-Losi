# Buggy-Losi

A look into how the old game "Buggy" (PC/PS1) and "Team Losi RC Racer" (USA PS1 port) works

# Car Names

In order as they are stored on the respective disc

| Buggy                 | Team Losi RC Racer   |
|-----------------------|----------------------|
| CLOCK WAGON           | KRUSH                |
| KRAVEN KULLER         | VIXXEN               |
| LUSH BUG              | FLAME DRAGON         |
| BLOOP                 | SCORPION             |
| VENOM                 | VENOM                |
| BLZ-808               | ROAD NINJA           |
| SOULSHARK BUGGEE      | XXT CR GRAPHITE PLUS |
| SKRATCH TRRAX XS-2000 | OUTLAW               |
| STOMP!                | XX4                  |
| KEFFISH               | LAND SHARK           |
| WASPEE                | DIRT DOG             |
| R-B-MK4000            | MOOK-808             |
| CARAPACE              | REAPER               |
| MOOT-8                | CHUPACABRA           |
| HARD CORPS            | HARD CORPS           |
| TASTY                 | BAD BOY              |

Although the order for the names remains the same, the stats do differ between "Losi" and "Buggy".

The bonus car order might also have changed. Uncomfirmed, but possible.

# DLLs

* r_pvr2.dll
  Seems to be PowerVR stuff, due to "PCX1" and "PCX2" strings being present in this file
  https://vintage3d.org/pcx2.php

# File format descriptions

* TIM: (standard PS1 texture format)
  - Is present in the PC release(s)
  - Only the first slot of each index is ever used, leaving 15 slots always filled with black (0x000000)
  - Animation sequences seem to be stored with the frames sorted backwards
  - Font that should be yellow, orange-brown or greyscale is blue.
  - Location of sprite masks and etc is currently unknown*

Example: MAPS\E_MAPS\MAP9\PIMS\TIMS.PIM

| Slot 0 content | Description |
|----------------|-------------|
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

# Save Data

EU/US savedata is not interchangable.
Attempts to save data prompts the insertion of the "correct" game disc. Likely caused by hardware regions rather than the game itself
