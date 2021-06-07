# Mount Image Action
An action that mounts an image's `boot` and `root` partitions inside a Ubuntu runner.

# Example
```
- name: Mount Image
      id: mount-image
      uses: damianperera/mount-image-action@v1
      with:
        imagePath: /home/github-runner/rpi4.img
        mountPoint: /mnt/rpi4
```
For a usage example refer [this workflow file](https://github.com/damianperera/openwrt-rpi/blob/main/.github/workflows/build.yml).

# Outputs
| **Value**          | **Description**                                                  |
|---------------------|------------------------------------------------------------------|
| `bootMountLocation` | Mount location of the `boot` partition                           |
| `rootMountLocation` | Mount location of the `root` partition                           |
| `bootDeviceMapper`  | The `boot` partition's mount device (e.g. `/dev/mapper/loop5p0`) |
| `rootDeviceMapper`  | The `root` partition's mount device (e.g. `/dev/mapper/loop5p1`) |
