# Gilgamesh Platform Proposals

The Gilgamesh platform allows Gilgamesh token (“GIL”)  holders vote on new features.  These votes will be tied to specific proposals, which for now will take the form of new suggestions on github.

This document explains why and how Gilgamesh’s Voting dApp will be used to democratically govern future updates to the platform.

## Mission

It is Gilgamesh’s mission to create a secure and engaging knowledge sharing social platform that helps readers connect socially with other readers and authors in a fun and interactive way.  Because users are the driving force behind this social platform, we believe that they should determine how the platform can be governed.  This democratic governance ensures that users needs are met and the platform will continue to be useful as a knowledge-generating platform.

## Basic Functionality

The Gilgamesh Voting DApp allows GIL token holders to propose and vote on new features.  The DApp uses smart contracts on the Ethereum network to execute votes in a model that is similar to processes developed by [CarbonVote](http://carbonvote.com/)  and [District0x](https://district0x.io).

While the Gilgamesh platform will eventually be controlled entirely by its users, voting on critical decisions such as governance, economics, and major protocols are not available in the current build.  This level of user control will be implemented after the [Aragon Core](https://aragon.one/core/) is launched on the Mainnet.


## Submitting a Proposal

Gilgamesh is currently accepting proposals for the [Shakespeare release](https://www.gilgameshplatform.com/roadmap), the second release on our IOS app.  All proposals must be submitted as an [issue](https://github.com/skiral/gilgamesh-proposals/issues/new) in the `skiral/gilgamesh-proposals` repository on github.  Proposals are reviewed and accepted by moderators before they are released to the community for voting, and they must adhere to the Gilgamesh Proposal Standard, described below.  


## Gilgamesh Proposal Standard

In order to be accepted by moderators, all proposals must follow the Gilgamesh Proposal Standard.  This template ensures that submissions are organized in a manner that conveys complete information about the proposal.  All proposals must be structured as follows:

**Name:** Include the name of the proposed feature in both the first line of text and the title of the issue in the repository.

**Purpose:** Explain in one or two paragraphs why the proposed feature is necessary and useful to Gilgamesh users.  Be sure to address the interface and functionality of the feature, as well as what problem it is designed to solve.

**Description:** Describe how the feature will be integrated into the existing user interface, including the change in user experience and look of the platform.  Include sketches or mocks that provide a visual of the proposed feature.

**ETH address:** Because winning proposals receive a GIL reward, please make sure to include your ETH address at the end of your proposal.

## Proposal Review and Approval

Gilgamesh moderators will review all proposals submitted through github, assess them for compliance with the Gilgamesh Proposal Standard, and review their content for accuracy and appropriateness.  After review, proposals will be labeled as follows:

**Green ("Accepted"):** The proposal followed all requirements and has been accepted for voting.

**Yellow ("Elaborate"):** The proposal requires more content or some degree of revision to adhere to the Gilgamesh Proposal Standard. 

**Red ("Rejected"):** Your proposal has been flagged for one or more of the following reasons:

1. **Spamming:** Spam proposals will be rejected, and users who create spam proposals will be blocked from interacting with Github repo. Continued abuse in any form will be reported to GitHub for further action.
2. **Duplicate:** An identical or substantially similar proposal has already been submitted.
3. **Invalid:** Proposals that do not adhere to the Gilgamesh Proposal Standards will be closed without further consideration.

Proposal Labels can be previewed [here](https://github.com/skiral/gilgamesh-proposals/labels).  If you believe your proposal has been labeled incorrectly, please leave a comment explaining your grievance. To expedite, you can always reach out to our community manager on [Slack](https://slack.gilgameshplatform.com).

Proposal review and approval policies are subject to change, in which case we will notify everyone though our [blog](https://blog.gilgameshplatform.com). 

## Voting and Unvoting
GIL token holders and the community of Gilgamesh users can vote on approved submissions using one of two methods:

1. **Vote using [MetaMask](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=en) chrome extension developed by [metamask.io](https://metamask.io/).**
Install the extension and enable the MetaMask on ROPSTEN Network in your browser. Fund your MetaMask with GIL Tokens (if you need GIL tokens fill out the following [Form](https://goo.gl/A7GsQC) and we will send you some). Click “Vote” on the proposal you want to vote for, and confirm the transaction via MetaMask.

2. **Vote using MyEtherWallet**
Go to https://www.myetherwallet.com/#contracts and select **"Ropsten Test Network"** from the **"Network"** dropdown located at top right corner of the screen.

In the **"Contract Address"** field insert Gilgamesh vote smart contract address: `0xf74A2C3C82653F20088B218cBe3101a7Afd21a53`

And enter the following in In the ABI / JSON Interface
```
[{"constant":true,"inputs":[],"name":"endBlock","outputs":[{"name":"","type":"uint256"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":false,"inputs":[],"name":"unVote","outputs":[],"payable":false,"stateMutability":"nonpayable","type":"function"},{"constant":false,"inputs":[{"name":"proposalId","type":"int256"}],"name":"vote","outputs":[],"payable":false,"stateMutability":"nonpayable","type":"function"},{"constant":false,"inputs":[{"name":"_endBlock","type":"uint256"}],"name":"changeEndBlock","outputs":[],"payable":false,"stateMutability":"nonpayable","type":"function"},{"constant":true,"inputs":[{"name":"offset","type":"uint256"},{"name":"limit","type":"uint256"}],"name":"getVoters","outputs":[{"name":"_voters","type":"address[]"},{"name":"_proposalIds","type":"int256[]"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[],"name":"votersCount","outputs":[{"name":"","type":"uint256"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"}],"name":"votes","outputs":[{"name":"","type":"int256"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"}],"name":"voters","outputs":[{"name":"","type":"address"}],"payable":false,"stateMutability":"view","type":"function"},{"constant":true,"inputs":[],"name":"admin","outputs":[{"name":"","type":"address"}],"payable":false,"stateMutability":"view","type":"function"},{"inputs":[{"name":"_endBlock","type":"uint256"}],"payable":false,"stateMutability":"nonpayable","type":"constructor"},{"anonymous":false,"inputs":[{"indexed":true,"name":"voter","type":"address"},{"indexed":true,"name":"proposalId","type":"int256"}],"name":"onVote","type":"event"},{"anonymous":false,"inputs":[{"indexed":true,"name":"voter","type":"address"},{"indexed":true,"name":"proposalId","type":"int256"}],"name":"onUnVote","type":"event"}]
```
Press `Access` then select function `vote` or `unvote.` Insert the number from the GitHub issue ID of the selected proposal in the `proposalId` field. Send and sign the transaction. **Do NOT send any ETH, GIL or any ERC20 token.**

## Proposal Incentives

To incentivize the submission of high quality and thoughtful proposals, Gilgamesh will issue **300,000 GIL** for the proposal that receives the most votes in a single voting cycle.

Proposal incentive reward amounts are subject to change any time.  Any change to the proposal incentive reward amounts will be announced in our [blog](https://blog.gilgameshplatform.com).  

Inspired by [District0x](https://district0x.io)
