---
layout: single
categories: ideas
title: VC Fund ICO Idea
excerpt: >
  I broke the trail of the Real Estate idea to pursue what I considered a unique opportunity
  that pulled me into the mesmerizing world of cryptocurrency ICOs.
---

So after a few conversations with a friend, and due to the apparent explosion of interest in ICOs in the past few months, I decided to give ICOs a shot. There was no long-term plan here &mdash; I simply wanted to move quickly and run a test to see if it's actually possible to raise a bunch of money for a project. The project itself didn't matter so much &mdash; to quote Miley Cyrus: "it's the climb". 

## Tool of choice

I used [Notion](https://notion.so) for planning and documenting everything. It works great &mdash; mostly like a Google Doc with nested pages &mdash; and so here's what that looked like:

![Notion - Blockchain ICO plan](/assets/notion-blockchain.png)

## The Plan

- Understand the Basics
- Find an Idea
- [16 July] Pre-announce the ICO
- [17 July] Draft the White Paper
- [18 July] Draft copy for the Wesbite
- [20 July] Launch the website
- [19 July] Recruit prominent advisors
- [22 July] Create a basic Smart Contract
- [23 July] Reach out to ICO lists
- [24 July] Publicity
- [26 July] Launch ICO

I figured if I could get everything done in about 10 days, it'd be great &mdash; even if the experiment doesn't raise anything. 

## The Basics 🍼 

Check these excellent resources out, for an explanation of the basics:

-  [Explain Bitcoin like I'm 5](https://medium.com/@nik5ter/explain-bitcoin-like-im-five-73b4257ac833) 
-  [Blockchain 101: A visual demo &mdash; Video](https://www.youtube.com/watch?v=_160oMzblY8) 
-  [Ethereum WhitePaper](https://solidity.readthedocs.io/en/latest/introduction-to-smart-contracts.html) 

For more on Ethereum, read along:

### Ethereum Concepts

Source: [https://github.com/ethereum/wiki/wiki/White-Paper](https://github.com/ethereum/wiki/wiki/White-Paper) 

#### Accounts

An Ethereum account contains four fields:

- The **nonce** , a counter used to make sure each transaction can only be processed once
- The account's current **ether balance** 
- The account's **contract code** , if present
- The account's **storage** (empty by default)

In general, there are two types of accounts: **externally owned accounts** , controlled by private keys, and **contract accounts** , controlled by their contract code. 

 _An externally owned account has no code_ , and one can send messages from an externally owned account by creating and signing a transaction. In a contract account, _every time the contract account receives a message its code activates_ , allowing it to read and write to internal storage and send other messages or create contracts in turn.

#### Contracts

Note that "contracts" in Ethereum should not be seen as something that should be "fulfilled" or "complied with"; rather, they are more like "autonomous agents" that live inside of the Ethereum execution environment, **always executing a specific piece of code when "poked" by a message or transaction** , and having direct control over their own ether balance and their own key/value store to keep track of persistent variables.

#### Transactions

The term "transaction" is used in Ethereum to refer to the signed data package that stores a message to be sent from an externally owned account. Transactions contain:

- the recipient of the message;
- a signature identifying the sender;
- the amount of ether to transfer from the sender to the recipient;
- an optional data field;
- a `STARTGAS` value, representing the maximum number of computational steps the transaction execution is allowed to take; and
- a `GASPRICE` value, representing the fee the sender pays per computational step.

#### Messages

Contracts have the ability to send "messages" to other contracts. Messages are virtual objects that are never serialized and exist only in the Ethereum execution environment. A message contains:

- the sender of the message (implicit);
- the recipient of the message;
- the amount of ether to transfer alongside the message;
- an optional data field; and
- a `STARTGAS` value.

Essentially, **a message is like a transaction** , _except it is produced by a contract and not an external actor_ . A message is produced when a contract currently executing code executes the `CALL` opcode, which produces and executes a message. Like a transaction, a message leads to the recipient account running its code.

### Ethereum Code Execution

#### Storage

The operations have access to three types of space in which to store data:

- The stack, a last-in-first-out container to which values can be pushed and popped
- Memory, an infinitely expandable byte array
- The contract's long-term storage, a key/value store. Unlike stack and memory, which reset after computation ends, storage persists for the long term.

The code can also access the `value` , `sender` and `data` of the incoming message, as well as block `header` data, and the code can also return a byte array of data as an output.

#### Blockchain & Mining

The main difference between Ethereum and Bitcoin with regard to the blockchain architecture is that, unlike Bitcoin, **Ethereum blocks contain a copy of both the transaction list and the most recent state** . Aside from that, two other values, the block number and the difficulty, are also stored in the block.

### Questions I had that were later clarified:

- If gas is used every time the program is executed, and the program is executed on multiple nodes (presumably, simultaneously) — what's to prevent all of the gas from getting consumed _each time_ ? Answer [here](https://ethereum.stackexchange.com/a/21091/14187)
- Where is stuff actually _stored_ ? Answer [here](https://ethereum.stackexchange.com/a/6413/14187) 

## Finding an Idea

Now that we're armed with a better understanding of the blockchain, bitcoin and more importantly *Ethereum* &hellip; we'll need an idea to execute on.

According to [this](https://blog.gdax.com/how-to-raise-money-on-a-blockchain-with-a-token-510562c9cdfa) , we should find an idea that can benefit from Network Effects (i.e. the more users that use it, the better it gets).

> The biggest benefit to the token model is that it provides the economic incentives for your network to get off the ground and overcome the classic chicken and egg problem. In other words, it gives all users of your app the ability to own a little piece of your network, incentivizing them to start using it at the start — Fred (Cofounder, Coinbase)

### Examples

-  [Storj.io](https://storj.io/) : Storj is a system for decentralized file storage. Like Bitcoin or Ethereum, there is no central operator of the network. The project raised $30m through a crowdfund of their token, Storjcoin, on the blockchain.
-  [Steem](https://steemit.com/) : a decentralized Reddit where people are paid to contribute news and content.

> You’ll notice one other thing about these “projects” or “apps”: they are really decentralized software protocols. A protocol is a fancy technical term that means: a standard language that lets a bunch of people on the internet work together on a specific problem. — [Source](https://blog.coinbase.com/app-coins-and-the-dawn-of-the-decentralized-business-model-8b8c951e734f) 

### Types of Applications

In general, there are three types of applications on top of Ethereum. 

- Financial applications, providing users with more powerful ways of managing and entering into contracts using their money. This includes sub-currencies, financial derivatives, hedging contracts, savings wallets, wills, and ultimately even some classes of full-scale employment contracts. 
- Semi-financial applications, where money is involved but there is also a heavy non-monetary side to what is being done; a perfect example is self-enforcing bounties for solutions to computational problems. 
- Other applications such as online voting and decentralized governance that are not financial at all.

### Found an Idea

Simple. Build a VC firm, based on the blockchain.

For the name, I had a number of choices:

-  [herd.capital](http://herd.capital) 
-  [collect.capital](http://collect.capital) 
-  [general.capital](http://general.capital) 
-  [general.fund](http://general.fund) 
-  [every.fund](http://every.fund) 
-  [verify.fund](http://verify.fund) 
-  [unit.fund](http://unit.fund) 
-  [lot.fund](http://lot.fund) 
-  [elect.fund](http://elect.fund) 
-  [elected.fund](http://elected.fund)

Ended up using **Unit.Fund**
