# Governance Based Migrations

As the project grows, deploying new features to contracts becomes necessary in order to ensure both MARS token’s long-term sustainability, and a continuous evolution and adaptation of the Mars Protocol and ecosystem.
Currently, there are two popular approaches to solve this: PancakeSwap’s and Goosedefi’s.

Let’s look at why both are bad solutions:

* **PancakeSwap** uses a “migrator code,” which was initially implemented by SushiSwap on Ethereum. This code brings a [security vulnerability](https://github.com/quantstamp/sushiswap-security-review#32-migrate-is-dependent-on-a-currently-unspecified-migrator-contract) that was listed as a [red flag by Binance](https://www.binance.org/en/blog/how-to-identify-malicious-contract-on-binance-smart-chain/). PancakeSwap could potentially take all of your money by using a malicious migrator. Even if they never do it, we believe that having a backdoor on a smart contract removes all the benefits of decentralized platforms. Even without the need for a malicious actor from within PancakeSwap’s dev team, if their private keys are compromised, your tokens are at risk. PancakeSwap justifies the migrator code arguing that it is necessary for migrating to new versions of the project. But, you should ask yourself: Would you sign a contract with a closure which terms that the other party can modify at any given point without your consent?
* **Goosedefi** decided to go with a different approach, and removed the migrator code altogether. This action quickly became the standard for new farms. An issue with this approach is that the DeFi ecosystem is constantly evolving, and it’s doing it really quick. For example: __How can projects survive years without ever updating their codebase and main contracts?__. UniSwap V3 brings an innovative way of thinking and reingeneering LPs, but projects without migrator code would never be able to evolve. Goosedefi was born in 2021, and (sad as it is) it’s code will be in its current form forever.

MarsSwap solves migrations by using its Governance protocol. Instead of being unilaterally able to migrate LPs, any migration must be approved by MARS token holders. This strategy will allow MarsSwap to evolve and keep growing while ensuring that any change is beneficial for the token holders.  
The governance contract is behind a Timelock contract, so MARS holders who disagree with a voting result will have time to exit the pools.

