
Update RaspberryPi

```sh
sudo apt update && sudo apt upgrade -y && sudo apt dist-upgrade -y
```

Install raspberry utils:

```sh
sudo apt install -y linux-modules-extra-raspi && sudo reboot
```
[Overlcock](https://beebom.com/how-overclock-raspberry-pi-4/)

Add to the end of `/boot/firmware/config.txt`:

```
arm_freq=2300
gpu_freq=750
gpu_mem=32
over_voltage=14
force_turbo=1
```

Add to the end of `/boot/firmware/cmdline.txt`:

```
cgroup_memory=1 cgroup_enable=memory
```

Reboot:

```sh
sudo reboot
```


Check CPU clockspeed:

```sh
watch -n1 vcgencmd measure_clock arm
```

Check CPU temperature:

```sh
watch -n1 vcgencmd measure_temp
```