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




- without proof-of-work you cannot the network will not accept the validation of an transaction
- what is a validation of a transaction?