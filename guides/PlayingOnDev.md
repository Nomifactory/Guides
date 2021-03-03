# Playing on Dev

This guide will teach you how to play on development snapshots following the release of 1.2.2.

For the previous version of this guide targeting dev snapshots leading into 1.2.2, use the [1.2.2 revision](https://github.com/OmnifactoryDevs/OmnifactoryGuides/blob/1.2.2/guides/InstallingUnofficialFixes.md).

## Preliminary Information

### What Are Development Snapshots?

Development snapshots are the bleeding-edge version of Omnifactory. We create a pair of client and server zip files automatically whenever we change the "dev" branch on our GitHub repository, keeping only the latest pair of files.

The main thing to note is that these are experimental builds. They have not been vetted to the same degree as releases. While we make a concerted effort to avoid breaking things, we don't make any guarantees.

If you do find a problem that hasn't been reported yet, please let us know on our issue tracker using the new issue template.

### Can You Update?

Dev snapshots, like releases, support safely upgrading from worlds at most as old as the previous official release. For example, you can safely update from 1.2.2 to the 1.3 dev snapshots, but not directly from 1.2.1.

If your world is older than the current release, please update to each subsequent release first, taking care of anything noted in the release notes before updating to the next version.

### Should You Update?

If you are interested in helping us find and fix bugs, or just simply seeing how things are going towards the next update, feel free.

If you want a stable gameplay experience, prefer the releases.

## Installation

Since we use an automatic build system, installation is nice and simple. Just download the zip called `Omnifactory-dev-<commit hash>-snapshot.zip` for client install and `Omnifactory-dev-<commit hash>-snapshot-server.zip` for the server. These are located [here](https://github.com/OmnifactoryDevs/Omnifactory/releases/tag/latest-dev-preview). This link always goes to the latest development snapshots.

### Version Numbering Scheme

You might be wondering what the versioning scheme for dev snapshots is. There is a seven-character section between `dev-` and `-snapshot` in the filename, which will also show up in the client's window title. This is the beginning of a longer number called a commit hash, which uniquely identifies a particular set of changes made to the pack.

It's not an incremental number like releases so it's somewhat unintuitive, but with just this number you can determine where you are in the commit history. The important thing is that the commit hash is identical between the server and client if you're playing on a dedicated server.

### Client Installation

Simply download the client zip and import it into your favorite launcher. We recommend [MultiMC](https://multimc.org), but any modern modded Minecraft launcher should do. The files will be downloaded and you can play it as usual.

#### Transferring Save Data

To keep important data from your prior client instance, copy the following files and folders:

File | Description
-----|------------
`minecraft/save` directory | Single Player worlds
`minecraft/resourcepacks` directory | Resource Packs
`minecraft/options.txt` | Minecraft settings like keybinds, selected resource packs, video options, etc.
`minecraft/journeymap` directory | Journeymap waypoints
`minecraft/config/jei/bookmarks.ini` | JEI Bookmarks

### Server Installation

If you want to run a dedicated server, then download the server zip and extract it into its own folder. You need a 64-bit Java Runtime Environment (JRE) installed to run the server, and it can be started using the file launch.bat (on Windows) or launch.sh (on Linux or other Unix-like systems).

Configure the amount of RAM you want to allocate to the heap by editing the startup script (there's instructions in the file). By default we set it to 2GB. Feel free to set it higher, but we don't recommend setting it above 4GB because the pack is unlikely to need more than that.

#### Transferring Save Data

Copy any customizations you want over into `server.properties`, and copy your save directory into the new server (by default called `world`).

### Installing Unofficial Fixes

We don't include any custom versions of pack mods in these zips.

As of 2020-12-05, the dev snapshots are using the latest versions of GregTechCE and Shadows of Greg. You should not use the custom jars for those mods anymore (it will break your pack).

For any other mods, refer to [Installing Unofficial Fixes](InstallingUnofficialFixes.md).
