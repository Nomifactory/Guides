Made for Nomifactory **1.2.2**. **Don't** try to apply it to later or earlier versions!

# Installing Unofficial Fixes for Nomifactory 1.2.2

## Introduction

This guide covers the installation of most unofficial fixes for the 1.2.2 version of Nomifactory. Mainly, these are the custom jars by Exa that would have been included in the pack proper if Curseforge allowed it.

## Steps

This guides assumes you already have 1.2.2 Nomifactory installed. [Link](https://www.curseforge.com/minecraft/modpacks/nomifactory/files/all), select topmost(latest) file.

### Exa's fixes
Originally a zip of fixes for 1.2.1, most of it has been integrated into the pack, except for the [GTCE](files/UnofficialFixes/jars/gregtech-1.12.2-1.8.4.419exa2.jar) and [Shadows of Greg](files/UnofficialFixes/jars/Shadows_of_Greg-1.12.2-2.8.0_fix.jar) jars (push the Download button). They are backports of GTCE/SoG fixes on Nomi's version of GTCE. No, you **don't** need the rest of the Exa's fixes (scripts, etc) - they are integrated into 1.2.2, only the jars aren't. To install, just replace with them the similarly-named `gregtech` and `Shadows_of_Greg` jars in the `mods` folder of your instance.

#### Sources
Links to the repos for Exa's forks, to be compliant with \*GPL licenses: [GTCE](https://github.com/Exaxxion/GregTech/), [SoG](https://github.com/Exaxxion/Shadows-of-Greg/). **You probably don't need these links - use the ones in the previous paragraph.**

### Third-party fixes
This section is for the *really* unofficial stuff, made by fans of Nomifactory for fans of Nomifactory.
#### Talchas's AE2 fix
A relatively minor change in AE2 logic, optimizing it to not recalculate the entire network if anything changes when AE2 is in channelless mode. [The PR for it to be included into AE2 proper](https://github.com/AppliedEnergistics/Applied-Energistics-2/pull/4220) was rejected, but there have yet to be any known problems from using it. Advantage: *massive* improvement in recalculation times for big channelless AE2 networks. This doesn't affect lag from working, only the freezes when you change something in the network's structure.

All the builds of Talchas's fixes are on [the repo](https://github.com/talchas/Applied-Energistics-2/releases), but for 1.2.2 specifically **you want the `rv6-stable-7` build**, **not** the `rv6-stable-6` one - they are for different AE2 versions, since in 1.2.2 AE2 was updated to `stable-7`. **Here's a** [direct link to the release you need for 1.2.2](https://github.com/talchas/Applied-Energistics-2/releases/tag/rv6.stable.7-talchas-b).  Replace your AE2 jar with it, just like with Exa's GTCE and SoG jars. Bonus: see how there are two jars in each release? If you're a server owner, you can download the jar that is named the same as the normal AE2 jar, and if you replace AE2 with it on your server, you won't need to make all your players install the fix to be able to connect - it's serverside-only.

#### PrototypeTrousers's AE2 fixes
**NOTE:** As of 2021-03-31, the dev snapshots include [Applied Energistics 2 Trousers Edition](https://github.com/PrototypeTrousers/Applied-Energistics-2) by default, replacing Applied Energistics 2 and Just Enough Energistics. It's no longer necessary to install it manually.

Continuing where Talchas left off, [PrototypeTrousers's fork of AE2](https://github.com/PrototypeTrousers/Applied-Energistics-2/releases) is a much more extensive set of bugfixes and enhancements to improve the experience of using AE2 in Nomifactory. If you use this version of AE2, **you need it on both the server and client** and you should also delete your Just Enough Energistics jar from your mods folder.
