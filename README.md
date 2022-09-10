# delta-neutral-mlp-vault
A prototype of a trading vault strategy that benefits from the MLP index APY while attempting to be delta neutral to the composite tokens 

Ideas how to build/integrate this: 
-play with the % of the standard mlp index
-look into combining or allocating a % of the tokens into liquidity minning of whatever token(s) are currently trading at a discount to a 200MA BB
-look into offering variable MLP indexes, historic price/weight ratios, side pools?

https://swaps.docs.mycelium.xyz/perpetual-swaps/mycelium-perpetual-swaps
https://swaps.docs.mycelium.xyz/developer-resources/contract-addresses
https://github.com/mycelium-ethereum
https://github.com/mycelium-ethereum/pools-client

Consider This: (

from Discord, #pools-general, https://discord.com/channels/808906099172442122/887464543058534432/1017779849420603462

@SUBGURU
One last question... do my tokens gain valuation IMMEDIATELY with the entry of the new money into the short side of the pool OR only with the upside movement from the moment of the entry point? Does just the entry of the new money cause the increased valuation of my tokens since there is more capital on the short side of the pool?

iguanarchist — Today at 5:53 AM
New money entering the pool isn't a gain/loss event. How a position performs is primarily based on oracles. A new position's entry price is based on an average price of the next 8 hours after minting the position.
The only way new money entering a pool can affect your position is by changing the skew - which may impact how much you gain.


from Discord, #🍄Gereneral, https://discord.com/channels/808906099172442122/1016195655665979472/1017948464216297534
🍄_vcBacked_Bob_Boyle_🍄 — Today at 5:09 PM
It’s a different kind of leverage product, the pools are based on a process where collateral is transferred back and forth between the long and short side, depending on the collateral proportions in the pool there is also a skew to the leverage that will cause it to stray higher or lower than the 10x when this happens it is called the effective leverage. Because your position can never go to zero, you can not be liquidated, though you can effectively diminish your position to near zero.

The swaps pool 10x position is a leveraged position taken against the assets in the MLP pool, if you hit a liquidation price you will lose your deposited collateral
