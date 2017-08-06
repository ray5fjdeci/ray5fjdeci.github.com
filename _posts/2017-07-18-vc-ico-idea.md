---
layout: single
categories: ideas
title: VC Fund ICO Idea
excerpt: >
  I broke the trail of the Real Estate idea to pursue what I considered a unique opportunity
  that pulled me into the mesmerizing world of cryptocurrency ICOs.
---

So after some conversations with a few friends, and due to the apparent explosion of interest in ICOs in the past few months, I decided to give ICOs a shot. There was no long-term plan here &mdash; I simply wanted to move quickly and run a test to see if it's actually possible to raise a bunch of money for a project. The project itself didn't matter so much &mdash; to quote Miley Cyrus: "it's the climb". 

I knew I'd be sharing the experience later on, so I used [Notion](https://notion.so) for planning and documenting everything. It works great &mdash; mostly like a Google Doc with nested pages. Here's what that looked like:

![Notion - Blockchain ICO plan](/assets/notion-blockchain.png)

I ported everything over here, so you can just read along.

## The Plan

- Understand the Basics
- Find an Idea
- [15 July] Pre-announce the ICO
- [16 July] Draft the White Paper
- [17 July] Draft copy for the Website
- [19 July] Launch the website
- [20 July] Recruit prominent advisors
- [21 July] Create a basic Smart Contract
- [22 July] Reach out to ICO lists
- [23 July] Publicity
- [25 July] Launch ICO

I figured if I could get everything done in about 10 days, it'd be great &mdash; even if the ICO doesn't end up raising anything. It's an experiment after all&hellip; and the worst case scenario means I learn a ton about Ethereum and ICOs in the process. 

## The Basics 🍼 

I knew very little about cryptocurrencies and blockchain, so after a lot of reading I found a few resources that provided the most bang for word. 

These are:

