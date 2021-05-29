- - - -
#### [<img src="https://raw.githubusercontent.com/DuiToken/DuiToken/master/assets/Dui-icon.png" width="12" height="12" /> Root](https://github.com/DuiToken/DuiToken) | [Assets](https://github.com/DuiToken/DuiToken/tree/master/assets) | [```Audit```](https://github.com/DuiToken/DuiToken/tree/master/audit) | [Contract & Dev Notes](https://github.com/DuiToken/DuiToken/tree/master/contract) | [LP Wallet log](https://github.com/DuiToken/DuiToken/blob/master/contract/LP-Wallet-log.md)
- - - -

# DuiToken Audit

The inital audit completed by TechRate found a minor issue (The function ```includeInReward``` uses a loop to find and remove addresses from the ```_excluded``` list. We added a hard limit to mitigate for any possible gas error if excluding too many wallets - this was only a minor warning). 

We resolved this prior to launch & have published the revised audit here.

## Licence

The contents of this repo are licensed under Apache-2.0. See [LICENCE](https://github.com/DuiToken/DuiToken/blob/master/LICENSE).

-----

© 2021 [DúiToken](https://DuiCrypto.com)
