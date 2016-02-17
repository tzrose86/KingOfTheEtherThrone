# King of the Ether Throne

An Ethereum ÐApp (a "contract"), living on the blockchain, that will make you a King or Queen, might grant you riches, and will immortalize your name.

<a name="Important"/>
## Important Notice

A SERIOUS ISSUE has been identified that can cause monarch compensation payments to not be sent.

DO NOT send payments to the contract previously referenced on this page, or attempt to claim the throne. Refunds will CERTAINLY NOT be made for any payments made after this issue was identified on 2016-02-07.

This issue involves a somewhat surprising interation between contract-to-contract calls, low gas, and/or some wallet contracts, and is particularly likely to occur if one monarch claimed the throne using a contract-based wallet, and then the next monarch included only a small amount of gas with their payment. See this [reddit thread](https://www.reddit.com/r/ethereum/comments/44h1m1/a_new_%C3%B0app_king_of_the_ether_throne/) for details as they emerge. However, the issue may also occur in other situations.

Investigation is continuing to understand which payments succeeded and which failed. This is hindered by most blockchain explorers not showing or indexing all contract-to-contract calls (aka "internal transactions" or "message calls") - suggestions appreciated. A further update will be posted here by 2016-02-21 at the latest.

Following the investigation, a new Kingdom of the Ether is expected to arise (possibly with a twist) - and don't worry, those brave, noble (and maybe a little foolhardy) monarchs who entered the Hall of Monarchs during this turbulent Early Age of Kings will not be forgotten - may their names be remembered evermore.

Thank you for your patience and understanding.

## Contents

- [What does it do?](#WhatItDo)
- [Who is the Monarch?](#WhoMonarch)
- [Hall of Monarchs](#GreatHall)
- [How Can I Rule the Ether?](#HowIRule)
  - [with a ÐApp browser](#PayDappBrowser)
  - [manual payment](#PayManually)
  - [via Javascript console](#PayWithJavascript)
  - [by adding the contract](#PayAddContract)
  - [using chain explorers](#InteractChainExplorers)
- [Contract Details](#TheContract)
- [Other Bits and Pieces](#BitsAndBobs)
- [Disclaimer](#Disclaimer)

<a name="WhatItDo"/>
## What does it do?

The Ether Throne awaits you. It can be yours for a price - here are the rules as enforced by the contract:

- Let's say (for example) the current claim price for the throne is 10 ether.
- You like the sound of being King, so you send 10 ether to the contract.
- This makes you the new King of the Ether Throne, the First of His Name, the Uncentralized, Sovereign of the Exalted Order of Miners, Emperor of the Blocks beyond the Sidechains, Head of the Great Patricia Tree, and so on.
- Your name will be added to the [Hall of Monarchs](#GreatHall) in the blockchain.
- The contract will then send your 10 ether (less a small commission) to the previous Monarch you have usurped, as compensation.
- The new claim price for the throne will go up by 50%, to 15 ether.
- If an usurper comes along who is willing to pay 15 ether, she will depose you and become Queen, and you will receive her payment of 15 ether as compensation - a profit of 5 ether for you.
- Of course, if no usurper comes along, you will never get your 10 ether back - but what is that compared to ruling the ether forever?

<a name="WhoMonarch"/>
## Who is the Monarch?

Since 2016-02-07T20:22:06.000Z, the illustrious current ruler of the Ether Throne is **0xc0e22f23ff54ca58d93a65044a18a3f245552144**, the First of Their Name, the Uncentralized, the Sovereign of the Exalted Order of Miners, the Emperor of the Blocks beyond the Sidechains, the Head of the Great Patricia Tree, who sits in the [Hall of Monarchs](#GreatHall).

*NB: You don't have to trust this page (which was last updated based on a block with timestamp 2016-02-17T11:19:52.000Z); read on for how you can interact with the contract via the Ethereum blockchain to find out who is our ruler - and usurp them.*

<a name="GreatHall"/>
## Hall of Monarchs

|Number|Name|Claim Price Paid|
|---|---|---|
|Current|0xc0e22f23ff54ca58d93a65044a18a3f245552144|96 ether|
|17|Vitty www.skaitmeta.lt (0xd585c0c36d09164ab3b54a1ddcc2a26bef055925)|64 ether|
|16|Major Tom (0x9dec4be08b93838697fba22c3cdd28c1a03ed159)|42.7 ether|
|15|0xcb4046e50f71409a3af23da0961b5ce2f769de31|28.5 ether|
|14|Firescar96 (0xf031f36717cb524b883d440e3837c138180a0289)|19 ether|
|13|0x60cea93e5d7b98027f7e7e433673f9b30448b001|12.7 ether|
|12|Sir Buterin (0x71e3c9097edd8cf3b3136cdc2eb69ce2cec80f02)|8.52 ether|
|11|Aakil Fernandes  (0xdc99b79555385ab2fe0ff28c3c954a07b28aac5e)|5.68 ether|
|10|dpfbop (0xfa8ede0792b8a4f0d5299d76730244ba76b4ab0b)|3.79 ether|
|9|Bokky Poo Bah (0x9dec4be08b93838697fba22c3cdd28c1a03ed159)|2.53 ether|
|8|Dunning\_Krugerrands (0xefede69c637ca59ae461094ab64c5bbe99843f34)|1.69 ether|
|7|moo ha ha says the laughing cow (0x1db3439a222c519ab44bb1144fc28167b4fa6ee6)|1.13 ether|
|6|Max von Sydow (0xa15cc3b84ab0fb5598778366d0281714fc878d8d)|0.757 ether|
|5|\_natsu\_ (0xfe159b1852a4450ba4bd9c2630dbea72c9b8cd65)|0.505 ether|
|4|king\_pengui2 (0x9371ea0d13fb8a8306a420572cda36c4e8640f38)|0.337 ether|
|3|SPACE\_CHICKEN (0xb2afec1da55c15ad57b3310f9008c47f4e028de3)|0.225 ether|
|2|king\_pengui (0x9371ea0d13fb8a8306a420572cda36c4e8640f38)|0.15 ether|
|1|kingoftheether.com (0xfe159b1852a4450ba4bd9c2630dbea72c9b8cd65)|0.1 ether|
||[Vacant]|0 ether|

<a name="HowIRule"/>
## How Can I Rule the Ether?

The power of the Ether Throne can be yours for the **current claim price** of just **144 ether** (as of 2016-02-17T11:19:52.000Z).

Here's how you can pay the claim price and rule the Ether ...

<a name="PayDappBrowser"/>
### Pay Using an Ethereum ÐApp Browser

It's all a bit hemorrhaging-edge, but if you visit the live version of this page at [kingoftheether.com](http://www.kingoftheether.com/) - not in your normal browser, but inside a special Ethereum ÐApp browser such as [Mist (developer preview)](https://github.com/ethereum/mist/releases/tag/0.3.6) then you should see the ÐApp interface appear where you can interact with the contract via your local Ethereum node.

Unfortunately Mist is still under heavy development (I keep getting 'invalid address' errors), so you might have more luck if you use your normal browser (Chrome, Firefox) with the Ethereum [geth](https://github.com/ethereum/go-ethereum/wiki/geth) client running locally. You'll need to enable RPC calls so the ÐApp in your browser can talk to it - e.g. start geth like this:
```
# NB: the DApp always uses the first account, so unlock it:
geth --rpc --rpccorsdomain 'http://www.kingoftheether.com' --unlock 0 console
```

**IMPORTANT**: A SERIOUS ISSUE has been identified with this ÐApp/contract that can cause LOSS OF FUNDS - DO NOT send payments or attempt to claim the throne. See the [Important Notice](#Important) at the top of the page.



If that doesn't work, don't worry, read on for more ways to claim your throne ...

<a name="PayManually"/>
### Pay by Sending a Manual Payment

You can simply manually send your payment to `TEMPORARILY REMOVED AS A PRECAUTION`. You could use a wallet app such as Mist, an online wallet, or with some Javascript in the geth console.

**IMPORTANT**: A SERIOUS ISSUE has been identified with this ÐApp/contract that can cause LOSS OF FUNDS - DO NOT send payments or attempt to claim the throne. See the [Important Notice](#Important) at the top of the page.

If another monarch comes along and takes your throne, we'll send your compensation payment to the address you sent your payment from - so make sure you send the payment from an address you control.

We'll use your Ethereum address as your name, though if you like you can put your name in the data field - might need to convert from ASCII. e.g. with the geth Javascript console:

```
eth.sendTransaction({
  from: eth.accounts[0],
  value: web3.toWei(15, 'ether'), // change this
  to: 'TEMPORARILY REMOVED AS A PRECAUTION',
  gas: 500000,
  data: web3.fromAscii('Your Kingly Name') // change this
});
```

Please keep the length of your name to no more than 20 characters - some ÐApp software gets confused by long names.

See above for the current claim price of the throne (don't worry too much about getting it wrong, it will refund you if you pay too little / too much).

<a name="PayWithJavascript"/>
### Using the Web3 Javascript API

If you're running a geth node, you can interact with the contract using a little Javascript like this:

```
// tell web3 how to talk to the contract
var kingOfTheEtherThroneContract = web3.eth.contract([{"constant":false,"inputs":[{"name":"amount","type":"uint256"}],"name":"sweepCommission","outputs":[],"type":"function"},{"constant":true,"inputs":[],"name":"currentClaimPrice","outputs":[{"name":"","type":"uint256"}],"type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"}],"name":"pastMonarchs","outputs":[{"name":"etherAddress","type":"address"},{"name":"name","type":"string"},{"name":"claimPrice","type":"uint256"},{"name":"coronationTimestamp","type":"uint256"}],"type":"function"},{"constant":false,"inputs":[{"name":"name","type":"string"}],"name":"claimThrone","outputs":[],"type":"function"},{"constant":true,"inputs":[],"name":"numberOfMonarchs","outputs":[{"name":"n","type":"uint256"}],"type":"function"},{"constant":true,"inputs":[],"name":"currentMonarch","outputs":[{"name":"etherAddress","type":"address"},{"name":"name","type":"string"},{"name":"claimPrice","type":"uint256"},{"name":"coronationTimestamp","type":"uint256"}],"type":"function"},{"constant":false,"inputs":[{"name":"newOwner","type":"address"}],"name":"transferOwnership","outputs":[],"type":"function"},{"inputs":[],"type":"constructor"},{"anonymous":false,"inputs":[{"indexed":false,"name":"usurperEtherAddress","type":"address"},{"indexed":false,"name":"usurperName","type":"string"},{"indexed":false,"name":"newClaimPrice","type":"uint256"}],"name":"ThroneClaimed","type":"event"}]);

// tell web3 where the contract is
var kingOfTheEtherThrone = kingOfTheEtherThroneContract.at('TEMPORARILY REMOVED AS A PRECAUTION');

// ask contract what the current claim price is
web3.fromWei(kingOfTheEtherThrone.currentClaimPrice(),'ether');

// claim the throne
kingOfTheEtherThrone.claimThrone(
  'Put Name Here',
  { from: eth.accounts[0],
    value: kingOfTheEtherThrone.currentClaimPrice(),
    gas: 500000 } )
```

**IMPORTANT**: A SERIOUS ISSUE has been identified with this ÐApp/contract that can cause LOSS OF FUNDS - DO NOT send payments or attempt to claim the throne. See the [Important Notice](#Important) at the top of the page.


<a name="PayAddContract"/>
### Pay by Adding the Contract in the Mist Wallet

If you're using the (still experimental!) Mist Ethereum Wallet - e.g. from [https://github.com/ethereum/mist/releases](https://github.com/ethereum/mist/releases) - go to Contracts -> Add Contract, then fill in the details from the [Contract Details](#TheContract) section below. Yes, you do need to copy and paste that big long bit of JSON.

After you've added the Contract, if you click "Show Contract Information" (and perhaps click what appears underneath?), you should be able to see the Current Claim Price on the left and a 'claimThrone' function you can select and execute on the right. Don't forget to include the payment when executing the claimThrone function. The Current Claim Price is shown in Wei, so you might need to do a little conversion.

This worked (once) in version 0.3.8 of the wallet client on Windows, anyway. Unfortunately you might find in some versions that you cannot add a payment when executing a function - which isn't much good.

<a name="InteractChainExplorers"/>
### Interacting via Chain Explorers

You can watch transactions and storage changes happening in this contract on chain viewers at e.g. [etherchain.org](https://etherchain.org/account/0xb336a86e2feb1e87a328fcb7dd4d04de3df254d0), [etherscan.io](https://etherscan.io/address/0xb336a86e2feb1e87a328fcb7dd4d04de3df254d0), and [ethercamp](https://live.ether.camp/account/0xb336a86e2feb1e87a328fcb7dd4d04de3df254d0).

Some don't seem to be very good at showing transactions generated by the contract though. Ether.camp has the best visualisation but appears to be lagging behind a bit as of 7th Feb ...

<a name="TheContract"/>
## Contract Details

You can use these details to interact with the King of the Ether Throne contract:

#### CONTRACT NAME

`KingOfTheEtherThrone`

#### CONTRACT ADDRESS
`TEMPORARILY REMOVED AS A PRECAUTION`

#### JSON INTERFACE (CONTRACT ABI)

```
[{"constant":false,"inputs":[{"name":"amount","type":"uint256"}],"name":"sweepCommission","outputs":[],"type":"function"},{"constant":true,"inputs":[],"name":"currentClaimPrice","outputs":[{"name":"","type":"uint256"}],"type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"}],"name":"pastMonarchs","outputs":[{"name":"etherAddress","type":"address"},{"name":"name","type":"string"},{"name":"claimPrice","type":"uint256"},{"name":"coronationTimestamp","type":"uint256"}],"type":"function"},{"constant":false,"inputs":[{"name":"name","type":"string"}],"name":"claimThrone","outputs":[],"type":"function"},{"constant":true,"inputs":[],"name":"numberOfMonarchs","outputs":[{"name":"n","type":"uint256"}],"type":"function"},{"constant":true,"inputs":[],"name":"currentMonarch","outputs":[{"name":"etherAddress","type":"address"},{"name":"name","type":"string"},{"name":"claimPrice","type":"uint256"},{"name":"coronationTimestamp","type":"uint256"}],"type":"function"},{"constant":false,"inputs":[{"name":"newOwner","type":"address"}],"name":"transferOwnership","outputs":[],"type":"function"},{"inputs":[],"type":"constructor"},{"anonymous":false,"inputs":[{"indexed":false,"name":"usurperEtherAddress","type":"address"},{"indexed":false,"name":"usurperName","type":"string"},{"indexed":false,"name":"newClaimPrice","type":"uint256"}],"name":"ThroneClaimed","type":"event"}]
```

#### CONTRACT SOURCE CODE

The Solidarity source code for the contract lives at [KingOfTheEtherThrone.sol](https://github.com/kieranelby/KingOfTheEtherThrone/blob/v0.4.0/contracts/KingOfTheEtherThrone.sol). It was compiled with solidity version `0.2.1-fad2d4df` with optimization, just in case you want to verify the code matches the bytecode. **IMPORTANT**: A SERIOUS ISSUE has been identified with this contract that can cause LOSS OF FUNDS - DO NOT send payments or attempt to claim the throne using it. See the [Important Notice](#Important) at the top of the page. Avoid basing your own ÐApps/contracts on this source code until the issue is fully understood!



<a name="BitsAndBobs"/>
## Other Bits and Pieces

### How much is the commission charge?

One percent. This helps cover gas costs too.

### Haven't I seen something like this before?

Yes, probably - there are/were a number of Bitcoin chain games along similar lines (though they normally seemed to involve owning a magnificent gem or a special coin).

The difference with Ethereum is that you don't have to trust the author not to run away with the money - instead, you can inspect the contract and rely on the blockchain to ensure it is executed as written.

This contract was somewhat inspired by [ethereumpyramid.com](http://ethereumpyramid.com/) (to which this is in no way affiliated).

### I think something went wrong. Can I have my money back?

Long answer: Ah. Well, you see, one downside of trustless autonomous contracts executing on the blockchain is that there is no possibility of human intervention - no-one can reach into the back of the machine and tweak things, even if they wanted to. Besides, there is no money to give back - it's all been given to the previous monarch, remember? So you'll agree that refunds are impossible and unethical.

Short answer: No. See the Disclaimer below.

<a name="Disclaimer"/>
## Disclaimer

This is intended as a bit of fun and to explore what a contract running on the Ethereum blockchain can do. Please don't spend money you can't afford to lose - keep it fun.

If you suspect that spending crypto-currencies on virtual thrones for non-existent kingdoms is illegal in your jurisdiction, please avoid participating (and complain to your political representatives).

Please note that while the contract will live as long as the Ethereum blockchain, no warranty is given that this website will continue to exist or will continue to promote the contract or list your name.

Under no circumstances will refunds or compensation be paid even if the contract steals all your money and/or shoots your dog. The author disclaims all liability for the operation of the contract which should be considered its own autonomous legal entity - it is your responsiblity to study its likely behaviour before interacting with it, including taking into account that the actual behaviour of the compiled EVM bytecode in a real eth/geth note may differ from the assumed behaviour based on the solidity source code.

By interacting with the contract you agree to accept the conditions in this section as well as those listed at [ethereum.org/agreement](https://www.ethereum.org/agreement).
