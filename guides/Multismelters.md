# How Multismelter works

Multismelter is a GTCE multiblock machine that acts like a furnace (regular one, not an EBF!).

The "base" recipe for multismelter operation has a duration of 512 ticks (25.6s) and EU/t of `4 * heatingCoilLevel / heatingCoilDiscount`. It does not depend on the number of items it is processing this cycle. It can smelt up to `16*heatingCoilLevel` items at a time, even if they are of different types.
This recipe is then [overclocked](Overclocking.md) like other GTCE machines to obtain the true duration and drain.

For example, a Cupronickel-coiled (level 1,discount level 1) multismelter with an LV energy hatch will be overclocked once (4->16EU/t), for a duration of 256 ticks(12.8s). It will smelt 16 items at a time, for (assuming complete batches) a total of 16 ticks and 256 EU per item.

Another example: a HV Nichrome-coiled (level 4, discount level 1) multismelter will have a base EU/t of 16, which will be overclocked twice, resulting in a duration of 128 ticks(6.4s) and a EU/t of 256. It can smelt up to 64 items at a time, for a total of 2 ticks and 512 EU per item.

Because of GTCE's **overclocking** logic, this leads to a **strange result**: using coils with energy discount may sometimes make the smelter run much slower *and* not reduce energy usage all that much.

For instance, HV Tungstensteel MS takes 66 ticks to smelt and uses 33792 EU to do that. An HV HSS-G one takes 128 ticks and uses 32768 EU. At higher tiers, the disparity becomes much more pronounced.

As such, one might want to upgrade the coils until tungstensteel, then wait until they can acquire Naquadah Alloy coils, which are the best speed-wise.

**Multismelter coil comparison spreadsheet:**
![coil comparison](files/Multismelters/Coil%20Comparison.PNG)

**Warning**: in the current GTCE version, multismelters that run with a semi-full output may delete results that don't fit into it. Make sure the products are extracted!
