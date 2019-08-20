# Pi-Motioneye

Motioneye based CCTV setup on Pi ZeroWs

## Setup Cameras

[Installation Instructions](https://github.com/ccrisan/motioneyeos/wiki/Installation)


Need to pre-configure WiFi [as detailed here](https://github.com/ccrisan/motioneyeos/wiki/Wifi-Preconfiguration).

Initial un/pw is "admin"/""

Best results:

- use the latest image
- write `wpa_supplicant.conf` before first boot
- connect camera before first boot

## Setup server

Install the latest Rasbian

[Manually install motioneye](https://github.com/ccrisan/motioneye/wiki/Manual-Download-And-Installation)

[Raspbian instructions](https://github.com/ccrisan/motioneye/wiki/Install-On-Raspbian) helped too.

I had to try a couple times to get the right dependencies `apt` installed.

`mkdir ~/motioneye` and follow the instructions to copy configs.

Upgrade and restart:

```
pip install motioneye --upgrade
systemctl restart motioneye
```

## Troubleshoot

`vcgencmd get_camera` to see if Pi knows about camera
