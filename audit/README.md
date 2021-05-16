# DuiToken Audit

The inital audit completed by TechRate found a minor issue (The function ```includeInReward``` uses a loop to find and remove addresses from the ```_excluded``` list. We added a hard limit to mitigate for any possible gas error if excluding too many wallets). 

We resolved this prior to launch & have published the revised audit here.

## Licence

The contents of this repo are licensed under Apache-2.0. See [LICENCE](https://github.com/DuiToken/DuiToken/blob/master/LICENSE).

-----

© 2021 [DúiToken](https://DuiCrypto.com)
