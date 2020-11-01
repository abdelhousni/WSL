# Windows10 WSL2 Ubuntu / Debian # apt-get update failed # no network
source : https://stackoverflow.com/questions/60269422/windows10-wsl2-ubuntu-debian-apt-get-update-failed-no-network

## Problem : apt update doesn't from from a newly installed WSL2 Debian/Ubuntu

## Solution :

1.  Create a file: `/etc/wsl.conf`.
2.  Put the following lines in the file

    [network]
    generateResolvConf = false
    

1.  In a `cmd` window, run `wsl --shutdown`
2.  Restart WSL2
3.  Create a file: `/etc/resolv.conf`. If it exists, replace existing one with this new file.
4.  Put the following lines in the file

    nameserver 8.8.8.8
