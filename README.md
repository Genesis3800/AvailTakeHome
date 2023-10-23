# Title: Avail Take home assignment

## Introduction to the modular architecture

- Start by talking about the famous blockchain trilemma, and how scalability on Ethereum has been a major issue for a while.
- Talk about how Ethereum being monolithic contributes to the trilemma. Also explain what being monolithic even means.
- This would mean delving into the different layers, i.e. *Consensus, Execution, Settlement, Data availability*.

> Maybe include a graphic from somewhere like [canva.com](www.canva.com) that shows a monolithic blockchain's architecture.

- Now that the reader understands what a monolithic blockchain is, we tell them that the next section talks about how some current solutions that secure millions in value leverage the power of modularity.
- This brings us to Rollups.

## Rollups

- We expect the reader to be familiar with projects like Scroll and Optimism, and the basic consensus differences between them. As in the reader should know that Scroll uses ZK proofs and Optimism uses an Optimistic approach.
- We talk about how Rollups are a great way to scale Ethereum, and how they are essentially taking on the responsibility of executing transactions while still using Ethereum as the settlement layer.
- This means it is perfectly possible to take on at least one of Ethereum's responsibilities.

- What if there was a project that took on some of the other responsibilities of Ethereum, say for example **data availability** ?

## Why bother with data availability?

- The previous section showed how Rollups can take on the responsibility of executing transactions, and that it may be possible to take on the responsibility of data availability. But why should we bother with doing that?
- We remind the users that while executing txns off-chain scales blockchains significantly, data availability is still a bottleneck. Ethereum's architecture by design disincentivizes storing large amounts of on-chain data.
- This means if some other project takes on the responsibility of becoming the data availability layer, new possibilities open up.

- Cue *Validiums* and *Sovereign Rollups*.

- ZK rollups use ZK proofs to attest to the correctness of the data, and also store data on-chain, thus using Ethereum as the data availability layer. What if we still posted ZK proofs to attest to data correctness to on-chain contracts, but stored the data off-chain? This is what Validiums do.

- Lets get even more creative. What if, we do the same execution off-chain, but do not post any sort of data or ZK proof to Ethereum through a smart contract? What if we posted that data to an independent data availability layer? This is what Sovereign Rollups do.

> This is where the concept of an independent data availability layer should start making sense to the reader, and how it opens up a realm of possibilities.
> Finally to deal the ***coup de grace***, we expose the reader to the possibility of a data availability layer that can serve all of these different types of Rollups simultaneously. This is where Avail comes in.
> Also, include another fancy graphic that shows different kinds of blockchains posting to Avail as a data availability layer.

## Avail

- ***Cue Avail***.

- Avail is a consensus agnostic, unopinionated data availability layer that can serve all types of blockchains and rollups.
- Avail is a data availability layer that appends new data to the network in the same way as a blockchain, and does so using the POS consensus mechanism, but ***does not*** execute any transactions.
- Avail implements fraud proofs to ensure that the data posted to the network is correct, and also uses a slashing mechanism to disincentivize bad actors.
- To make sure that running an avail node is as cheap as possible, Avail allows validators/node operators to participate in any of the 3 capacities: ***Light nodes, Full nodes, and validators***.
- Talk about how Avail would make it very simple for '*applications*' built on top of it to download data, because each application will have a unique identifier, akin to a traditional ChainID, that will allow it to work with only the data relvant to it from within the Avail network. 
- Lastly, we can talk about some types of rollup architectures possible with Avail that have been built in-house by the Avail team:
for example the [op-EVM](https://github.com/availproject/op-evm).

- Maybe even contrast Avail from competitors like Starknet because unlike Starknet, Avail is not a Data Availability Committee. This could be expanded to contrast Avail with other competitors as well.
