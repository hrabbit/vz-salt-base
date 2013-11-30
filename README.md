vz-salt-base
============

Create a base package that allows dab creations to be deployed purely for use in salt networks. This image sets the salt master (if requested), and configures eth0 to be DHCP enabled. The idea behind this is that you would use salt to define a new network configuration for your minions after they come online.

Usage
-----

Ensure dab is installed.

`apt-get install dab`

Next, we need to grab the repository... See Github for all that wizbang stuff..

Finally, we jump into the directory of the build we want.

`cd vz-salt-base/debian-7.0-minimal`

And we run...

`make`

Optionally, you can call make with a defined salt master defined. (Default: salt)

`make SALT-MASTER=192.168.0.5`

This will create your base image with salt already deployed.

You can then move the resulting tar.gz file to your pve templates directory.
