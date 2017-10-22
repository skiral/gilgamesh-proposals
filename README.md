# Gilgamesh Platform Proposals

Gilgamesh token holders can vote and suggest new features to be built on the Gilgamesh Platform.
Voters can propose a new suggestion by creating an issue on github.

Gilgamesh Voting dApp is based on [CarbonVote](http://carbonvote.com/) implementation and also inspired by [District0x](https://district0x.io).

Voting on more critical decisions such as the economics of the platform won't be supported by the current implementaiton and will implemented after the Aragon Core is launched on the Mainnet, 

## How to Vote and Unvote

In order to vote on future proposals go to our [Voting dApp](https://vote.gilgameshplatform.com/) and follow the instructions.

## How to submit a Proposal

Currently, we are accepting Proposals only for the [Shakespeare release](https://www.gilgameshplatform.com/roadmap), which is the second release on our IOS app.

Adhere the following guidelines to get an 'Accepted Proposal'
1. The proposal must be submitted as an [issue](https://github.com/skiral/gilgamesh-proposals/issues/new) in the skiral/gilgamesh-proposals repository.
2. The proposal aligns with [Gilgamesh Proposal Standard template](#gilgamesh-proposal-standard)

## Gilgamesh Proposal Standard
The Gilgamesh Proposal Standard is a template for proposals to ensure that submissions follow best practices and contain sufficient amount of information, All proposals should be structured as follows:

**Name:** Include the name of the proposed feature, ideally, it should be in the title section.

**Purpose:** Why is this feature needed? what's the problem that is going to solve? one or two paragraph explanation is sufficient.

**Description:** Describe how the feature needs to be implemented, and what are the impacted experiences and screens. include sketches or mocks.

## Proposal Incentives
To incentiveze, the submission of high quality and thoughtful Gilgamesh proposals, the following rewards will be issued:
300,000 GIL = Proposal is accepted and has received the most votes on a voting cycle.

Please make sure to include your ETH address at the end of your proposal.

Note: Proposal incentive reward amounts are subject to change any time.

## Proposal Labels
[Proposal Labels](https://github.com/skiral/gilgamesh-proposals/labels) are a great way to identify the nature of the proposal and simplify collaboration.

Note: If you believe that you proposal has been incorrectly labled, Please comment with the correct label or a newly suggested label that better describes your proposal. to expedite, you can always reach out to our community manager on Slack.

**List of proposal labels:**

* **Green 'Accepted' Label** Your proposal has followed the guidelines and has been accepted for voting.

* **Yellow 'Elaborate':** this label is used one a more content or description is required for the proposal to become accepted.

* **Red 'Rejected' Label** Your proposal has been flaged for one of the following reasons.
* 1- Spamming: if users create spam proposals and fail to adhere to the guidelines and refuse to follow the proposal standards, upon receiving the spam tag, your account will be blocked from interacting with Github repo. Continued abuse in any form will result in a report to GitHub staff to investigate the account(s).

* 2- Duplicate: it indicates that a similar proposal has been submited.
* 3- Invalid: Proposals that do not adhere to the Gilgamesh proposal standards outlined in this document. These proposals will be closed.

The labels and subject to change and we will notify everone in our [blog](https://blog.gilgameshplatform.com)


## How to vote from MyEtherWallet
1. Go to https://www.myetherwallet.com/#contracts 
2. Select Ropsten Test Network from the Network dropdown, located at top right corner of the screen
2. In the `Contract Address` field insert Gilgamesh vote smart contract address `0xf74A2C3C82653F20088B218cBe3101a7Afd21a53`
3. In the ABI / JSON Interface enter the following:
```
[{"constant":true,"inputs":[],"name":"endBlock","outputs":[{"name":"","type":"uint256"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":false,"inputs":[],"name":"unVote","outputs":[],"payable":false,"stateMutability":"nonpayable","type":"function"},{"constant":false,"inputs":[{"name":"proposalId","type":"int256"}],"name":"vote","outputs":[],"payable":false,"stateMutability":"nonpayable","type":"function"},{"constant":false,"inputs":[{"name":"_endBlock","type":"uint256"}],"name":"changeEndBlock","outputs":[],"payable":false,"stateMutability":"nonpayable","type":"function"},{"constant":true,"inputs":[{"name":"offset","type":"uint256"},{"name":"limit","type":"uint256"}],"name":"getVoters","outputs":[{"name":"_voters","type":"address[]"},{"name":"_proposalIds","type":"int256[]"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[],"name":"votersCount","outputs":[{"name":"","type":"uint256"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"}],"name":"votes","outputs":[{"name":"","type":"int256"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"}],"name":"voters","outputs":[{"name":"","type":"address"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[],"name":"admin","outputs":[{"name":"","type":"address"}],"payable":false,"stateMutability":"view","type":"function"},{"inputs":[{"name":"_endBlock","type":"uint256"}],"payable":false,"stateMutability":"nonpayable","type":"constructor"},{"anonymous":false,"inputs":[{"indexed":true,"name":"voter","type":"address"},{"indexed":true,"name":"proposalId","type":"int256"}],"name":"onVote","type":"event"},{"anonymous":false,"inputs":[{"indexed":true,"name":"voter","type":"address"},{"indexed":true,"name":"proposalId","type":"int256"}],"name":"onUnVote","type":"event"}]
```
4. Press `Access`
5. Select function -> `vote`
6. In the `proposalId` field put the number of your selection, which is shown as the `ID:` on the voting interface or github issue ID.
7. Send and sign the transaction.
**Don't send any ETH, GIL or any ERC20 token**

## How to un vote from MyEtherWallet
1. follow step 1 to 4 from previous section
2. Select function -> `unVote`
3. Send and sign the transaction.
**Don't send any ETH, GIL or any ERC20 token**

Inspired by [District0x](https://district0x.io)
