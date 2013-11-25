vz-salt-base
============

Create a base package that allows dab creations to be deployed purely for use in salt networks.

Usage
-----

Ensure dab is installed.

`apt-get install dab`

Next, we need to grab the repository... See Github for all that wizbang stuff..

Finally, we jump into the directory of the build we want.

`cd vz-salt-base/debian-7.0-minimal`

And we run...

`make`

This will create your base image with salt already deployed.

You can then move the resulting tar.gz file to your pve templates directory.
