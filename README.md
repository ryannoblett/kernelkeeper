# kernelkeeper
### Script for maintaining kernels on Ubuntu

A consistent issue I've had with Ubuntu when using unattended-upgrades is that it never remomves the old kernels like it's supposed to. This is a problem because it can quickly fill up your filesystem, especially if you have a separate /boot. To solve this, I wrote kernelkeeper, a simple shell script that intelligently removes unused kernels. Simply place it in /etc/cron.weekly (or daily/monthly, your preference) and it will check all the kernels in /boot, and remove all except for the current running kernel, and the most recent kernel for each kernel metapacakge you have installed (generic, rt, and so on).
