# qemu-arm-osx

    $ brew install qemu

# Images

    Raspbian Stretch        https://downloads.raspberrypi.org/
    Debian Buster 64 Bits   https://people.debian.org/~stapelberg/raspberrypi3/2018-01-08/
    Hypriot                 https://blog.hypriot.com/downloads/
    Hypriot 64 bits         https://github.com/DieterReuter/image-builder-rpi64/releases/

# Armv6

    $ qemu-system-arm \
        -M versatilepb \
        -cpu arm1176 \
        -m 256 \
        -hda 2019-04-08-raspbian-stretch-lite.img \
        -net nic \
        -net user,hostfwd=tcp::5022-:22 \
        -dtb versatile-pb.dtb \
        -kernel kernel-stretch \
        -append 'root=/dev/sda2 panic=1' \
        -no-reboot

# Armv7

# Armv8

# Sources

    https://github.com/dhruvvyas90/qemu-rpi-kernel
    
