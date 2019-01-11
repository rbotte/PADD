# PADD

PADD (formerly Chronometer2) is a more expansive version of the original chronometer.sh that is included with [Pi-Hole](https://pi-hole.net). PADD provides in-depth information about your Pi-hole.

![PADD](https://jpmck.com/img/blog/padd.png)

## Setup PADD
*More in-depth information about setting up PADD can be found in this repo’s [wiki](https://github.com/jpmck/PADD/wiki/Setup).*

- Get a copy of PADD by running:
```bash
cd ~
wget -N https://raw.githubusercontent.com/rbotte/PADD/master/padd.sh
```
- Make PADD executable by running
```bash
sudo chmod +x padd.sh
```
- Set PADD to auto run by adding the following to the end of `~/.bashrc`:
```bash
# Run PADD
# If we’re on the PiTFT screen (ssh is xterm)
if [ "$TERM" == "linux" ] ; then
  while :
  do
    ./padd.sh
    sleep 1
  done
fi
```
- Reboot your Pi-Hole by running `sudo reboot`. PADD should now run when your Pi-Hole has completed booting.

## Updating PADD
- Just run
```bash
cd ~
wget -N https://raw.githubusercontent.com/jpmck/PADD/master/padd.sh
```

**Note: if you are already running Chronometer2 v1.3.1 or below, you’ll need to follow [these instructions](https://github.com/jpmck/PADD/wiki/Updating-from-Chronometer2)!**

## FAQ
*Answers to frequently asked questions can be found in this repo’s [wiki](https://github.com/jpmck/PADD/wiki/FAQ).*
