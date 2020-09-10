Originally written when the dev was 1.2.2, still valid.
# Playing on the Development version
So you've decided to playtest the newest features yourself. Please note that while the current dev version is *pretty* stable, it's still dev - you may encounter bugs and problems (please report to the tracker if you do!). That said, 1.2.2 already has a ton of upgrades over 1.2.1, so it's not strange to want to try them out.

1.2.2 currently does not require a new world (it's specifically made not to), although, well, it's a dev version, so make sure to have a backup.

## Installation
The process is nice and simple: start by downloading the zip of the repo's current state. For this, we have Neeve's continious integration bot: [latest-dev-preview](https://github.com/OmnifactoryDevs/Omnifactory/releases/tag/latest-dev-preview). This is a github tag that gets updated automativally every time the repository recieves a new change. It has two links you care about: client and server. **Use this server zip if you're not playing in singleplayer; don't try to patch 1.2.1 server files to be compatible with 1.2.2** (disturbingly many people have attempted to).

The client zip can then be imported into a nice launcher like MultiMC. In MultiMC, you can do this by going Add Instance - Import from Zip and choosing the zip you downloaded. Note: you might want to include in the instance's name a reference to the specific state of the repo. This is why the snapshot zips include a weird string like `66833c` - that's the closest a github repo has to a version number.

The server zip, if you need it, is a full server, with Forge and start scripts included. Just unpack it somewhere and run using the script.

These actions are enough to install the dev version, but...

## Installing Fixes

...it still doesn't have those fixes that curseforge can't ship - ones that consist of custom jars. So you might still want to install some of the unofficial fixes available, just like in [the 1.2.1 case ](InstallingUnofficialFixes.md).



## Transferring the world over

If you don't wish to start a new world with 1.2.2, you don't have to. You can just transfer your world to the new instance. To do that, navigate to your old instance's `minecraft` folder, then in the `saves` folder find a folder named after your world. Copy *that* entire folder to the `saves` folder of the new instance.

You'll also likely want to copy over the entire `journeymap` folder (in `minecraft`)(your waypoints), as well as `options.txt` (all the options you've tweaked, so that you don't have to ~~set GUI scale to Large once again-~~ configure them again).
