# Terminology and common sense
Since we’ve been working on the edge of traditional fintech and blockchain, we need to clarify certain terms used 
throughout this book as well as provide a brief overview of the specific perspective from which we analyze those 
well-known concepts.

## For traditional CTOs / architects / full stack engineers / BAs / PMs:

### Transaction
A cryptographically signed set of operations that initiates a change in the state of some ledger.

### Ledger
A database that stores information about accounts, their balances, and permissions.

### Node
A hardware and software system that stores the full history of transactions and makes decisions to update the ledger 
state.

### Distributed ledger
A ledger that is managed and stored by multiple parties.

### Blockchain
We won’t be using the word “blockchain” (for the most part). For an engineer, “blockchain” (or DLT) should mean a secure 
method of storage and synchronization of a ledger between independent parties who do not necessarily trust each other. 
This method is based on 1) cryptographic mechanisms (hashes, digital signatures) and 2) consensus protocols. Their 
application will be described in this book with no cliches such as “blockchain will save the world” or alternatively 
“blockchain is slow and not a magic pill”, but rather it will be derived primarily from the security model requirements 
for accounting systems. And obviously, techniques in this book are NOT about issuing cryptocurrencies and getting rich 
overnight.

Why are we talking about DLT/blockchain in the first place? After all, this may seem strange in the context of applying 
it to a centralized business. In fact, it is not, and there are several reasons for that. All reasons stem from existing 
requirements for IT systems that should provide an adequate level of security while operating on the Internet:
1. The integrity of transactions and their history should be controlled via a digital signature. 
2. Non-repudiation of every action in the system should be guaranteed. 
3. Every user/admin should have a digital identity. 
4. The IT infrastructure should have no single point of failure (this applies even to the case of a few departments of 
one business or multiple branches of one bank). 
5. Decision-making in a distributed environment (stakeholders of a business are distributed) should be protected by 
cryptography and the consensus mechanism. 
6. Reconciliation between different businesses should be based on mathematics and not on their trust towards each other 
or an intermediary.

If one tries to implement such requirements from scratch, he/she will end up with the techniques described in this book.

## For blockchain engineers:

### Bitcoin
The first permissionless, censorship-resistant financial system. It has already found its niche, challenging the belief 
that money should always be tied to a state (as with religion, information production, or the freedom of speech). But 
this isn’t the focus of this book. We are trying to show how the existing approaches, some of which were introduced 
first in Bitcoin, can be applied to digitize ALL assets—whether they are issued by a startup in the form of a share, by 
a state for fiat currency, by a warehouse for warehouse receipts, etc. So we will mostly discuss the situation where 
identified parties want to transact with each other.

### Utility token issuance
Our ideas are far from that. This was popular during the ICO hype period of 2017 when people blindly copied the Bitcoin 
approach and tried to tie it to a centralized business (which makes no sense).

### Token
To avoid confusion, we won’t be using the word token at all. The reason for this is that most people use the words 
*token, coin, cryptocurrency, and digitized/tokenized asset* interchangeably while meaning completely different things. 
The closest definition for a *token is an accounting unit used to represent the user’s balance of some asset* (it could 
be a currency, commodity, security, etc.). A token is NEVER an asset—it is just the representation of ownership rights 
for an asset. Therefore we won’t be using terms such as *“transfer of a token”* because, in the end, this is all about 
assets, and assets don’t care how and where they are accounted for—whether it is on paper, Excel, MySQL, or some 
distributed ledger. Instead, we will be using terms such as *“transfer of an asset”*, *“transfer of a tokenized asset“*, 
*“transfer of an ownership right”*.

### Blockchain
We won’t be referencing any particular blockchain if not stated otherwise. The meaning of *blockchain is a secure method 
of storage and synchronization of the ledger between parties who do not trust each other*. The level of trust (or 
mistrust) between parties defines the consensus algorithm that should be used, and it can vary, from PoW and PoS to BFT 
and FBA, etc. We will explicitly mention public permissionless blockchain systems if we need to provide such an example.

### DLT (Distributed ledger technology)
In this book, the two terms, blockchain and DLT, are identical because they both refer to the stack of technologies 
applied to synchronize time-ordered data between several parties.

### Cryptocurrency
A permissionless accounting system with all processes decentralized: asset issuance, transaction confirmation, data 
storage, accounting system audit, and governance (decision-making about the updates). Anyone can become a member of the 
system, hold assets, and perform transactions under rules that are the same for all.

### Tokenization
In asset accounting and management transformation, the ownership of an asset is controlled directly herein via a 
cryptographic key. It doesn't change the principles of accounting or legal compliance—we still have ledgers, accounts, 
balances, and transactions. But now, any change in the system is always a separate transaction signed via a digital 
signature of its initiator.

### Tokenized asset
An ownership right for an asset that is managed via a cryptographic key.