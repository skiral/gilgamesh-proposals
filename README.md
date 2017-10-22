# Gilgamesh Platform Proposals

## How to vote from MyEtherWallet
1. Go to https://www.myetherwallet.com/#contracts 
2. Select Ropsten Test Network from the Network dropdown, located at top right corner of the screen
2. In the `Contract Address` field insert `0xf74A2C3C82653F20088B218cBe3101a7Afd21a53`
3. In the ABI / JSON Interface enter the following:
```
[{"constant":true,"inputs":[],"name":"endBlock","outputs":[{"name":"","type":"uint256"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":false,"inputs":[],"name":"unVote","outputs":[],"payable":false,"stateMutability":"nonpayable","type":"function"},{"constant":false,"inputs":[{"name":"proposalId","type":"int256"}],"name":"vote","outputs":[],"payable":false,"stateMutability":"nonpayable","type":"function"},{"constant":false,"inputs":[{"name":"_endBlock","type":"uint256"}],"name":"changeEndBlock","outputs":[],"payable":false,"stateMutability":"nonpayable","type":"function"},{"constant":true,"inputs":[{"name":"offset","type":"uint256"},{"name":"limit","type":"uint256"}],"name":"getVoters","outputs":[{"name":"_voters","type":"address[]"},{"name":"_proposalIds","type":"int256[]"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[],"name":"votersCount","outputs":[{"name":"","type":"uint256"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"}],"name":"votes","outputs":[{"name":"","type":"int256"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"}],"name":"voters","outputs":[{"name":"","type":"address"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[],"name":"admin","outputs":[{"name":"","type":"address"}],"payable":false,"stateMutability":"view","type":"function"},{"inputs":[{"name":"_endBlock","type":"uint256"}],"payable":false,"stateMutability":"nonpayable","type":"constructor"},{"anonymous":false,"inputs":[{"indexed":true,"name":"voter","type":"address"},{"indexed":true,"name":"proposalId","type":"int256"}],"name":"onVote","type":"event"},{"anonymous":false,"inputs":[{"indexed":true,"name":"voter","type":"address"},{"indexed":true,"name":"proposalId","type":"int256"}],"name":"onUnVote","type":"event"}]
```
4. Press `Access`
5. Select function -> `vote`
6. In the `proposalId` field put the number of your selection, which is shown as the `ID:` on the voting interface
7. Send and sign the transaction.
**Don't send any ETH,GIL or any ERC20 token**

## How to un vote from MyEtherWallet
1. follow step 1 to 4 from previous section
2. Select function -> `unVote`
3. Send and sign the transaction.
**Don't send any ETH,GIL or any ERC20 token**

Inspired by [District0x](https://district0x.io)
