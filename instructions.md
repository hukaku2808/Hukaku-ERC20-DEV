How to do an ICO on Ethereum in less than 20 minutes.

Congratulations, you finally found it. This is exactly what you were looking for all over the internet.

This tutorial will give you everything you need to deploy an Initial Coin Offer aka ICO contract on Ethereum main net #nojokes.

After releasing the guide: How to issue your own ERC20 in less than 20 minutes we had some insane results:

Ranking 1st on Google, above TechCrunch and Ethereum itself for “How to issue a Token”. 🎉
20k people from different backgrounds went through the whole tutorial already. 🎉
113 Different Tokens Officially Issued so far.🎉
The crazy amount of requests and amazing feedback inspired me to write this one.

Being 100% open-source advocate, and working extremely hard to empower people with Blockchain that are TRULY accessible to everyone,

I believe this can empower thousands of people to build meaningful things.

Hopefully, it will inspire you to build the next big thing on cryptoland and NOT to be the next big fucking scam.

In this tutorial I will walk you through the steps of setting up your account through to issuing your ICO contract on Ethereum network using a single smart contract and MyEtherWallet.

The tokens will be standard ERC20, you will be able to setup general specifics like the rate of ETH per token and time-line bonuses.

WARNINGS — READ THIS SHIT. FOR REAL.
With great powers come great responsibilities. I’m not responsible for you not being cautious with your ETH, or using these powers for the evil side of force (for Vitalik’s sake, don’t do that). I truly hope you do good and feel empowered by the potential that this technology puts in the hands of people.
THIS CONTRACT HAS NOT BEEN AUDITED. It means that it is experimental code, has not been verified and can be broken, if you intend to do a REAL ICO, you HAVE to Audit the code and do a proper contract tailored to your specs.
I have absolutely no responsibility for you, your dog, your money, or your life. Be big boys and girls and own it.
Before we start:
There are a few different components you will need in order to build your own token.

Ethereum Address (Ropsten Network)
Some Ethereum (Ropsten Network)
A text editor (I.e. Sublime / Atom)
Solidity contract
Be able to cross your fingers twice during the process🤞🤞.
Ethereum address

For this tutorial we will use a test network to issue the token so you don’t end up spending real Ether’s. We will use the Ropsten Test network. In order to get started, go to MyEtherWallet (MEW) and create an account there.
To get setup, click the right hand side corner, change the network to Ropsten (MyEtherWallet) → click the New Wallet →Enter a password you can remember → Download / Save your Keystore file in a safe space → Save your Private Key in a safe space.
To view your wallet address, go to →View Wallet Info →Private Key → Enter the saved private key →Unlock your Wallet and it should be there!
Text Editor

Download one of the following text editors:

Sublime Text
Atom
Contract

Download the smart contract that the legendary Ethereum unicorn rider, BokkyPooBah has helped us to make, by clicking here. ⬅️
You will be editing this code for your own ICO Contract.
Ropsten Ethers [UPDATED]

We have created our own faucet where you can request Ropsten Ethereum! Just access https://faucet.bitfwd.xyz/ and put your ropsten address and our smart contract will send you some!

Transfer only once please! And if it doesn’t work let me know in the comments!

IMPORTANT [Before I forget to ask you!]

Make sure you follow me on Twitter for more Crypto EPIC content, I’m building some siiick Blockchain Products, and I would love to give you exclusive access to them ;) @mrtzneto

Now let’s get started:
Open the contract you downloaded in your Text Editor.
Go to Line 3–15 and look at the comment section. Although this is a comment section, this will help you down the track. The name of the template ICO is ‘bitfwd’ CROWDSALE token contract
Change Line 4 to the title of your crowdsale.
You will just change Line 6 after you deploy the contract on the Blockchain.
Change Line 7’s Symbol to your respective coin name (Keep it short)
Change Line 8 to the name of your token

Next:

Go to Line 102 and change “bitfwd” to “(YourCrowdsaleName). DON’T USE SPACE OR IT WON’T WORK.
Do the same for Line 118
Go to Line 119 and change the symbol name, the same as the ones you did in the comment section
Do the same for Line 120
Leave Decimals at 18.
On line 122 you will have to define you first ICO parameter, when does the bonus ends?
And on line 123, you will define when does the Crowdsale ends.

Alright, we are almost done editing the contract code.

Now, go to line 212. On that comment, write what is the amount of your tokens you will be giving away for ETH.
On line 218, define how much people will get within the BONUS.
On line 220, define how much people will get without the BONUS (the same ratio that you put on line 212).
The “msg.value” is the amount of ETH that someone sent. So taking my contract as example, for every 1 ETH, i would give 1000 FWD in return.