-  [Explain Bitcoin like I'm 5](https://medium.com/@nik5ter/explain-bitcoin-like-im-five-73b4257ac833) 
-  [Blockchain 101: A visual demo &mdash; Video](https://www.youtube.com/watch?v=_160oMzblY8) 
-  [Ethereum WhitePaper](https://solidity.readthedocs.io/en/latest/introduction-to-smart-contracts.html) 

Once those are covered, we can proceed to learn more on Ethereum. Go through the last few links before reading along.

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

## Finding an Idea 🤔

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

Simple. Build a VC firm, based on the blockchain. Not complicated technically, but also solves an apparently existing problem (only available to ultra-high net worth individuals and institutions). Admittedly, I didn't think too much about this &mdash; I just wanted to get the experiment started.

I could've gone with something more exotic (and that actually benefits from the distributed nature of the blockchain), but it's unlikely I would'be been able to make much progress in just 10 days on anything more than the simplest concept.

For the name, I had a number of choices of available domain names:

-  [herd.capital](http://herd.capital) 
-  [collect.capital](http://collect.capital) 
-  [general.capital](http://general.capital) 
-  [general.fund](http://general.fund) 
-  [every.fund](http://every.fund) 
-  [verify.fund](http://verify.fund) 
-  [unit.fund](http://unit.fund) &larr; ended up using this
-  [lot.fund](http://lot.fund) 
-  [elect.fund](http://elect.fund) 
-  [elected.fund](http://elected.fund)

## Day 1: Preannouncement of the ICO 🔔 

Pre-announcement is the announcement of the future project in the communities of cryptocurrency investors, such as Bitcoin Talk, Reddit and others. The founders of the project write an executive summary - a small presentation to investors, in which they explain the essence and purpose of the ICO project. After the executive summary, the company receives the first feedback, which can be analyzed to see whether the project could interest investors or not.

 **You can pre-announce here:** 

- https://bitcointalk.org/index.php?board=159.0
- https://www.reddit.com/r/icocrypto/
- https://www.reddit.com/r/Bitcoin/

Consider using a PR group specializing in crypto, like: [https://vindynegroup.com/](https://vindynegroup.com/) 

**Things to include:**

- Summary of the offering
 [Unit.Fund](http://unit.Fund) is an Ethereum based closed-ended fund that allows anyone to invest in the world's best startups. No minimum investment amounts, and no minimum annual income means that anyone can now invest in the VC fund of the future — and realize the kind of gains only the rich could get access to.
- Social media links: 
	-  [https://twitter.com/unit_fund](https://twitter.com/unit_fund) 
	- [Slack Invite link](https://join.slack.com/t/unitfund/shared_invite/MjEzMzk0NDQwODIwLTE1MDAxMjAzOTQtZWQ2MWYwMmIxYQ) 

**Preannouncements posted:**

I posted the following pre-announcements:

- [BitcoinTalk](https://bitcointalk.org/index.php?topic=2023143)
- [Reddit](https://www.reddit.com/r/icocrypto/comments/6nrgio/preico_unit_fund_the_internets_own_vc_firm/)

Reddit fared alot better than BitcoinTalk. The overwhelming feedback from BitcoinTalk was to post with an account that's got more than just "Newbie" status (they didn't put it quite as nicely).

## Day 2: Draft the White Paper 📝


### Bullet Points

- The "Y Combinator" of online startups
- Today you're putting money in ICOs and don't know what you are getting. We solve that problem by pooling the money and vetting our investments ourselves with strict criteria. Oh, and we also have the best VCs as advisors to help guide us.
- Flipping the investor model on it's head. Instead of having a small group of Limited Partners invest all the money (and receive the lion's share of the return), we're going to raise the fund from a large group of small investors — sometimes investing as little as $1. We're democratizing the investment firm.
- Run by startup entrepreneurs, with veteran advisors: the best of the venture capital industry
- Instant Diversification. One investment gets you exposure to hundreds of investments.
- Vetted and Verified. 
- Like an Index Fund. Get exposure across multiple sectors, stages and geographies.
- The last ICO you'll ever need to invest in!

### How it Works

These points were extracted from various investment providers, including:
[Angelist Funds](https://angel.co/syndicates/for-investors#funds) [+](https://angel.co/funds) , [Republic.co](https://republic.co/crowdsafe) , [Eureeca](https://eureeca.com/Static/HowItWorksInvestors.aspx) , [CrowdCube](https://www.crowdcube.com/investing-your-money) [+](https://help.crowdcube.com/hc/en-us/categories/200958429-Investing) , [CoinList](https://coinlist.co) 

- All contributing investors are treated as a single "investor"
- Legal entity which commits the capital will be setup in a tax-free, startup friendly jurisdiction (e.g. British Virgin Islands)
- Investors can act as early adopters for the portfolio companies (a regular newsletter will got out with deal details to investors, so that they can
- How do funds select deals? Funds are designed to give broad market exposure, either to the early-stage market generally or to a specific sector (depending on the fund in which you invest). There is a multi-stage selection process that includes, among other things, evaluating co-investors, conflicts, concentration in any one syndicate and non-arms length transactions. We may not apply the same process to every deal.
- What reporting will funds do? Funds will disclose fund investments after they are finalized, and may provide qualitative updates to investors when available. Funds will not post audited financial statements. Funds will not mark valuations to market each year given the extreme difficulty of doing that in an accurate manner for early stage investments.
- Who can invest? Anyone over the age of 18 can invest. There are no net worth or income minimums, but U.S. law does limit how much you can invest. You do not need to be a U.S. citizen to invest. 
- Do you accept US investors? **No.** The US has very strict rules on marketing to or receiving investment from US persons. Therefore, we do not allow US persons — defined as persons with single or dual US nationality, persons residing in the US, or whose primary bank account is in the US — to invest through Eureeca.
- Investors can be private individuals as well as institutions. What they will all have in common is an interest in investing in high-yield potential private businesses.
- What due diligence checks are done? The due diligence check ensures that businesses applying to raise funds on Eureeca are legitimate and exist. Eureeca works with third-party compliance firms to assess if the company is incorporated, the duration of operations and that all necessary corporate and legal documents are in place. Additionally, background checks will be done on the team and founders to ensure that there is no history of fraud or other relevant criminal activity.
- Did you know that investing in early stage investments can generate an annual return of 27%? Bearing that in mind, how much do you think you would allocate to investing in SMEs per year?
- What is verified? The agency’s evaluation spans technical features of the platform in question, the business model and market niche, the team and business experience in the blockchain industry and development, strengths and weaknesses of the decentralized infrastructure, and other factors like technical background (e.g. quality of the prototype or source code), and analysis of community feedback.
- ICORating conducts the research of all aspects of the project, which stand for specific cryptocurrency financial instrument. The company analyzes the investment risks of the project entering ICO, in the following areas:
	- business model (its relevance, strong and weak points);
	- market niche (prospects and dynamics of the selected market niches for building business);
	- team (business experience in the traditional market segment, in blockchain industry, blockchain-development experience);
	- competition (competitive pressure level on the part of companies with similar business models of the traditional market segment and blockchain-economy);
	- technical background (availability and quality of the prototype or source code);
	- analysis of the feedback from the community;

### Relevant White Papers

- [TaaS Fund](http://taas.fund/media/whitepaper.pdf)
- [DAO Hub](https://forum.daohub.org/uploads/default/original/2X/6/6589831b3add67773e4e5af745f42b73c1712c86.pdf)
- [EncryptoTel](http://ico.encryptotel.com/assets/pdf/EncryptoTel_WP_v1.pdf)

### Resources

- [http://www.paulgraham.com/angelinvesting.html](http://www.paulgraham.com/angelinvesting.html)
- [http://venturehacks.com/articles/angel](http://venturehacks.com/articles/angel)

### Notes on becoming a good angel investor (by PG)

- To be a good angel investor, you have to be a good judge of potential.
- If you can recognize good startup founders by empathizing with them—if you both resonate at the same frequency—then you may already be a better startup picker than the median professional VC
- What makes **a good founder** ? _Good founders have a healthy respect for reality. But they are relentlessly resourceful. That's the closest I can get to the opposite of hapless. You want to fund people who are relentlessly resourceful. — PG_ 
- Bet on **people** .
- The problem is not finding startups, exactly, but finding a stream of reasonably high quality ones.
- If you want to invest seriously, the way to get started is to bootstrap yourself off your existing connections, be a good investor in the startups you meet that way, and eventually you'll start a chain reaction.
- To be good, be decisive. There's a hack for being decisive when you're inexperienced: ratchet down the size of your investment till it's an amount you wouldn't care too much about losing.

### The White Paper

You'll find the final version of the paper below:

[ ![PDF Icon](/assets/icon-pdf.svg) Read UnitFund Whitepaper](/assets/unitfund-whitepaper.pdf)

I had to think through a few things, and the white paper provided a good avenue to do so. I included things liked minimum raise amount, maximum raise, investment strategy, etc. It's light on details, but again &mdash; I could always figure those out later.

## Day 3: Draft copy for the Website 🌐

In order to effectively write up some copy for the website, I had to think through some things. Here's how I did that:

### What is the goal?

Get people to invest in the Unit Fund ICO

### Why would people invest in the ICO?

- Opportunity to make high returns (2.5x in 7 years)
- Greater trust for the fund than **trust** for individual ICOs

### What objections stand between them and investing?

-  **Trust** . Why the heck should I give you my money (instead of invest it myself?)

### How do you establish trust?

- Links from reputable sources
- Explain the "how" in detail — show that you have a plan.
- Demonstrate knowledge in the VC industry
	- White Paper
	- Blog posts
- Don't pretend it's guaranteed profit. Everyone knows it is not. Be upfront about the risks and highlight them before allowing anyone to invest
- Terms and Conditions
- Contact Us page: address, phone
- Clear profiles/bios of the people behind the project
- Showcase figures of authority
- Herd mentality — show that others have committed capital already

### Remember:

- Use [active voice](https://www.distilled.net/blog/distilled/content/how-to-kick-ass-at-copywriting-for-your-website/) , not passive voice
- Stay customer-focused ("you" vs. "we")
-  [Benefits, not features](https://www.useronboard.com/features-vs-benefits/) 

### Page Flow

- Explain value proposition
	- Headline
	- Herd mentality — show that others have committed capital already
	- Feature list
	- The problem it addresses
	- How the solution works
	- Plan / Roadmap
	- White Paper
	- Return-prediction tool
- Tackle Objections
	- Put terms and conditions, with confirmation modal before investing
	- Place disclaimer — no guarantees, no investors from the US
	- Links from reputable sources
	- Clear profiles/bios of the people behind the project
	- How to Contribute
	- FAQs
	- Contact Us page: address, phone

### Design Guidelines

Since we're after trust, [Blue is the appropriate base color](http://www.creativebloq.com/web-design/12-colours-and-emotions-they-evoke-61515112) to choose.

### Website Draft

Here's [a link to the draft website copy](https://docs.google.com/document/d/1sgBEND7Jaa2T2tD7_YouF95OoSri91HTtqrLtKwXTpI/edit?usp=sharing) that I prepared. 

[ ![PDF Icon](/assets/icon-pdf.svg) Read Website Copy draft](/assets/unitfund-website-copy.pdf)

## Launch the website 🎂 

### Guidelines

- Great design is **crucial** . It's a common thread among all of the most successful companies
- Have a track record that you can boast. Show off your accomplishments
- Find industry experts and add them to your "board" to build trust. They better be wearing suits.

### Tasks

- Check out previous successful crowdsale companies. You may need to use the Wayback Machine to see what the website looked like at the time of the respective ICOs for each one (since they've probably changed).
	-  [Storj](https://storj.io/tokensale) ($30M)
	-  [Brave](https://www.basicattentiontoken.org/) ($35M in 30 seconds)
	-  [Tezos](https://www.tezos.com/) ($200M)
	-  [Gigawatt](https://cryptonomos.com/wtt/) (ongoing)
- Check out [https://99bitcoins.com/bitcoin-scam-test/](https://99bitcoins.com/bitcoin-scam-test/) for guidelines of what to do/not do
- Hire a copywriter to spruce it up (Skipped)
- Hire a front-end designer to make it look like a million bucks (Skipped, used a template)
- Translate to Chinese (Skipped)
- Compress images
- Consolidate all scripts / styles into a single file (to reduce HTTP calls)
- Include proposal update samples (Skipped)

I wasn't able to get all these done (the items marked "Skipped" were skipped). I had a day to put everything together, so time was of the essence.

**TODO:** Talk about the experience with District0x, and their design firm.

## Recruit advisors 👔

Ideally, we'll need advisors in the Investing, Legal space.

I started with people in my direct network. These folks were likely to say Yes, since I knew them all:

- Hasan Haidar [500, Partner]
- Ramzy Ismail [Techstars, Director]
- Antonio Sosa [REOF Capital, MD]

There were also people that I *hoped* I'd be able to get onboard. If I closed any of these folks, there's a much higher chance that this project would succeed (because of their reputation). These folks included:

- Dave McClure [ex500]
- Paul Graham [exYC]
- Chris Sacca
- Peter Thiel
- Mark Cuban
- Justin Kan [exYC]
- Garry Tan [exYC]
- Ashton Kucher
- Jack Dorsey
- Kevin O Leary
- Jessica Alba
- Robert Herjavec
- Kevin Systrom
- Evan Williams
- Gary Vaynerchuck

I put this list together based on my knowledge of the investment space (and from my experience watching Shark Tank episodes). Many of the people on this list are ex-VCs/Accelerators, since those currently in such roles may face some conflict of interest that would prevent them from getting involved with this fund (even in an advisory capacity). Before reaching out, I needed to have some sort of strategy for approaching them.

Basic strategy I wanted to follow:
- Prepare a dedicated 60 second video to each one, explaining exactly what you want and what's in it for them.
- Prepare an image, showing all of the other folks that you plan to close, showing the recipient's name as "Pending" (in a sea of prominent names)

> Note: In retrospect, I should've focused ALOT more on this part. It was clear that this could have a huge impact on the outcome, and yet I did very little in terms of outreach and follow up. I thought that the value proposition (helping startups, making $'s &mdash; in exchange for very little of their time) was convincing enough to solicit at least passing interest from a couple of these investors. Now that I think about it, I may have sounded a little bit like a Nigerian prince to them 🤔. Getting an intro through a mutual connection > cold email.
