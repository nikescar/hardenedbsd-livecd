LiveCD builder for HardenedBSD

Last updated 06/05/2021

## End-of-life notice for community ISO images
Thank you for your interest in FuryBSD.  This project has been discontinued.  Plans to publish Q4 2020 images have been cancelled.

## What happened to the community telegram, blog, website, and forums?
On 10/30/2020 the telegram channel was comprimised which accelerated the decision to terminate these resources sooner.  Protecting the forums even with the assistance of volenteers from spam has been an uphill battle over the last year.  Those volenteers have moved on from the project.  Simiarly the original volenteer who helped create and maintain wordpress has moved on from the project.  This added overhead, and decrease in volenteers is the primary reason for the decision.  

## What to do if you have installed using the live media?
If you have installed using the live media you can continue [updating and upgrading FreeBSD](https://www.freebsd.org/doc/handbook/updating-upgrading.html), and there is no need for a migration of your installed system.  

## What to do for updated versions of the LiveCD?
If you enjoyed using the LiveCD please see projects which succeed it such as [GhostBSD](http://www.ghostbsd.org).  

## System Requirements for building LiveCD

* 2 GHz dual core processor
* 4 GiB RAM (system memory)
* 50 GB of hard-drive space
* Either a CD-RW/DVD-RW drive or a USB port for writing the installer media
* FreeBSD 12.1-RELEASE or later

## System Requirements for using LiveCD

* 2 GHz dual core processor
* 4 GiB RAM (system memory for physical and viritualized installs)
* VGA capable of 1024x768 screen resolution 
* Either a CD/DVD drive or a USB port for booting the installer media

## Customize (optional)

Add more packages to XFCE edition:
```
edit settings/packages.xfce
```

Enable more services:
```
edit settings/rc.conf.xfce
```

## Build a new release 
Generate an ISO with XFCE:
```
./build.sh
```
Generate an ISO with Gnome3:
```
./build.sh gnome
```
Generate an ISO with KDE Plasma 5:
```
./build.sh kde
```

## Burn

Burn the XFCE image to DVD:

```
pkg install cdrtools
cdrecord /usr/local/furybsd/iso/HardenedBSD-12-stable-XFCE-amd64.iso
```

Write the XFCE image to USB stick:
```
sudo dd if=/usr/local/furybsd/iso/HardenedBSD-12-stable-XFCE-amd64.iso of=/dev/daX bs=4m status=progress
```

## Credentials for live media

There is no password for `liveuser`. The `liveuser` account is removed upon install.  There is also no root password until it is set in the installer.

## Legacy repositories

To keep the current furybsd organization well organized all legacy repositories which are no longer in use have been moved to the furybsd-legacy organization.

https://github.com/furybsd-legacy
