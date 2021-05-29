- - - -
#### [<img src="https://raw.githubusercontent.com/DuiToken/DuiToken/master/assets/Dui-icon.png" width="12" height="12" /> Root](https://github.com/DuiToken/DuiToken) | [Assets](https://github.com/DuiToken/DuiToken/tree/master/assets) | [Audit](https://github.com/DuiToken/DuiToken/tree/master/audit) | [```Contract & Dev Notes```](https://github.com/DuiToken/DuiToken/tree/master/contract) | [LP Wallet log](https://github.com/DuiToken/DuiToken/blob/master/contract/LP-Wallet-log.md)
- - - -

# DúiToken Contract & Related Notes

All logic for $DUI is built within the genesis smart contract ```DuiToken.sol``` the only external interaction with is the PancakeSwap V2 Router / LP.

The TechRate Audit details can be found [in the repo here](https://github.com/DuiToken/DuiToken/tree/master/audit).

## Triex Notes

- At this point it seems like there was an issue with deploying part of the ```swapAndLiquify``` function when the token contract was spun up, could also be something to do with DXSale - I have come across this issue once during testing prior to launch, the contract was tested with LP in Pancakeswap multiple times, and all functions worked correctly. We also created another identical deployment with a different name which ran without issue, following the launch.
The functioning identical copy/test token can be found [here](https://bscscan.com/token/0x1fcc1d84601ba90c1b86170c25246eb74db448dc), created by the $DUI owner wallet.
~ noted 18/5/21
- Re: the deployment issue - We are working on possible solutions for the ```swapAndLiquify``` function, however if unable to resolve - it will instead be turned into a positive for the project, this does not affect the long term plans for $DUI at all. If this is the case, it means the token no longer will have a Liquidity Pool+Holder Reward tax, and is able to become purely a Holder Reward token. The final holdhttps://bscscan.com/tx/0xbb685aa55be45f6e53dd331aefb3b9313c48dc0a561dc10e6270563a59525c8eer reward % would be brought to a community vote. The team also have other solutions for the LP outside of ```swapAndLiquify``` which would be announced.
~ noted 19/5/21
- There are some rumours and accusations of wrongdoing during our launch, I wanted to address a few concerns I've been approached about and seen mentioned in the community : I accidentally set the Tax Percent to 100% for a moment, instead of the MaxTx - this stopped trading same as the ```swapAndLiquify``` function, this happened during a panic moment when things were high pressure, I was trying every variable/parameter that could possibly be affecting things (sadly there was nothing in contract that could resolve it, so we went for just making it run) my Telegram/phone was getting flooded with hundreds of death threats, angry messages & calls throughout the entire process (damn, $DUI hyped hard for launch eh?). There was also an issue with my wallet having pending transactions, which took a minute or so. This was resolved immediately after. All of these issues were primarily caused by the ```swapAndLiquify``` function causing ALL transactions to break (regular send + pcs etc). I also want to note - my personal and professional identity is publicly linked to this project, and $DUI has long term goals, the team did not, and will not do anything to jeopordise trust in the project intentionally - in my view it makes no sense for a long term project to do something like that. > Let's turn the issue with the contract into a huge positive for holders instead!
~ noted 21/5/21
- $DUI will become/rebrand as a Holder Reward token, utilising the ```tokenFromDui``` and ```duitFromToken``` functions every TX distributes 3% instantly to all holders, proportionate to the amount they hold (final % to be set by community vote). We have solutions and the token distro you can read in the 'Team Token Distribution' section below. The LP wallet helps solve the lost liquidity tax, and allows to give more to holders instead. Noting roughly during process - to be adjusted as finalised. Max TX is currently set to 5% (will most likely be adjusted moving forward).
~ noted 22/5/21
- Adjusted Max TX to 1% to bring it in line with the initial plans for the token, and help mitigate whales.
~ noted 23/5/21
- Bought $DUI using a portion of the marketing fund via the owner wallet to pay for a partnership - [TXN](https://bscscan.com/tx/0xd8b6318b5e2cf2d8950ae33fa3427c4fab993ea333f2d99cca00b79e56188850)
~ noted 24/5/21
- Tax will be increased to 8% at 12:00pm UTC today, to explain the new solution we have come up with; 2.4346% out of the 8% tax (8%×2.4346=0.194768%) will go to each of the wallets mentioned below (as they are holders) to allow $DUI to continuously provide liquidity, donate to charity, keep up marketing etc. 
~ noted 25/5/21
- The team decided it’s best to give everyone 48 hours from the initial time before the 8% tax/holder reward goes live to ensure everyone has ample time to understand and digest the increase in tax + to give more time to utilise this as an opportunity to pull in new holders etc. 8% tax/reward change time - 05/27 12PM UTC 
~ noted 25/5/21
- Removed liquidity from $3X3 example/proof token to avoid people buying it unknowingly - [TXN](https://bscscan.com/tx/0xecdc7968f3920eedd2a3b4a36176f2e615ee08b808888866700666159c721d95)
~ noted 27/5/21
- $DUI Tax / Holder Reward raised from 3% to 8% @ 12:00 UTC - [TXN](https://bscscan.com/tx/0x318b933c6cca21077921b190ec9450aa1d7901cfa70436ebbce3091d848ce8b7)
~ noted 27/5/21
- Moved LP logs to their own file to tidy up the devnotes - [LP-Wallet-log.md](https://github.com/DuiToken/DuiToken/blob/master/contract/LP-Wallet-log.md)
~ noted 28/5/21

### Team Token Distribution

: LP Wallet : [0xdB0A4cFCddB3A666c2DB554B34A9e51D8A95F3D0](https://bscscan.com/token/0x8943b6d1677a4addbe5aa58f429e11e856746fba?a=0xdb0a4cfcddb3a666c2db554b34a9e51d8a95f3d0)
2.4346% Supply (still need to finalise smart contract to automate LP sending, otherwise will do this manually for the moment)

: Team Wallet : [0x52BD91dC11018ccf31e22F494A1A73BADBA3248f](https://bscscan.com/token/0x8943b6d1677a4addbe5aa58f429e11e856746fba?a=0x52BD91dC11018ccf31e22F494A1A73BADBA3248f)
2.4346% Supply (tokens locked via unicrypt for 3 months)
(Total is 73036520113.5-0.35%(unicrypt fee)=72780892293.1 tokens, locked for 3 months - you can see the tokens in the contract [here](https://bscscan.com/token/0x8943b6d1677a4addbe5aa58f429e11e856746fba?a=0xeaed594b5926a7d5fbbc61985390baaf936a6b8d) or in the [$DUI holders](https://bscscan.com/token/0x8943b6d1677a4addbe5aa58f429e11e856746fba#balances))

: Marketing Wallet : [0x4632156900191A274B8e14B590E85d7cbB7A8b24](https://bscscan.com/token/0x8943b6d1677a4addbe5aa58f429e11e856746fba?a=0x4632156900191a274b8e14b590e85d7cbb7a8b24)
2.4346% Supply 

: Charity Wallet : [0x426df8730370220B4Ca07D8C2cC8549bcBc4D26f](https://bscscan.com/token/0x8943b6d1677a4addbe5aa58f429e11e856746fba?a=0x426df8730370220B4Ca07D8C2cC8549bcBc4D26f)
2.4346% Supply 

- LP Wallet excluded from fee - [TXN: 0x423899780ef66280feea0a25a97d07139509cecc170f09d937f5a290972e9646](https://bscscan.com/tx/0x423899780ef66280feea0a25a97d07139509cecc170f09d937f5a290972e9646)
- Team Wallet excluded from fee - [TXN: 0x3130167960c9a47c0f8d4cc62353205d707f6973337ab222c17b658361e09b25](https://bscscan.com/tx/0x3130167960c9a47c0f8d4cc62353205d707f6973337ab222c17b658361e09b25)
- Team Wallet excluded from reward - [TXN: 0xc0225bcfacac33193ef6163fbddaea8bac6f58f3429030fd55eceef223d63683](https://bscscan.com/tx/0xc0225bcfacac33193ef6163fbddaea8bac6f58f3429030fd55eceef223d63683) (will undo in 3mo when unlocking tokens if we are going to remove them to the wallet at that time)
- Marketing Wallet excluded from fee - [TXN: 0xd5598555588b37bf24452aceecfe87e4a5fbcbf7726e7d3bd7c87e6f2b59a3be](https://bscscan.com/tx/0xd5598555588b37bf24452aceecfe87e4a5fbcbf7726e7d3bd7c87e6f2b59a3be)
- Charity Wallet excluded from fee - [TXN: 0x807b122000082cb939f7e36fad1729afba2e5fed757e50e7a3b12164da25a1ef](https://bscscan.com/tx/0x807b122000082cb939f7e36fad1729afba2e5fed757e50e7a3b12164da25a1ef)
- Unicrypt Locking/Vesting contract excluded from fee - [TXN: 0xa06718ae04a3229de7ebbdea1ac4d073ec84f2724ba65ea04564519abb2ce2b3](https://bscscan.com/tx/0xa06718ae04a3229de7ebbdea1ac4d073ec84f2724ba65ea04564519abb2ce2b3)
- Team Wallet Tokens locked in Unicrypt - [TXN: 0x9bb6fa5c0e436ebc73e399dcd6257d8b78288114db0a27f11ace6cf33022cdf6](https://bscscan.com/tx/0x9bb6fa5c0e436ebc73e399dcd6257d8b78288114db0a27f11ace6cf33022cdf6)

LP, Team, Marketing, Charity sent. Team funds locked until 22 August 2021. Need smart contract for LP wallet.

- 73036520113.5 $DUI [sent to LP Wallet](https://bscscan.com/tx/0xbc42234d56ad38ea4e90f685c9cc2523b90ee4276db9060034edd7a8927cf41d)
- 73036520113.5 $DUI [sent to Team Wallet](https://bscscan.com/tx/0x90c5ce372014afcf1cd2a6eaffa1912b5c93a2f89f74dc16a067a4d5ffade8f3)
- 73036520113.5 $DUI [sent to Marketing Wallet](https://bscscan.com/tx/0xa58d20d475bc4d23068190166b6e59ae76daea5431ed6713b0a50673fe08bff4)
- 73037115594.989 $DUI [sent to Charity Wallet](https://bscscan.com/tx/0x739f68dd2a3d92c53e82a4b65fc3922f8741411c4eedcb9776d1b15234fb3186)

In the [Token Contract](https://bscscan.com/token/0x8943b6d1677a4addbe5aa58f429e11e856746fba?a=0x8943b6d1677a4addbe5aa58f429e11e856746fba) there is 243,687,627,873.814151461 $DUI, or approx 8.1% of the supply stuck/burned from an issue during launch. We do not have any function in the contract that allows us to withdraw BEP20 tokens, only stuck BNB - because this has never occurred during testing. This allows us to start off with a lower supply then initially anticipated. We have also asked TechRate, and others to look into and confirm this, we intend to have a secondary audit + release a breakdown around the ```swapAndLiquify``` issue. (Was advised by TechRate that a secondary audit is unnecessary, as the token contract is straightforward & has no issue.)

There is also a progressive burn - we sent 90,000,000,000 $DUI (3%/supply) to the BSC universal burning wallet ```0x0000000000000000000000000000000000000001``` - you can see this growing [here](https://bscscan.com/token/0x8943b6d1677a4addbe5aa58f429e11e856746fba?a=0x0000000000000000000000000000000000000001) . At time of this note it is at 94,639,177,187.849053671 $DUI . This causes $DUI to be more and more deflationary over time as we have no ability to mint new tokens .

You can find the Pancakeswap Liquidity Pool Locker [at DXsale here](https://dxsale.app/app/pages/dxlockview?id=1454&add=0&type=lpdefi&chain=BSC). After 21/11/2021, we will decide what is best moving forward - whether to relock all. This will depend on project growth, and future potential listings etc. (Likely burn 50% of LP tokens when they unlock regardless)

### LP Log

Currently the LP wallet transactions are being done manually until the automation is implemented. You can find the dev TX logs at the below link.

[Manual LP transaction logs can be viewed in the LP-Wallet-log.md](https://github.com/DuiToken/DuiToken/blob/master/contract/LP-Wallet-log.md)

## Licence

The contents of this repo are licensed under Apache-2.0. See [LICENCE](https://github.com/DuiToken/DuiToken/blob/master/LICENSE).

----- 

© 2021 [DúiToken](https://DuiCrypto.com)
