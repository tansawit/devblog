---
author: "Sawit Trisirisatayawong"
title: "Blockchain Consensus"
date: "2020-04-06"
tags:
- daily-notes
- blockchain
- distrubuted-systems
image: /blockchain-basics/featured.jpg
---

Byzantine Fault Tolerance, Proof of Work ...

<!--more-->

## Byzantine General's Problem

Essence: how can individual parties find a way to guarantee full consensus?

**Anecdote**

Imagine a group of generals attacking a single target city. Each of them have their own army situated in different locations around the target city.

- The generals need to agree on either attacking or retreating
- It doesn’t matter which they choose, as long as they all agree on a common decision

Consider the following requirements:
- Each general haste decide and vote on either attacking or retreating
- After the vote is made, it cannot be changed
- All generals have to agree on the same decision and execute it in coordination.

What's more, the only way for them to communicate through messages. However, this brings about their own set of problems:

- Messages can be delayed, destroyed, or lost
- One or more generals may choose to send a fraudulent message, leading to total failure


**In the context of blockchains**
- Each general represent a network node
- They need to reach consensus on the state the system
	- The majority of participants within a distributed network have to agree and execute the same actions to avoid failure

A blockchain or any other system that is able to resist this type of problem is said to be Byzantine Fault Tolerant.

## Byzantine Fault Tolerance

The property of a system that is able to resist the class of failures derived from the Byzantine General’s Problem. A BFT system is able to continue to operating even if some of the nodes fail to communicate or behave maliciously.

There are multiple ways of building a BFT blockchain (Proof of Stake, Proof of Work, etc.) which are related to the different types of Consensus Algorithms.

## Proof of Work

A concept that substitute a formal barrier to participation with an economic one: the weight of a single node in the consensus voting process is directly proportional to the computing power that the node brings.

**Proof of Work Condition**
The double-SHA-256 hash of every block, treated as a 256-but number, must be less than a dynamically adjusted target.

This is to make block creation computationally hard.

As SHA256 is designed to be a completely unpredictable pseudo-random function, the only way to create a valid block is simply trial and error, repeatedly incrementing the nonce and seeing if the new hash matches.

## Proof of Stake

Instead of calculating the weight of a node as being proportional to the computational resources it brings such as in Proof-of-Work, Proof-of-Stake consensus algorithms instead calculate it based based on the node's currency holdings.
