# Ubuntu 22.04



## Installation

### [Youtube](https://www.youtube.com/playlist?list=PLGZ6M30GmbVM6qM-t1w5V0XBpHc_mNKYj)



## Configuration

### Chinese Keyboard

1. Open Settings, go to `Language and Region` -> `Manage Installed Languages` -> `Install / Remove languages`.
2. Select `Chinese (Simplified)`. Make sure `Keyboard Input method system` has `Ibus` selected. Apply.
3. Reboot
4. Log back in, reopen Settings, go to `Keyboard`.
5. Click on the "+" sign under `Input sources`.
6. Select `Chinese (China)` and then `Chinese (Intelligent Pinyin)`.



### [Fix Windows and Linux Showing Different Times When Dual Booting](https://www.howtogeek.com/323390/how-to-fix-windows-and-linux-showing-different-times-when-dual-booting/#:~:text=By%20default%2C%20Windows%20assumes%20the,make%20Windows%20use%20UTC%20time.)

#### Make Linux Use Local Time to Fix Time Discrepancy

Run the following command to put the real time clock on the motherboard into local time. Linux will store the time in local time, just like Windows does.

```bash
timedatectl set-local-rtc 1 --adjust-system-clock
```

You will not get any feedback after you execute the command. To check your current settings, run:

```bash
timedatectl
```

If you see "RTC in local TZ: yes", Linux is set to use the local time zone instead of UTC. The command warns you that this mode is not fully supported and can cause some problems when changing between time zones and with daylight savings time. However, this mode is probably better supported than the UTC option in Windows. If you dual-boot with Windows, Windows will handle daylight savings time for you.

If you ever want to undo this change, run the following command:

```bash
timedatectl set-local-rtc 0 --adjust-system-clock
```

