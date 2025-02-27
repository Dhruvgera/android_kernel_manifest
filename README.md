[<center><img src="https://raw.githubusercontent.com/sourajitk/STX-Logo/main/stx-2021-kernel.png" height="50%" width="50%;" /></center>](https://github.com/StatiXOS)

## Repo Init ##

```bash
repo init -u https://github.com/Dhruvgera/android_kernel_manifest -b master
```

## Sync Source ##

```bash
repo sync --force-sync --no-clone-bundle --current-branch --no-tags -j$(nproc --all)
```

## Build ##

Rename `DEVICE_NAME` with the appropriate device codename

For Clang builds
```bash
BUILD_CONFIG=build.config.xiaomi.${DEVICE_NAME} BUILD_KERNEL=1 build/build.sh
```

For GCC builds
```bash
BUILD_CONFIG=build.config.xiaomi.${DEVICE_NAME} COMPILER=gcc BUILD_KERNEL=1 build/build.sh
```

Example:

For munch with GCC
```bash
BUILD_CONFIG=build.config.xiaomi.munch COMPILER=gcc BUILD_KERNEL=1 build/build.sh
```

### Submitting Patches ###

Please refer to this for submitting patches: https://github.com/StatiXOS/android_manifest#submitting-patches
