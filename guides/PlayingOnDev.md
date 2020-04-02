# Playing on the Development version
So you've decided to playtest the newest features yourself. Please note that while the current dev version is *pretty* stable, it's still dev - you may encounter bugs and problems (please report to the tracker if you do!). That said, 1.2.2 already has a ton of upgrades over 1.2.1, so it's not strange to want to try them out.

1.2.2 currently does not require a new world (it's specifically made not to), although, well, it's a dev version, so make sure to have a backup.

## Installation
The process is nice and simple: download the zip of the repo's current state([link](https://github.com/Exaxxion/Omnifactory/archive/1.3-PR.zip), or go to [the repo](https://github.com/OmnifactoryDevs/Omnifactory) and push the big green `Clone or Download` button and choose to download the zip).

This zip can then be imported into a nice launcher like MultiMC. In MultiMC, you can do this by going Add Instance - Import from Zip and choosing the zip you downloaded. Note: you might want to include in the instance's name a reference to the specific state of the repo. The best way to do it is to look at the last commit at the moment you're downloading the pack and include it in the instance's name:

![latest commit](files/UnofficialFixes/LatestCommit.png)

These actions are enough to install the dev version, but...

## Installing Fixes

...it still doesn't have those fixes that curseforge can't ship - ones that consist of custom jars. So you need to do similar things to [the 1.2.1 fixes guide](InstallingUnofficialFixes121.md), but with minor differences. Mod updates are **unneeded** - those can and are shipped in the modpack proper.

Here's a full list of popular custom jars - in all cases, you replace the original jar in your `mods` folder with the new one:

- Exa's [GTCE](files/UnofficialFixes/jars/gregtech-1.12.2-1.8.4.419exa2.jar) and [Shadows of Greg](files/UnofficialFixes/jars/Shadows_of_Greg-1.12.2-2.8.0_fix.jar) jars. Are backports of GTCE/SoG fixes on Omni's version of GTCE.
- Talchas's AE2 fix. See [the section on it](InstallingUnofficialFixes121.md#talchass-ae2-fix) in the 1.2.1 fixes guide. The only change is that **for 1.2.2 you need the** rv6-stable-**7** version.
