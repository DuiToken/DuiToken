# DúiToken Contract

All logic for $DUI is built within the genesis smart contract ```DuiToken.sol``` the only external interaction with is the PancakeSwap V2 Router / LP.

The TechRate Audit details can be found [in the repo here](https://github.com/DuiToken/DuiToken/tree/master/audit).

- At this point it seems like there was an issue with deploying part of the ```swapAndLiquify``` function when the token contract was spun up, could also be something to do with DXSale - I have come across this issue once during testing prior to launch, the contract was tested with LP in Pancakeswap multiple times, and all functions worked correctly. We also created another identical deployment with a different name which ran without issue, following the launch.
The functioning identical copy/test token can be found [here](https://bscscan.com/token/0x1fcc1d84601ba90c1b86170c25246eb74db448dc), created by the $DUI owner wallet.
~ noted 18/5/21
- Re: the above issue - We are working on possible solutions for the ```swapAndLiquify``` function, however if unable to resolve - it will instead be turned into a positive for the project, this does not affect the long term plans for $DUI at all. If this is the case, it means the token no longer will have a Liquidity Pool+Holder Reward tax, and is able to become purely a Holder Reward token. The final holder reward % would be brought to a community vote. The team also have other solutions for the LP outside of ```swapAndLiquify``` which would be announced.
~ noted 19/5/21

## Licence

The contents of this repo are licensed under Apache-2.0. See [LICENCE](https://github.com/DuiToken/DuiToken/blob/master/LICENSE).

----- 

© 2021 [DúiToken](https://DuiCrypto.com)
