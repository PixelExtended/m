 [![Download Pixel Extended-ROM](https://img.shields.io/sourceforge/dm/pixelextended.svg)](https://sourceforge.net/projects/pixelextended/files/latest/download)

# Pixel Extended #
<img src="https://imgur.com/likQDEZ.png">

### Initialize local repository ###

```bash
repo init -u https://github.com/PixelExtended/manifest -b eleven
```
 or you can do a shallow clone if you dont't have much bandwidth
```bash
repo init -u https://github.com/PixelExtended/manifest -b eleven --depth=1
```
Shallow clone lets you pull down just the latest commits, not the entire repo history. So if your project has years of history, or history from thousands of commits, you can select a particular depth to pull.

So if we are providing argument of `-- depth 1` to the repo init command it will copy only the latest revision of a repo.

### Sync ###

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
You can just use `repo sync` or above command, but this will save you from lot of terminal spam, data and time.
```bash
repo sync -c -q --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
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
### Maintainership ###

If You wish to maintain PixelExtended For your device Officially **Form can be found here:** [Maintainership Application Form](https://docs.google.com/forms/d/e/1FAIpQLScLH2gdeB6FzkOXTrYbBdzReLGgNiD5GiYrMesHLFt8SFDMlw/viewform)

Some Things to Consider before applying :- 

1. Tree Should be maintained properly with authorship .
2. You should be able to fix your device specific issue on your own , saying "me nuub" isn't fun anymore.

That's it , Happy Cooking .
