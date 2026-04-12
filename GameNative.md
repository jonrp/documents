# GameNative Guide


> [!IMPORTANT]
> Get it from https://gamenative.app/

Then after logging into your steam account, make sure to go into settings and toggle off _Auto-apply known config_; While it's supposed to be helpful, you don't really know which config it's fetching (and currently it's really a mess if you go have a look into GameNative's compatibility list). You can always trigger it manually on a game if you feel lucky.

## Default config

This will be the baseline config we use for all games.

- General
  - Container Variant: make sure it's on _bionic_ (default)
  - Wine Version: make sure it's on proton-9.0-arm64ec
  - Screen Size: set it to whatever aspect ratio matches your screen for a 720p height (aka 1280x720 for 16:9)
- Graphics
  - Graphics Driver Version: select the best driver for your chipset (Snapdragon 8Gen2: Mr_Purple T26)
  - Max Device Memory: helps with stability to cap it, 2048 MB for 8 GB peasants, 4096 MB for 16 GB master race
- Emulation
  - 32-bit Emulator: I have it set to FEXCore as it fixed some games for me
  - FEXCore Preset: Intermediate
- Wine
  - Video Memory Size:  helps with stability to cap it, 2048 MB for 8 GB peasants, 4096 MB for 16 GB master race
- Wine Components
  - DirectSound: Setting it to Builtin (Wine) fixed audio for a few games for me
- Environment
  - DXVK_FRAME_RATE: allows you to cap game framerate, usually a good idea to cap at 30 or 40 for better performance / battery life
- Advanced
  - Processor Affinity: uncheck CPU7 for better stability

> [!TIP]
> A new stable version of FEX has come out and is not included in GameNative yet by default, you can download it and import it yourself from https://github.com/StevenMXZ/Winlator-Contents/blob/main/FEXCore/2604.wcp
> 
> From tests so far it improves slightly performance and stability, and generally has new logic to reduce ram usage.

## Troubleshooting running

Now once you install a game, edit the container to select the executable to launch and try to run it, if it fails, a good idea is to run the container and manually run the prerequisites installers (aka PhysX / DirectX / VCRedist). They are normally under C:\Program Files (x86)\Steam\common\steamapp\<gamename>\_CommonRedit, but GameNative seems to have a bug currently that downloads them to the game folder root and doesn't auto install them.

If it still fails, try to switch General > Wine Version to proton-10.0-arm64ec.

If it still fails, try to switch Graphics > DXVK Version to 2.6.1-gplasync; For DirectX 12 games the DX Wrapper will be VK3D and it's worth a shot to try version 3.0b.

Once everything run, you can try to push Emulation > FEXCore Preset > Performance for extra performance (from what I've read Extreme is the same as Performance so no need to go further).

## Troubleshooting graphics

If the games works (DXVK) but with flickering graphics / shadows, switch Graphics > DXVK Version to async-1.10.3

## Troubleshooting controls

Some games will run but with messed up or non responding controls. While this is a known area in needs of improvement in GameNative, so far a couple of games got fixed by doing the following:
- In the game container settings disable SDL / XInput
- Run the container (not the game)
- Go into controls and force the pad into disable state

This is has fixed controls for _Binary Domain_ and _Tokyo Xtreme Racer_.

> [!CAUTION]
> If past this point the game still doesn't work, just give up for now.


## Compatibility list (GameNative v0.9.0)

| Game  | Source | Graphics | Emulation | Notes |
| - | - | - | - | - |
|  |  |  |  |  |

## Improve compatibility

Haven't played that much with that yet, but using nightly build of the various core emulation components should help get more games going, potentially improve performance.

They can be downloaded from there https://github.com/The412Banner/Nightlies/releases

You will want to get the WCP files for:
- DXVK
- FEX
- VK3D
- PROTON
