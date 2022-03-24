---
tags: [Whitepaper]
---

[[lightning-network-paper.pdf]]

# The Bitcoin Lightning Network: Scalable Off-Chain Instant Payments  

### Authors
- Joseph Poon - joseph@lightning.network  
- Thaddeus Dryja - rx@awsomnet.org


## 1 The Bitcoin Blockchain Scalability Problem
The payment network Visa achieved 47,000 peak transactions per second (tps) on its network during the 2013 holidays<sub>2</sub><sup>2</sup>, and currently averages hundreds of millions per day. Currently, Bitcoin supports less than 7 transactions per second with a 1 megabyte block limit. If we use an average of 300 bytes per bitcoin transaction and assumed unlimited block sizes, an equiva-  
lent capacity to peak Visa transaction volume of 47,000/tps would be nearly 8 gigabytes per Bitcoin block, every ten minutes on average. Continuously, that would be over 400 terabytes of data per year.

## 2 A Network of Micropayment Channels Can Solve Scalability
“If a tree falls in the forest and no one is around to hear it, does  
it make a sound?”  

The above quote questions the relevance of unobserved events if nobody hears the tree fall, whether it made a sound or not is of no consequence. Similarly, in the blockchain, if only two participants care about an everyday recurring transaction, it’s not necessary for all other nodes in the bitcoin network to know about that transaction.

### 2.1 Micropayment Channels Do Not Require Trust  
Like the age-old question of whether the tree falling in the woods makes a sound, if all parties agree that the tree fell at 2:45 in the afternoon, then the tree really did fall at 2:45 in the afternoon. Similarly, if both counterparties agree that the current balance inside a channel is 0.07 BTC to Alice and 0.03 BTC to Bob, then that’s the true balance.