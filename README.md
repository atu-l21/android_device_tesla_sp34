# TWRP Device tree for Alcatel 5059D

## Building instructions

```
mkdir -p ~/twrp && cd ~/twrp
repo init --depth=1 -u https://github.com/5059d/platform_manifest_twrp_omni.git -b twrp-8.1
repo sync
git clone https://github.com/5059d/android_device_alcatel_5059d.git device/alcatel/5059d
git clone https://github.com/5059d/android_device_generic_twrpbuilder.git device/generic/twrpbuilder
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch omni_5059d-eng
mka recoveryimage
```

Your final image will be `recovery.img` in `~/twrp/out/target/product/5059d/`. 

If you encounter any problems, create a Github issue. 

## Acknowledgements

TeamWin, OmniRom, TwrpBuilder

Copyright (c) 2018 5059D Project and contributors. 
