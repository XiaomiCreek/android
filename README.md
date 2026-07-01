# Initialize local repository

The repo init will depend on the Rom you choose. 
For example:
- Lineage
```
repo init -u https://github.com/LineageOS/android.git -b lineage-23.2 --git-lfs
```
- Evolution-X
```
repo init -u https://github.com/Evolution-X/manifest -b cnb --git-lfs
```

# Clone your local manifest for Device
```
git clone https://github.com/project-creek/xiaomi-creek.git -b 16 .repo/local_manifests
```

# Sync up
```
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

# Build

- Set up the build environment
```
. build/envsetup.sh
```

- Lunch a target
```
lunch lineage_codename-cp2a-user
```

- To start compiling
```
m evolution or mka bacon
```
