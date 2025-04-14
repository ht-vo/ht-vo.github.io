# **KB01** Sparkle Arc A310 ECO Fan Issue

!!! warning annotate "To acknowledge"

    This procedure is based on my own **experimentation**. 
    
    **No support will be provided for this procedure.**

## Context

At the start, I was pleased with the purchase because the GPU looked great on the paper for encoding and transcoding media. 

However, in reality, the fan keeps revving up and down, and the noise drove me crazy... Some others have the issue too.

## Solution

???+ info annotate "Source"
    Big up to @qualmstatic for his [tutorial](https://forum.jellyfin.org/t-flash-intel-arc-gpu-firmware-in-linux?pid=52180#pid52180) that fixed the issue.

    **Tested version**: 101.6653

    **Issue Status**: Not resolved (just less louder)

I assume that all the following action will be executed in the same directory.

1. Download `igsc` binary

    ```shell
    curl -fL https://github.com/Solaris17/ARC-Firmware-Tool/archive/refs/tags/1.44.tar.gz | tar -xz \
    && cd ARC-Firmware-Tool-1.44/Linux\ Build \
    && chmod +x igsc
    ```

1. Download Intel Arc firmware

    ```shell
    curl -fLO https://github.com/Solaris17/Arc-Firmware/raw/refs/heads/master/101.6653/dg2_gfx_fwupdate_SOC2.bin -O https://github.com/Solaris17/Arc-Firmware/raw/refs/heads/master/101.6653/fwdata.zip

    unzip -q fwdata.zip
    ```

1. Check the current firmware version

    ```shell
    sudo ./igsc list-devices
    ```

    ```shell
    sudo ./igsc fw version --device /dev/mei1
    ```

1. Flash the latest firmware version

    ```shell
    sudo ./igsc fw update --device /dev/mei1 --image dg2_gfx_fwupdate_SOC2.bin
    ```

    ```shell
    sudo ./igsc fw-data update --device /dev/mei1 --image fwdata/dg2_sparkle_lp-eco-a310_config-data.bin
    ```