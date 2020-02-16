# Why can't I start an AE craft?

`Why can't I start an AE craft? I have all the items and the Start button is active, but nothing happens when I click it.`

It's usually caused by reserved items being stolen by automation in the period between the end of crafting tree calculation and you clicking the button. You can avoid that by holding Shift when clicking the Next button in the quantity selection screen - this will skip the crafting screen, starting the craft immediately on the end of calculation. Note that you may have to hold Shift during the entire calculation process for it to be registered properly.

**Another possible cause** is AE system incorrectly estimating what resources it has due to use of compacting drawers. They report all item forms at once, so if a drawer has 9000 redstone, it will report both it and 1000 redstone blocks. If a craft requests 700 blocks and 6000 more redstone, it will seem possible to AE at first glance, but will fail to start.