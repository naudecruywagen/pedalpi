# pedalpi

## Getting set up

[SSH into Pi Zero over USB](https://desertbot.io/blog/ssh-into-pi-zero-over-usb)

If you get the message 'Host raspberrypi.local not found in /Users/[user]/.ssh/known_hosts' when running 
`ssh-keygen -R raspberrypi.local` ignore it.

### Installing the BCM2835 Libraries

`curl http://www.airspayce.com/mikem/bcm2835/bcm2835-1.55.tar.gz -o bcm2835-1.55.tar.gz`

`scp bcm2835-1.55.tar.gz pi@raspberrypi.local:bcm2835/bcm2835-1.55.tar.gz`

### Compile and execute c file

`gcc -o example -l rt example.c -l bcm2835`

`./example`
