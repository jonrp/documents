# GameNative Guide


Once installed, don't forget to import your own secret console firmware dump and matching prod dot keys file.
Also from the app itself fetch and install / select the adviced custom GPU driver.

## Default Config

This will be the baseline config we use for all games.
- Set **System > Docked Mode** to *Enabled* unless you're tight on RAM
- Set **Applets > Airplane Mode** to *Enabled*
- Set **Graphics > Optimise SPIRV output** to *On Load*
- Set **Graphics > GPU Mode** to *Fast*
- Set **Graphics > Anisotropic filtering** to *x16*
- Set **Graphics > ASTC Decoding Method** to *GPU*
- Set **Graphics > ASTC Recompression Method** to *Uncompressed*
- Set **Graphics > Disk shader cache** to *Enabled*
- Set **Graphics > Extended Dynamic State** to *1*
- Set **Graphics > Provoking Vertex** to *Enabled*
- Set **Graphics > Descriptor Indexing** to *Enabled*

## Troubleshooting

Generally two things allow to fix most problematic games:
- Set **Graphics > GPU Mode** to *Accurate*
- Set **Debug > CPU backend** to *Dynarmic (JIT)*
