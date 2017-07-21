# Home

Welcome to the Documentation of Oraclize!

The documentation is divided in the following sections:

* [Background](#background): the rationale behind the Oraclize's Oracle Model
* [General Concepts](#general-concepts): the main concepts behind Oraclize 
* [Data-Sources](#data-source):  information regarding the types of data sources Oraclize supports
* [Integrations](#integrations): how to integrate a blockchain application with Oraclize
* [Development Tools](#development-tools): a list of tools to aide development of Oraclize-integrated smart contracts
* [Security Deep Dive](#security-deep-dive): how Oraclize's Authenticity proofs works 
* [Pricing](#pricing): information on our pricing model for production uses 


## Background 

Oraclize is the leading oracle service for smart contracts and blockchain applications, serving thousands of requests for day every day on Ethereum, Bitcoin and Rootstock.

In the blockchain space, an oracle is a party which provides data. The need for such figure arise from the fact that blockchain applications, such as Bitcoin scripts and smart contracts cannot access and fetch directly the data they require: price feeds for assets and financial applications; weather-related informations for peer-to-peer insurance; random number generation for gambling. 

But to rely on a new trusted intermidiary, the oracle in this case, it would be betraying the security and reduced-trust model of blockchain applications: which is what makes them interesting and useful in first place. 

One solution is to accept data inputs from more than one untrusted or partially trusted party and then execute the data-dependant action only after a number of them have provided the same answer or an answer within some constrains. This type of system can be considered a decentralized oracle system. Unfortunately, this approach has severe limitations:

* It requires a predefined standard on data format 
* It is inherently inefficient: all the parties participating will require a fee and, for every request, it will take time before reaching a sufficient number of answers. 

The solution developed by Oraclize is instead to demonstrate that the data fetched from the original data-source is genuine and untampered. This is accomplished by accompanying the returned data together with a document called authenticity proof. The authenticity proofs can build upon different technologies such as auditable virtual machines and Trusted Execution Environments. 

A more detailed overview of Oraclize authenticity proofs is provided in the [Authenticity Proofs](#Authenticity Proof) section of this documentation.

This solutions elegantly solves the Oracle Problem:
* Blockchain Application's developers and the users of such applications don't have to trust Oraclize; the security model is mantained.
* Data providers don't have to modify their services in order to be compatible with blockchain protocols. Smart contracts can directly access data from Web sites or APIs. 

Oraclize engine can be easily integrated with both private and public instances of different blockchain protocols.

While building the service, the Oraclize team has realized that the concept of authenticity proofs has much broader applicability that initially envisioned. For example, the Oraclize Random Data-source can be used even by traditional gambling applications to ensure users of continuous fairness of operation
