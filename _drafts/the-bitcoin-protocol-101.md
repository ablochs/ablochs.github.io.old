---
layout: post
title:  "The Bitcoin protocol notes"
date: 2015-03-20
categories: bitcoin
tags: [bitcoin]
---

## Notes

- how can we prevent her from using the same bit string over and over
- Anyone in the world (including Bob) can use Alice’s public key to verify that Alice really was the person who signed the message “I, Alice, am giving Bob one infocoin”.
- What we’d like is a way of making infocoins unique. They need a label or serial number. 
- To make this scheme work we need a trusted source of serial numbers for the infocoins. One way to create such a source is to introduce a bank.
- Make everyone the bank
- Let’s suppose she uses an automated system to set up a large number of separate identities, let’s say a billion, on the Infocoin network.
- There’s a clever way of avoiding this problem, using an idea known as proof-of-work. The idea is counterintuitive and involves a combination of two ideas: (1) to (artificially) make it computationally costly for network users to validate transactions; and (2) to reward them for trying to help validate transactions. 
- The benefit of making it costly to validate transactions is that validation can no longer be influenced by the number of network identities someone controls, but only by the total computational power they can bring to bear on validation
- What is the proof-of-work (POW) that needs to be solved
- The puzzle David has to solve – the proof-of-work – is to find a nonce x such that when we append x to l and hash the combination the output hash begins with a long run of zeroes.
- So if we want the output hash value to begin with 10 zeroes, say, then David will need, on average, to try 16^{10} \approx 10^{12} different values for x before he finds a suitable nonce. That’s a pretty challenging task, requiring lots of computational power.
- Obviously, it’s possible to make this puzzle more or less difficult to solve by requiring more or fewer zeroes in the output from the hash function. In fact, the Bitcoin protocol gets quite a fine level of control over the difficulty of the puzzle, by using a slight variation on the proof-of-work puzzle described above. Instead of requiring leading zeroes, the Bitcoin proof-of-work puzzle requires the hash of a block’s header to be lower than or equal to a number known as the target. 
- In the Bitcoin protocol, this validation process is called mining. For each block of transactions validated, the successful miner receives a bitcoin reward. Initially, this was set to be a 50 bitcoin reward. But for every 210,000 validated blocks (roughly, once every four years) the reward halves. This has happened just once, to date, and so the current reward for mining a block is 25 bitcoins. This halving in the rate will continue every four years until the year 2140 CE. At that point, the reward for mining will drop below 10^{-8} bitcoins per block.  10^{-8} bitcoins is actually the minimal unit of Bitcoin, and is known as a satoshi.
- A miner’s chance of winning the competition is (roughly, and with some caveats) equal to the proportion of the total computing power that they control.
- We’d ideally like the Infocoin network to agree upon the order in which transactions have occurred
- Occasionally, a fork will appear in the block chain. This can happen, for instance, if by chance two miners happen to validate a block of transactions near-simultaneously
- Fortunately, there’s a simple idea that can be used to remove any forks. The rule is this: if a fork occurs, people on the network keep track of both forks. But at any given time, miners only work to extend whichever fork is longest in their copy of the block chain.
- In Bitcoin proper, a transaction is not considered confirmed until: (1) it is part of a block in the longest fork, and (2) at least 5 blocks follow it in the longest fork.

- without proof-of-work you cannot the network will not accept the validation of an transaction
- what is a validation of a transaction?


## Links
[http://www.michaelnielsen.org/ddi/how-the-bitcoin-protocol-actually-works/](http://www.michaelnielsen.org/ddi/how-the-bitcoin-protocol-actually-works/)