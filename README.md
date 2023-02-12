# Portmaster-OpenRCT2


# Installation


# Controls

## BLAH BLAH CONTROLS


To enter text: press **Start + Down**, then use **Up** and **Down** selects the letter, **Left** and **Right** moves forwards and backwards. **Start** or **A** to finish editing.

# Game folder structure

Install your RCT2 game files into `{PORTFOLDER}/openrct2/RCT2`, 

## Required libs

- the following libraries from Debian 11 Bullseye Aarch64
  - libicudata.so.67
  - libicuuc.so.67
  - libzip.so.4

 
## Building

    git clone https://github.com/OpenRCT2/OpenRCT2.git

    cd openrct2

    mkdir build

    cd build

    cmake .. -DCMAKE_BUILD_TYPE=MinSizeRel -DDISABLE_GOOGLE_BENCHMARK="ON" -DDISABLE_DISCORD_RPC="ON" -DPORTABLE="ON" -DCMAKE_INSTALL_PREFIX:FILE="engine"

    make -j4

    make install

    rm -f engine.zip
    rm -f engine/bin/libopenrct2.a
    rm -f engine/bin/openrct2-cli

    zip -9r engine.zip engine/

At the end, you want the `engine.zip`.

# TODO:

- [ ] Get a map to work!
- [ ] Figure out controls
- [ ] Test it on AmberELEC
- [ ] Test it on ArkOS

# Thanks

A special thanks to the excellent folks on the [AmberELEC discord](https://discord.com/invite/R9Er7hkRMe).
