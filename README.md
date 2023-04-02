 [![Download Pixel Extended-ROM](https://img.shields.io/sourceforge/dm/pixelextended.svg)](https://sourceforge.net/projects/pixelextended/files/latest/download)

# Pixel Extended #
<img src="https://imgur.com/likQDEZ.png">

### Initialize local repository ###

```bash
repo init -u https://github.com/PixelExtended/manifest -b thunder
```
 or you can do a shallow clone if you dont't have much bandwidth
```bash
repo init -u https://github.com/PixelExtended/manifest -b thunder --depth=1
```
Shallow clone lets you pull down just the latest commits, not the entire repo history. So if your project has years of history, or history from thousands of commits, you can select a particular depth to pull.

So if we are providing argument of `-- depth 1` to the repo init command it will copy only the latest revision of a repo.

### Sync ###

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
You can just use `repo sync` or above command, but this will save you from lot of terminal spam, data and time.
```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -jX
```
