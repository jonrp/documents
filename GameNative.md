# GameNative Guide


> [!IMPORTANT]
> Get it from https://gamenative.app/


## Default config

> [!NOTE]
> A new stable version of FEX has come out and is not included in GameNative yet by default, you can download it and import it yourself from https://github.com/StevenMXZ/Winlator-Contents/blob/main/FEXCore/2604.wcp
> 
> From tests so far it improves slightly performance and stability, and generally has new logic to reduce ram usage.

## Troubleshooting running

## Troubleshooting graphics

## Troubleshooting controls

Some games will run but with messed up or non responding controls. While this is a known area in needs of improvement in GameNative, so far a couple of games got fixed by doing the following:
- In the game container settings disable SDL / XInput
- Run the container (not the game)
- Go into controls and force the pad into disable state

This is has fixed controls for **Binary Domain** and **Tokyo Xtreme Racer**.

> [!WARNING]
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
