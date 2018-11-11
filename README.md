TWRP device tree for Galaxy J7 (2016 Exynos7870)

Building Instructions
*The sources are for 6.0 MM,So Follow Steps Below..

To initialize your local repository using the OMNIROM trees to build TWRP, use a command like this:
```
repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-6.0
```

Then to sync up:
```
repo sync
```

We are using 6.0 sources so to build latest twrp we need to clone latest  bootable/recovery

```bash
rm -rf bootable/recovery
git clone https://github.com/omnirom/android_bootable_recovery -b android-8.1 bootable/recovery
```

Syncing Twrp Device Trees

```
repo sync

. build/envsetup.sh
lunch
mka recovery image
```

Done 

Happy Flashing
