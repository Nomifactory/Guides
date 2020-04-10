# Playing on the Development version
So you've decided to playtest the newest features yourself. Please note that while the current dev version is *pretty* stable, it's still dev - you may encounter bugs and problems (please report to the tracker if you do!). That said, 1.2.2 already has a ton of upgrades over 1.2.1, so it's not strange to want to try them out.

1.2.2 currently does not require a new world (it's specifically made not to), although, well, it's a dev version, so make sure to have a backup.

## Installation
The process is nice and simple: start by downloading the zip of the repo's current state. For this, we have Neeve's continious integration bot: [latest-dev-preview](https://github.com/OmnifactoryDevs/Omnifactory/releases/tag/latest-dev-preview). This is a github tag that gets updated automativally every time the repository recieves a new change. It has two links you care about: client and server. **Use this server zip if you're not playing in singleplayer; don't try to patch 1.2.1 server files to be compatible with 1.2.2** (disturbingly many people have attempted to).

The client zip can then be imported into a nice launcher like MultiMC. In MultiMC, you can do this by going Add Instance - Import from Zip and choosing the zip you downloaded. Note: you might want to include in the instance's name a reference to the specific state of the repo. This is why the snapshot zips include a weird string like `66833c` - that's the closest a github repo has to a version number.

The server zip, if you need it, is a full server, with Forge and start scripts included. Just unpack it somewhere and run using the script.

These actions are enough to install the dev version, but...

## Installing Fixes

...it still doesn't have those fixes that curseforge can't ship - ones that consist of custom jars. So you might still want to install some of the unofficial fixes available, similar to [the 1.2.1 case ](InstallingUnofficialFixes121.md), but with minor differences. Mod updates are **unneeded** - those can and are shipped in the modpack proper.

Generally, you should install the same fixes on both the server and all clients (although many of them can let you get away with only replacing the jar serverside).

Here's a full list of popular custom jars - in all cases, you replace the original jar in your `mods` folder with the new one:

- Exa's [GTCE](files/UnofficialFixes/jars/gregtech-1.12.2-1.8.4.419exa2.jar) and [Shadows of Greg](files/UnofficialFixes/jars/Shadows_of_Greg-1.12.2-2.8.0_fix.jar) jars. Are backports of GTCE/SoG fixes on Omni's version of GTCE. No, you **don't** need the rest of the Exa's fixes (scripts, etc) - they are integrated into 1.2.2, only the jars aren't.
- Talchas's AE2 fix. See [the section on it](InstallingUnofficialFixes121.md#talchass-ae2-fix) in the 1.2.1 fixes guide. The only change is that **for 1.2.2 you need the** rv6-stable-**7** version.


## Transferring the world over

If you don't wish to start a new world with 1.2.2, you don't have to. You can just transfer your world to the new instance. To do that, navigate to your old instance's `minecraft` folder, then in the `saves` folder find a folder named after your world. Copy *that* entire folder to the `saves` folder of the new instance.

You'll also likely want to copy over the entire `journeymap` folder (in `minecraft`)(your waypoints), as well as `options.txt` (all the options you've tweaked, so that you don't have to ~~set GUI scale to Large once again-~~ configure them again).