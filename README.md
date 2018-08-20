# A community-updated version of the official Nano FAQ
**What is Nano?**

- Nano is a trustless, low-latency cryptocurrency that uses a novel block-lattice architecture, where each account has its own blockchain and consensus is achieved through delegated Proof of Stake voting.

- It offers near instant transactions, with 0 transaction fees, and unlimited scalability. This makes Nano ideal for peer-to-peer transactions.

- The network requires minimal resources, no mining, and can process high transaction throughput. 

- To date, the Nano network has processed over four million transactions with an unpruned ledger size of only 1.7GB.

- For a more in-depth look at Nano, please read our [whitepaper](https://nano.org/en/whitepaper).

**How does Nano work?**

- Unlike conventional blockchains used in many other cryptocurrencies, Nano uses a block-lattice structure. Each account has its own blockchain (account-chain), which contains the account’s transaction/balance history. An account-chain can only be updated by the account’s owner, meaning that each account-chain can be updated immediately and asynchronously from the rest of the block-lattice. This results in quick transactions. 

- Since blocks can only be added by each account-chain’s owner, transferring funds from one account to another requires two transactions: a send transaction deducting the amount from the sender’s balance and a receive transaction adding the amount to the receiving account’s balance.

- Refer to sections three and four of the [whitepaper](https://nano.org/en/whitepaper) for a more thorough look at how Nano works.

**What are the advantages of Nano?**

*Zero Fees*

Since the protocol is so lightweight, running a node costs next to nothing. This means that all Nano transactions can be processed with no fees. One transaction fits within a single UDP packet, and transactions are handled independently, eliminating any block size issue.

*Instantaneous Transaction Speed*

Wallets pre-cache the anti-spam Proof of Work for the next transaction once a transaction is sent, making transactions instantaneous (since both sides have the Proof of Work ready to go). For ongoing transactions there may be delays, but this is intentional to prevent spam.

*Scalability*

Nano has been [profiled at 7000 transactions per second (TPS)](https://www.reddit.com/r/RaiBlocks/comments/7ko5l7/colin_lemahieu_founder_and_lead_developer_of/drj44qv/) on commodity hardware, and the production network has been successfully tested at over [300 TPS](https://medium.com/@bnp117/stress-testing-the-raiblocks-network-part-ii-def83653b21f) (limited only by the tester's ability to pre-compute Proof of Work). Additional live stress tests are planned, but Nano appears to be limited only by currently available hardware. The protocol will process transactions as fast as hardware allows.

Transaction lookups scale with the logarithm of the data set size logNO with a tree-like structure or O1 if they are based on a hash table. To get an idea of how this scales, if it was a simple binary tree with 1,000 entries it would take 10 lookups. With 1,000,000 entries it takes 20 and 1 billion would take 30. Pruned nodes only need to keep the latest block of each account-chain, further reducing lookup time and system resources.

*Energy Efficient*

Nano only consumes around 0.111 Wh per transaction (vs Bitcoin's 950 kWh), meaning  that you can make EIGHT MILLION transactions for the same power usage as a SINGLE Bitcoin transaction. This means that the Nano network is so efficient it could run on a single wind turbine! 

Nano is green! [https://youtu.be/JChBTohSHlM](https://youtu.be/JChBTohSHlM)

**Who is the team behind Nano?**

Please see our [Team Page](https://nano.org/en/team/).

**Can I mine Nano?**

Nano is not mined and has reached its maximum supply of 133,248,290 NANO. Funds were initially distributed via a captcha-based faucet distribution system that ended in October 2017. Websites claiming to mine NANO are actually mining other cryptocurrencies (e.g. Monero), to trade for NANO on an exchange, and then paying out miners in NANO, leveraging Nano’ feeless transactions.

**What is the incentive to run a node?**

While there is no direct monetary incentive (e.g. mining) to run a node, there are multiple indirect incentives:

- Businesses wanting to cut costs from credit & debit card fees (0.5%-3%)

- Supporting the network so you can take advantage of its benefits (0 transaction fees, near instant transactions, etc)

- Ideological, political, and personal incentives like providing people with access to global finance

Examples of these kinds of incentives working successfully include Wikipedia and Bitcoin full nodes.

**Where is the Nano community located?**

- Discord: [chat.nano.org](https://chat.nano.org)

- Facebook: [facebook.com/Nanocurrency/](https://www.facebook.com/nanocurrency/)

- Reddit: [/r/Nanocurrency](https://www.reddit.com/r/nanocurrency/)

- Twitter: [@Nano](https://twitter.com/Nano)

**Where is Nano traded?**

Nano is currently traded on several exchanges under the ticker symbol $NANO

- [CoinMarketCap Markets for NANO](https://coinmarketcap.com/currencies/nano/#markets)

The development team is actively working to add Nano to additional exchanges, with the goal of Nano ultimately trading on every major exchange.

Unfortunately, the Nano team is not permitted to discuss potential listings on additional exchanges until Nano is officially listed. The Nano team will announce each new exchange listing as soon as they are available.

**Where can I find the Nano wallet?**

Nano has multiple wallet options on all major platforms:

- Desktop, mobile, and online wallets can be found on [the Nano website](https://nano.org/en#getwallets)

- Some of the most popular community wallets are [Canoe](https://getcanoe.io/), [NanoVault.io](http://nanovault.io), and [NanoWallet.io](https://nanowallet.io/).

- An integrated wallet within the Telegram app is available here [https://t.me/RaiWalletBot](https://t.me/RaiWalletBot)

**What are Nano’ units?**

The NANO ticker currently represents 1 million nano (Mnano), which is 10^30 raw (the smallest unit of Nano).

Nano’ smallest unit is 1 raw (equivalent to a satoshi in Bitcoin), while 1 Gnano is the largest. 

- 1 NANO equals 1 Mnano equals 1 million nano equals 10^30 raw

- 1 NANO (uppercase) does NOT equal 1 nano (lowercase). 1 NANO currently equals 1 Mnano

NANO is the ticker used on exchanges/software to trade Mnano.

Name dividers have been put in place to notate the factor of raw units in SI notation:

| 1 Raw |  |  |  |  | | 1 unano | 1 mnano | 1 nano | 1 knano | 1 Mnano | 1 Gnano |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 10<sup>0</sup> | 10<sup>3</sup> | 10<sup>6</sup> | 10<sup>9</sup> | 10<sup>12</sup> | 10<sup>15</sup> | 10<sup>18</sup> | 10<sup>21</sup> | 10<sup>24</sup> | 10<sup>27</sup> | 10<sup>30</sup> | 10<sup>33</sup> |

**How does Nano achieve consensus?**

The voting process is balance-weighted. Every account selects a wallet address of a representative node. This is just a node that is configured to stay online and be ready to vote. When an account selects their representative, the vote weight of that account is increased by the balance of the source account.

Votes are weighted by account balances. Those who have more funds in the system are inherently incentivized to keep the system honest; a dishonest system would make their investment worthless.

Additional transactions don’t contribute to securing the network; transactions settle individually within a few seconds regardless of other network activity. Because of this there’s no reason to incentivize generating activity.

A list of current representatives, sorted by voting power, can be found [here](https://www.nanode.co/representatives). Any wallet, regardless of balance, can be a representative. A good representative is always online to vote.

**Is Nano vulnerable to attacks?**

Nano, like all decentralized cryptocurrencies, may be attacked by malicious parties for attempted financial gain or system demise. In section five of the [whitepaper](https://nano.org/en/whitepaper), we outline multiple attack scenarios, the consequences of such an attack, and Nano’ protocol for dealing with each attack. 

A summary of attacks and how Nano mitigates them can be found on the [official Nano GitHub](https://github.com/nanocurrency/raiblocks/wiki/Attacks).

**What are some of the long-term goals for Nano?**

To see the protocol itself defined as an infrequently-updated Internet Standard (RFC) that is managed by a diverse group of people from different geopolitical areas. It would not be controlled by Nano' founder or any small group of people. Any such group should not add configurable network parameters to avoid political issues (like Bitcoin's block size debate).

Add IPv6 multicast to transaction broadcasting: announcing a transaction to everyone in the world who wants it.

Have existing payment-providers accept NANO much like they accept fiat currency today.

To give the large group of people who do not have access to banks the assurance that payments they accept are secure at the point of exchange.

**How does Nano compare to other cryptocurrencies?**

*vs. Bitcoin*

Bitcoin organizes transactions into blocks with an average processing time of 10 minutes per block. For a transaction to go through, it must be included in a block, and that block must be mined. To be safe, transactions are usually not considered complete until a few additional blocks are added to the blockchain. Because of this, Bitcoin transactions typically process on the order of hours. With Nano, each individual transaction is a block, and each block is able to be processed instantly by the network. The limit to the speed of the transactions is primarily network-bound; transactions are processed as fast as they can be propagated throughout the Nano network.

Bitcoin’s security is derived from hundreds of terawatts of computing power computing power computing hashes. In order to perform malicious actions, such as a double spend, on the Bitcoin blockchain, an attacker would have to accrue at least half of the network’s computation power, which is both financially and practically infeasible.

Nano secures it’s ledger via delegated proof of stake (dPoS). In order to perform malicious actions on the Nano block-lattice, an attacker would have to posses >50% of the online voting power. Such an attack would spoil their large financial investment, and as such not an attractive option. The dPoS of Nano consumes minimal energy, allowing full-nodes to run on inexpensive, low-power hardware.

*vs. IOTA*

IOTA’s consensus is decided by Proof of Work (PoW) stacking of consecutive transactions, while Nano’ is achieved by voting on conflicting transactions. PoW stacking requires maximizing the continuous network hash rate which is an expense that is inherently paid in electricity by users of the network. Because Nano doesn’t rely on high network PoW to maintain security, the operating cost of Nano nodes and Nano users are much lower.

While IOTA’s Tangle and Nano’ block-lattice are both DAG data-structures, offering instantaneous and feeless transactions, the way they operate are significantly different. With IOTA, two “tip” transaction must first be discovered via a probabilistic algorithm, such as a Monte Carlo Random Walk; a good tip is a recent transaction and expands the tangle in a “forward” moving direction. The idea is that if everyone uses similar tip selection algorithms, recent valid transactions will be approved by newer, valid transactions. Once a transaction is sufficiently deep in the Tangle, it is considered confirmed. Nano’ block-lattice is an organized structure that doesn’t require “tip” discovery. The last block on each account-chain is easily found/cached, and account transactions can only be appended, like a conventional blockchain. For typical transactions, this transaction is instantaneous and doesn’t require any additional blocks for a transaction to be considered confirmed.

IOTA’s vision is machine-to-machine communication, commerce, data storage and to become the premier protocol of IoT devices. Nano’ focus is on reliable, quick peer-to-peer payments and rapid exchange transfers for arbitrage.

*vs. Ethereum*

Ethereum is an alternative or separate technology from Nano. The entire concept of programs executing on top of the Ethereum Virtual Machine is something Nano doesn’t attempt to replicate. The part we focus on is an efficient transfer of value i.e. purely a currency, so while Ethereum requires miners and electricity input which is paid for by devaluing the currency, Nano has no fees and no devaluing while operating.
