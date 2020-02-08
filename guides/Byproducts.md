Valid for Omnifactory v.1.2.1

# How GTCE byproducts work
When a recipe has a % chance of one of the outputs when you mouse over it, it means it's a chanced byproduct. The actual chance of it depends on the tier of the machine you are doing this recipe in. The byproduct chance is always capped at 100%. Byproduct multiplying is unrelated to overclocking - all this still applies with overclocking disabled.
## Macerators
| Tier      | Chance(on 14% ore processing recipes) |
|-----------|---------------------------------------|
| LV        | 0%                                    |
| MV        | 14%(actual:4.62%)                     |
| HV        | 28%                                   |
| EV        | 56%                                   |
| IV and up | 100%                                  |

The byproduct chance is doubled for every tier above MV. IV, for example, have an x8 byproduct multiplier. **Also**: MV Macerators have only a single byproduct slot, despite most ore processing recipes having two byproducts. They contend for the slot, and **stone dust takes precedence**. As a result, the standard 14% byproduct chance with 67% stone dust becomes 0.33*0.14=**4.62%** in MV macerators. As such, it is recommended to **not set up a serious ore processing line until you can build HV Macerators** - those have a 28% byproduct chance on common recipes, six times that of MV.
## Other machines
The byproduct chance is multiplied by 2 for each tier the machine's voltage is higher than the recipe's.
For example, an MV centrifuge doing a 20 EU/t recipe would get a 2x byproduct multiplier.
