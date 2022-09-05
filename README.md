# Marlin 2 Build Site
 
Contains the additional files I need for building Marlin 2.x for my 3D printer

## Directions
Use a different branch for each version of Marlin you want to build. Hopefully you will be able to branch from the
previous one without too much effort. Of course, that may not be true if I'm lazy and go a few years between upgrades 
while the busy Marlin developers go changing things hither and yon. In that case, I may be in for a bit of work.

- Download the distro and Configurations for the version you want.
- Go to the Configurations example folder and find the one for the Wand Duplicator i3 2.1. This is the same as
  the Monoproce Maker Select v2 and is our starting point.
- Copy the Configuration.h and Configuration_adv.h from there to Brads_MMS_V2
- Merge those files from the version of Marlin you're currently running onto the versions you just copied. The goal
  is to incorporate any new configuration settings while retaining your old ones.
- Unpack the Marlin distro. It will probably be in a folder named 2.1.1 or something similar
- Edit buildMarlin.sh to use the new folder name
- Run buildMarlin.sh
- Copy the resulting .hex file from artifacts/ to the octopi and run flashMega.sh

