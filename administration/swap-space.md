# Enabling Swap Space

Swap space is necessary for the database components to function properly.

## Swap Size

For production servers, set swap to 50% of the physical memory.

For testing systems, set swap to 100% of the physical memory.

Check available memory:

```sh
free
```

<!-- markdownlint-disable MD107 -->

```ls
             total       used       free     shared    buffers     cached
Mem:       1922136    1274196     647940         32      92508     315664
-/+ buffers/cache:     866024    1056112
Swap:      2064380      31016    2033364
```

<!-- markdownlint-enable MD107 -->

## Enabling Swap

The following instructions describe how to create swap without restarting the server.

Create 1 GB file (`1M * 1024`). Increase `count=` as appropriate.

```sh
sudo dd if=/dev/zero of=/swapfile bs=1M count=1024
```

Set permissions and configure the swap file.

```sh
sudo chmod 0600 /swapfile
```

```sh
sudo mkswap /swapfile
```

Enable swap.

```sh
sudo swapon /swapfile
```

Enable swap on boot.

```sh
sudo echo "/swapfile swap swap defaults 0 0" >> /etc/fstab
```

Verify that the swap is enabled.

```sh
free
```

The output must contain a row with Swap total not equal to zero.
<!-- markdownlint-disable MD107 -->

```ls
             total       used       free     shared    buffers     cached
Mem:       7697000    6104904    1592096         32      86628    3062424
-/+ buffers/cache:    2955852    4741148
Swap:      1023996          0    1023996
```