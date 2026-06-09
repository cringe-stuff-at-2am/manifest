LineageOS (another personal custom fork) - Android 14 QPR1 branch
===========

Getting started
---------------

To get started with Android/LineageOS, you'll need to get familiar with [Source Control Tools](https://source.android.com/setup/develop).

To initialize your local repository using the LineageOS trees, use a command like this:
```
repo init -u https://github.com/cringe-stuff-at-2am/manifest.git -b lineage-21.0-uq1a --git-lfs

# alternate way, to save up the disk space
repo init -u https://github.com/cringe-stuff-at-2am/manifest.git -b lineage-21.0-uq1a --git-lfs --depth=1
```
Then to sync up:
```
repo sync -j$(nproc --all) -c --force-sync --no-clone-bundle --no-tags --prune
```

Build
-----
```sh
. build/envsetup.sh
lunch lineage_DEVICE-user # or userdebug
m bacon

# alternate way
. build/envsetup.sh
brunch DEVICE user
```