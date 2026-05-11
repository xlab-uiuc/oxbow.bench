# oxbow.bench
Benchmark for Oxbow file system.

To get benchmark selectively.

```shell
# git submodule update --recursive --init <path>
# For example:

git submodule update --recursive --init micro
```

To get all of them.

```shell
git submodule update --recursive --init -j 4
```

## Setting up file systems

### Ext4

Find the correct device path (You can use `lsblk`). For example, `/dev/nvme0n1`.

Format to ext4 file system and mount it.

```shell
# Format.
sudo mkfs.ext4 /dev/nvmeXnY

# Mount it.
sudo mkdir /mnt/ext4
sudo mount /dev/nvmeXnY /mnt/ext4
```

To run the micro benchmark, refer to `micro/README.md`.
