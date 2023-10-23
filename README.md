## Problem statement

# **Avail Technical Writer Exercise**

# **Context**

As part of getting to know you better, we want you to know what it will be like to work with us at Avail, and for us to understand how you work as well. We have developed this challenge to learn how you work to get things done, including how you learn new concepts, how you manage your time and set milestones, and how you communicate with the team.

# **The Process**

The goal is to tackle the challenge below in a realistic way. We are a remote-first team, and are more than happy to join a shared chat of your choice (Telegram, Slack, etc) to answer any questions. We can also set up meetings for more in-depth discussion as often as needed—just ask.

Please keep us updated on your progress and timelines, and whether you need anything from us to make progress.

The output will be judged on technical depth, clarity, and fitness for purpose. But note that you will be evaluated on the entire process, it is not just about the output.

# **The Challenge**

We need to create a new section in the docs about how modular blockchains work, and how the various components of the modular ecosystem can be used together to create designs for the challenges that developers are faced with.

Please create the following:

1. An overview of how you would structure this section, what you would include as the main sub-sections, and which key points would be needed in each. You do not need to create the content itself, only a high level overview/outline.

2. An intro section explaining how Avail fits in when it comes to the Modular Blockchain architecture.

## My Answer

### Introduction to the modular architecture

- Start by talking about the famous blockchain trilemma, and how scalability on Ethereum has been a major issue for a while.
- Talk about how Ethereum being monolithic contributes to the trilemma. Also explain what being monolithic even means.
- This would mean delving into the different layers, i.e. *Consensus, Execution, Settlement, Data availability*.

> Maybe include a graphic from somewhere like [canva.com](www.canva.com) that shows a monolithic blockchain's architecture.

- Now that the reader understands what a monolithic blockchain is, we tell them that the next section talks about how some current solutions that secure millions in value leverage the power of modularity.
- This brings us to Rollups.

### Rollups

- We expect the reader to be familiar with projects like Scroll and Optimism, and the basic consensus differences between them. As in the reader should know that Scroll uses ZK proofs and Optimism uses an Optimistic approach.
- We talk about how Rollups are a great way to scale Ethereum, and how they are essentially taking on the responsibility of executing transactions while still using Ethereum as the settlement layer.
- This means it is perfectly possible to take on at least one of Ethereum's responsibilities.

- What if there was a project that took on some of the other responsibilities of Ethereum, say for example **data availability** ?

### Why bother with data availability?

- The previous section showed how Rollups can take on the responsibility of executing transactions, and that it may be possible to take on the responsibility of data availability. But why should we bother with doing that?
- We remind the users that storing data on Ethereum is expensive, and that is a bottleneck. Ethereum's architecture by design disincentivizes storing large amounts of on-chain data.
- This means if some other project takes on the responsibility of becoming the data availability layer, new possibilities open up.

- Cue *Validiums* and *Sovereign Rollups*.

- ZK rollups use ZK proofs to attest to the correctness of the data, and also store data on-chain, thus using Ethereum as the data availability layer. What if we still posted ZK proofs to attest to data correctness to on-chain contracts, but stored the data off-chain? This is what Validiums do.

- Lets get even more creative. What if, we do the same execution off-chain, but do not post any sort of data or ZK proof to Ethereum through a smart contract? What if we posted that data to an independent data availability layer? This is what Sovereign Rollups do.

> This is where the concept of an independent data availability layer should start making sense to the reader, and how it opens up a realm of possibilities.

> Finally to deal the ***coup de grace***, we expose the reader to the possibility of a data availability layer that can serve all of these different types of Rollups simultaneously. This is where Avail comes in.