Boom! The contract is done. Yes, it was that easy right? Now we are going to do some fun stuff, so bare with me until the end!

Go to http://remix.ethereum.org/
In the browser/ballot.sol, paste the code you just edited! If something red comes up, there is something wrong in the code. If there are any yellow warnings it’s alright, let’s hope for the best.

Remix Editor
Now Under Compile→Choose the Token you are creating →Details
On ByteCode press the 📋button to copy the ByteCode to your clipboard.
Now, you will paste it into code editor. DON’T FREAK OUT. There will be a lot of stuff there. The one and only thing we want is the BYTECODE (a huge chunk of numbers and letters) from the object. What you will see will be like: “object”: “BYTECODE”, .
Add 0x to the beginning of the BYTECODE, like: “object”: “0xBYTECODE”,. And copy it to another file on the text editor.

The object BYTECODE with 0x added at the beginning
Now, go to MEW where we will start to deploy the contract. REMEMBER we want to be on the Ropsten Test Network so make sure the top right hand corner says that.
Navigate to the Contracts tab → Press Deploy Contract
Paste your ByteCode into the ByteCode box. Your gas limit should automatically update
Access your wallet by going into the Private Key → Enter your private key →Unlock your wallet
Now press Sign Transaction → Deploy Contract
ATTENTION: This is the moment where you have to cross your fingers for the first time during a few seconds. 🤞
Click on the transaction tx or access https://ropsten.etherscan.io to check if the contract went through. If it didn’t, start again and try to figure it out what you got wrong. If it worked, you did it, you little cryptohead!

COINgratulations! ba-dum-ts.
If everything works out, this is a sample image of what you should be seeing.


Now we are going to register this contract. To do that:

In the Overview Tab → Click on the Contract Address
Go to the Contract Code Tab → Click Verify and Publish

Nearly there… The following steps are really important. So pay attention. Basically what we are doing here is trying to guarantee that the code fits what you saying you are deploying and registering this on the network. FOREVER.

So if you commit mistakes, it will be wrong forever. What a good friend once told me is that on the Blockchain:

Get it right once or get it wrong forever.
Now you have 5 things to do on this page.

Be sure that the contract address field corresponds to the contract address that you have just deployed. Remember contract address is different to the MEW address you created so make sure not to get them confused
The contract name has to match the one in the code, in my case is this: bitfwdToken. This was on Line 102 in your code
To check which version of the complier, go back to the remix page where you got the BYTECODE from and look at the URL, the complier version will be there. In most cases it should be: v0.4.19+commit.c4cbbb05.js
On Optimisation, choose No (We haven’t enable it before).
On ENTER THE SOLIDITY CONTRACT CODE BELOW, copy the whole code from Remix, and paste in that area. NOT THE BYTECODE, but the code itself. Can also be copied from your text editor.
*Remember to add on line 6 the contract address that has been generated!

Now, leave the other fields in blank and click on Verify and Publish.

But be aware… This is the moment that you were waiting for… It is about to happen!

FINGERS CROSSED AGAIN FOR VITALIK’S SAKE. 🤞


The last challenge.
The moment of truth…


Success!!!
If a success page come along with green checkmarks and stuff, you did it! You’ve made it, I’m proud of you, now you are a cypher punk, a part of the crypto movement. Yaaaaaaay!

If a red message comes along…try it again and see where you might have missed a step. I’m happy to try to help if you leave a comment below but remember you have to do the work, no free pizzas here.

Ok, so how does it work?
It’s pretty straight forward, you send Ropsten ETH to the just deployed Contract Address and it will send you your brand new Tokens in return at the rate that you previously defined on the Code, and anyone who sends will also receive the Tokens.

Voilá.👨‍🎨

The Ropsten ETH sent will be allocated to the contract owner address.

You in this case 🦄

Considerations:
Remember! This contract has not been audited, meaning that if you are thinking about doing this on Main Net, you should definitely hire someone who has a crazy good idea of what are they doing and has tons of evidence to show you. Remember what happen in the DAO Hack right? Really not cool.
If you got here, you just acquired some sick Blockchain superpowers, be proud and remember to use this to do good things to the community, to inspire people, to build cool shit, and NOT TO DO ANOTHER FUCKING SCAM ICO.
Although I have faith on you, what you decide to do with these skills, it’s on yourself, absolutely not my responsibility, for good or bad.
Leave any questions or comments in the section below and share with everyone if you are working on something interesting. The bitfwd community is always keen to help with cool and meaningful projects.


Keep Reading.
NOW WHAT?
🚨🚨Post on the comments the address for your Ropsten ICO so people can see your Smart Contract and also get some of your tokens!
