**Install PulseAudio Volume Control (pavucontrol):**

```shell
sudo apt install pavucontrol
```
**Now we will route your microphone to your speakers. Do this by running the following command:**

```shell
pactl load-module module-loopback latency_msec=1
```

On the Recording tab of pavucontrol, you can show all streams (combobox at the bottom) and then configure which microphone (if you have more than one) should loopback into the built-in analog stereo

**To stop it running, run:**

```shell
pactl unload-module module-loopback
```

---

>source: https://askubuntu.com/a/262297