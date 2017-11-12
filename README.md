![alt text](http://res.cloudinary.com/loristeeth/image/upload/v1510175135/tm_big_logo_wxtnbt.png "Bitcoin code vortex")
# Bitcoin Security Threat Model
### A security review of the Bitcoin cryptocurrency

---

## Motivation
The Bitcoin threat model is intended to help developers, investors and users better understand the security of Bitcoin. Threats are assumed to be any activity designed to prevent Bitcoin from accomplishing its mission to become cash (including a unit of account). Under each threat is a description of the threat, the safety features designed to protect against the threat, and any past examples of attacks executing the threat. Bitcoin can be attacked directly by making the software behave in a way that is ineffective as cash or by attacking the humans that are needed to support the software.

## Conclusion
Currently there are no threats that have been identified that could prevent or significantly slow adoption of Bitcoin as cash. However, new threats could be discovered or existing threats may prove to be more impactful. Given the impact Bitcoin is likely to have, and the frequency and intensity of past attacks, this remains a real possibility.

---

# Introduction
The Bitcoin threat model is intend to help
developers, investors and users
better understand the security of Bitcoin.
Threats are assumed to be any activity designed to
prevent Bitcoin from accomplishing its mission
to become cash (including a unit of account).
Under each threat is a description of the threat,
the safety features designed to protect against the threat,
and any past examples of attacks executing the threat.
Bitcoin can be attacked directly
by making the software behave in a way that is ineffective as cash
or by attacking the humans that are needed to support the software.

Threats are categorized as one of the following:
* ***Prevent Adoption*** - These threats have a reasonable chance of preventing Bitcoin from being adopted as cash.
* ***Significantly Slow Adoption*** - These threats have a reasonable chance of significantly slowing the adoption of Bitcoin as cash.
* ***No Impact on Adoption*** - These threats do not have a reasonable chance of significantly slowing the adoption of Bitcoin as cash.

Currently there are no threats that have been identified that could
prevent or significantly slow adoption of Bitcoin as cash.
However, new threats could be discovered or
existing threats may prove to be more impactful.
Given the impact Bitcoin is likely to have,
and the frequency and intensity of past attacks,
this remains a real possibility.

---

# Software Threats
Software threats are threats that
take advantage of security flaws within the software
to prevent Bitcoin from becoming cash.

## Creating a transaction
Owners of Bitcoin can send their Bitcoin to another user by
creating a digitally signed transaction
and broadcasting it to the Bitcoin network.
The piece of software that creates transactions is called a "wallet."
For a transaction to be accepted by the network it must be digitally signed
using the owners private key.
Keeping the private keys secret is also handled by the Bitcoin wallet software.

### An attacker could steal a users private keys to steal their bitcoin.
![alt text](https://user-images.githubusercontent.com/10575321/31319377-429ab034-ac30-11e7-96d0-d1526183ea18.jpg "Stolen Private Keys")

If an attacker can gain access to a users private key
he can send the associated bitcoin to himself.

***Safety Features***
* Because each Bitcoin user maintains his own private keys
an attacker can only steal from one person at a time.
This greatly reduces the incentive
for a attacker because in most centralized systems
such as banks, credit reporting agencies and brokerages
a successful attack could result in access to the funds of thousands of users.

* As long as thefts of private keys is not systemic
it will not prevent the adoption of Bitcoin as cash.
This is especially true as long as theft of private keys remains more
difficult than the theft government money.

* Hardware wallets are gaining in popularity and
they make theft of private keys nearly impossible
without physical access to the device and password or pin number.
This is a level of security that is
far higher than is common in banking.

***Past Attacks***
* Bitcoin owner has private keys stolen in 2011 when keeping private keys safe was much harder.
https://bitcointalk.org/index.php?topic=16457.msg214423#msg214423
* Bitcoin owners give away their private keys on Sheep (that is the name of the service).
https://www.theverge.com/2013/12/2/5167670/sheep-marketplace-bitcoin-heist-nets-at-least-5-million-owners-blamed
* Bitcoin owners give away their private keys on MtGox
https://www.wired.com/2014/03/bitcoin-exchange/

***No Impact on Adoption***
Although users need to be careful to
keep their private keys safe,
Bitcoin remains the most secure
digital asset.

---

### An attacker could use a quantum computer to guess everyone's private keys.
![alt text](https://user-images.githubusercontent.com/10575321/31319523-ca53f20e-ac32-11e7-9cd5-c915bbb22ee5.jpg "Stolen Private Keys")

If an attacker could gain access to everyone's private keys
he could steal every bitcoin.

***Safety Features***
* The private key is so large that it would take more energy
than is produced by the sun in its entire lifetime to power
a computer capable of guessing it.

***Past Attacks***
There have been no known attempts to perform this attack.

***No Impact on Adoption***
This attack is probably impossible.
It is very unlikely that quantum computing
or any other field of scientific research
will result in such a drastic rewriting
of our understanding of the basic laws of physics
that guessing private keys would become possible.

---

## Broadcasting a transaction to the network
After a transaction is created
it is relayed over the Bitcoin network.

### An attacker could broadcast a fake transaction to the network in order to steal bitcoins.
![alt text](https://user-images.githubusercontent.com/10575321/31319560-95fb70d0-ac33-11e7-89c3-3f4b28efee10.jpg "Stolen Private Keys")

If an attacker could convince the network that a transaction was legitimate
he could transfer bitcoins from a victims balance to his own account.

***Safety Features***
* The Bitcoin network will reject any transactions that are not
digitally signed by the private keys of the owner of the bitcoins.
* If a flaw in the digital signature mechanism is discovered
the Bitcoin network could consider any transactions
after the flaw was discovered to be invalid.
This would be far from ideal as some legitimate transactions
could be ignored,
but this possibility
reduces the incentives for attackers
to attempt this attack.
* Digital signatures are a fundamental building block of computer security
and have proven to be effective and secure in many applications
including Bitcoin.

***Past Attacks***
There have been no known attempts to perform this attack.

***No Impact on Adoption***
It is unlikely that a flaw will be discovered
that allows an attacker to forge a digital signature.

---

### An attacker could broadcast a large number of transactions that pay himself in order to clog the network.

Because anyone can broadcast a transaction on the Bitcoin network
it is possible for an attacker to broadcast a large number of transactions
that transfer bitcoins to themselves.
The Bitcoin network has no way to distinguish
between legitimate transactions and transactions
created with the intention of clogging the network.
If the network is unable to process legitimate transactions
Bitcoin would not be suitable as cash.

***Safety Features***
* Bitcoin transactions are processed in order of the fees
associated with the transaction.
This makes congesting the network with frivolous transactions costly.
* Layer two and side chain networks
allow Bitcoin transactions to be consolidated.
This decreases demand for space for transactions
making more room for both legitimate and frivolous transactions.
* Layer two and side chains technologies
allow Bitcoin transactions to be consolidated.
This increases the amount of fees that can be paid
for legitimate transactions since
each single transaction actually represents a batch of transactions.
This will make this attack more expensive
as frivolous transactions would have even more difficulty outbidding
legitimate transactions.
* Bitcoin limits the number of transactions that can be processed
using a "block size" limit.
This ensures that clogging the network would require competing
for space through fees.

***Past Attacks***
* Bitcoin spam attacks in 2015-2017
https://bravenewcoin.com/news/bitcoin-spam-attack-stressed-network-for-at-least-18-months-claims-software-developer/
* Bitcoin investor is fearful this will prevent Bitcoin from becoming cash
https://steemit.com/cryptocurrency/@superfreek/btc-spam-attack-200-000-unconfirmed-transactions-halts-bitcoin
* Bitcoin spam attack is used as support for attack 2.5.3.
https://bitcoinmagazine.com/articles/curious-case-bitcoins-moby-dick-spam-and-miners-confirmed-it/

***No Impact no Adoption***
Although this attack has been performed regularly in recent months
its only effect
has been occasional transaction delays and higher fees.
It has not significantly slowed adoption.
This is partially due to the fact that Bitcoin is so early in its
evolution to become money that it is still in the "store of value" stage
and partially because investors are aware that new features are on the way
that will make this attack impractical.

---

### An attacker could identify the participants in transactions through network traffic analysis
Bitcoin transactions are broadcast across the Internet by the sender.
If an attacker can view network traffic and discover the source and
destination of transactions this would make Bitcoin less suitable for cash.

***Safety Features***
* Bitcoin destination addresses are randomly generated
for each transaction
and not tied to an individuals identity.
* Bitcoin is an open source project with growing participation
and regular contributions from the top cryptographers
and software security experts.
It is likely that additional safety features will be added
to address this issue soon.
* Bitcoin transactions can be sent from anonymous networks
such as free wifi hotspots at coffee shops.
However this is still a major inconvenience
and it can still reveal the senders general location.

***Past Attacks***
* The NSA collects and stores all Internet traffic.
It is reasonable to assume all Bitcoin transactions are archived
and analyzed so that they are easily readable and tied to individuals.
Access to this data may currently be limited to the thousands of employees
and contractors that work for governments friendly to the US,
but it is likely that this data will be more broadly distributed through a leak
or hack if it hasn't been already.
https://www.theguardian.com/world/interactive/2013/jul/31/nsa-xkeyscore-program-full-presentation
https://en.wikipedia.org/wiki/XKeyscore

***No Impact on Adoption***
Bitcoin transactions can be tied to the senders by analyzing network traffic,
however unless Bitcoin transactions become less secure than government money
transactions this is unlikely to prevent Bitcoin from becoming cash.
It is also likely that additional safety features will be added
before this flaw has a significant impact on adoption.

---

### An attacker could identify the participants in a transaction through public transaction data.
Bitcoin transactions are published on the public ledger
and they contain the source, destination, approximate time and amount
of each transaction.
If it is possible for an attacker to discover
the people involved in a transaction
this would make Bitcoin less attractive as cash.

***Safety Features***
* Bitcoin destination addresses are randomly generated
for each transaction
and not tied to an individuals identity.
* Even with this fault, Bitcoin remains more secure
than government money transactions.
* Bitcoin is an open source project with growing participation
and regular contributions from the top cryptographers
and software security experts.
It is likely that additional safety features will be added
to address this issue soon.

***Past Attacks***
* Ross Ulbrict's transactions are traced by the FBI.
https://www.wired.com/2015/01/prosecutors-trace-13-4-million-bitcoins-silk-road-ulbrichts-laptop/

***Medium Risk***
Bitcoin transactions can be tied to the senders by analyzing the public ledger,
however unless Bitcoin transactions become less secure than government money
transactions this is unlikely to prevent Bitcoin from becoming cash.
It is also likely that additional safety features will be added
before this flaw has a significant impact on adoption.

---

## Confirming Bitcoin transactions
Bitcoin transactions are confirmed through a process called mining.
To prevent double spending of transactions they are grouped together
and a difficult math problem is solved using this set of transactions,
and the previous set of transactions,
as inputs.
Sets of transactions are called "blocks."
The math problem is so difficult that a significant amount of money,
must be spent on electricity in order to solve the problem.
The person that solves the math problem is rewarded with bitcoin,
in the form of transaction fees included by the senders of transactions,
and a "block reward" where additional bitcoins are created.
Solving this math problem is called "finding a block."
Everyone running mining software is
competing to be the first to find the next block.

### an attacker could run mining software in order to prevent transactions from being confirmed.
Because anyone is able to download and run the software
that confirms transactions on the Bitcoin network
it is possible for an attacker to mine blocks without including
transactions.

***Safety Features***
* Transactions include transaction fees.
If an attacker ignores these transactions,
he will not be able to collect the associated transaction fees.
* If an attacker ignores a transaction in a block,
it is likely that he will not be the miner that solves the next block
so he will have only succeeded in delaying the transaction
for a short period of time.
* In order to delay a transaction for a longer period of time
an attacker would need to dedicate more computing power to the network.
This would be expensive because he would
have to spend a lot of money on electricity and computer hardware
and his only reward would be in bitcoins
that would be less valuable as a result of his actions.
* The value of Bitcoin has been increasing rapidly since it was created.
Many individuals with the funding and knowledge to execute this attack
would gain more from investing in Bitcoin than from attacking it.
* Unlike other proof of work systems
the Bitcoin proof of work doesn't generate anything
desirable to the marketplace beyond securing the network.
This prevents attacks like these from being partially subsidized
through the sale of the other proof of work outputs.
* Bitcoin mining uses cutting edge chip design to produce
computer power as efficiently as humanly possible.
This means that an attacker could not easily develop more effective hardware
in order to make this attack more cost effective.
* This attack would increase fees.
Increased fees would incentivize others to mine
blocks with the transactions
and this would increase the cost of the attack.

***Past Attacks***
* Miners are creating blocks without any transactions.
https://bitcoinmagazine.com/articles/why-do-some-bitcoin-mining-pools-mine-empty-blocks-1468337739/

***No Impact on Adoption***
The only effect of this attack would be to increase fees
and fees are unlikely to go high enough
to significantly slow adoption
as investors anticipate that this
attack will be less effective in the future.

---

### An attacker could run mining software in order to double spend bitcoins.
Because anyone is able to download and run the software
that confirms transactions on the Bitcoin network
it is possible for a bad actor to mine blocks without including
transactions.

If the attacker sends bitcoin he could
delay that transaction until a new transaction,
using the same funds,
is confirmed by the network.
This would make the initial transaction invalid
after it was relayed across the network.

***Safety Features***
* The cost of executing this attack increases exponentially
as the transaction moves further back into the block history
because the Bitcoin network considers the longest (valid)
history to be correct.
* Many Bitcoin wallets don't display a transaction completely
finalized until it is at least 6 blocks old.
* Layer 2 technologies such as the lightning network
reduce this threat because transactions are confirmed instantly.
* Unlike other proof of work systems
the Bitcoin proof of work doesn't generate anything
desirable to the marketplace beyond securing the network.
This prevents attacks like these from being partially subsidized
through the sale of other proof of work outputs.

***No Impact on Adoption***
This attack is not cost effective.


---

### An attacker could exploit a flaw in the proof of work algorithm to fake the performance of work.
If an attacker is able to find a flaw in the proof of work algorithm
he could obtain the benefits of transaction fees and block rewards
without doing the work required to secure the Bitcoin network.

***Safety Features***
* The proof or work algorithm is based on the SHA-256 hash algorithm.
This algorithm has been in use for over a decade and is critical to
most digital security applications
and it is believed to be secure.
* The Bitcoin proof of work has been in use on the Bitcoin network
for over 8 years and
the only flaw uncovered to date
only allowed the attacker to fake ~20% of his work.

***Past attacks***
* Attackers discover a way to fake work.
https://www.asicboost.com/

***No Impact on Adoption***
Although past attacks have been successful
they were a result of a known design flaw (transaction malleability)
that has been fixed.

---

### An attacker could steal all of the hardware used to confirm Bitcoin transactions.
If an attacker could gain control of all of the hardware used to confirm Bitcoin
transactions he could prevent some or all Bitcoin transactions.

***Safety Features***

* Bitcoin mining is decentralized.
Mining computers are located in many geographic areas
that are under the control of various criminal organizations
that are hostile to one another.
Even if all mining hardware could be found,
coordination between hostile groups,
that may see Bitcoin as a lesser threat to their interests than to their rivals,
seems unlikely.
* The Bitcoin protocol was designed to
keep incentives for mining in a single location
as small as possible.
For example the delay between a miner finding a block
and the rest of the miners knowing about this discovery
is short.
* Miners are, to some degree, aware of this threat.
This encourages miners to remain anonymous and
keep their locations secret.
If this attack is attempted this awareness
will be greatly increased.

---

### An attacker could claim to be Satoshi and remove a safety feature from the next version of Bitcoin.
Satoshi Nakamoto is the name of the author of the original Bitcoin
white paper and software.
Because he is so well respected in the Bitcoin community he,
or someone pretending to be him,
could attempt to remove a security feature in the next version of Bitcoin.

***Safety Features***

* Satoshi Nakamoto disappeared from the Bitcoin community years ago.
Since that time many well respected developers and security researchers
have become experts in Bitcoin and the design and implementation decisions
that keep it secure. Convincing the best security researchers in the world
to remove a safety feature in Bitcoin would not be easy,
even by someone with the reputation of Satoshi.
* Impersonating Satoshi is difficult because he retains ownership of
bitcoin balances. Anyone claiming to be Satoshi should be able to provide
proof of his identity by sending those bitcoins.
* In some debates people have attempted to use Satoshi's vision,
or intention as support for their position.
In these cases an appeal to the authority of Satoshi has generally
undermined the argument because it distracts
from the technical advantages and disadvantages
of a given design or implementation decision.

***Past Attacks***
* Craig Wright impersonates Satoshi in order to remove the block size limit.
https://dankaminsky.com/2016/05/02/validating-satoshi-or-not/


---

### An attacker could remove a safety feature from the next version of Bitcoin to enable a new capability.
In all software projects there is a tension between adding new
features or capabilities and maintaining safety features.
This is often exacerbated by the fact that safety features often prevent
software from being used certain desirable ways.
As an example cars have speed limiters
to prevent a car from driving as fast as the engine will allow
but it does prevent users from racing at top speed.

Even in the most effective software projects
the security vs features trade off decisions
become heated and political.
If an attacker is able to convince the community that a new feature
is more important than an existing safety feature,
the safety feature would be removed.

***Safety Features***
* The Bitcoin technical community has the best software security experts
working diligently to keep Bitcoin secure.
* Because the Bitcoin software is currently securing over 60 Billion USD
in value the technical community is slaw to make changes that could
introduce security vulnerabilities.
* Side chains allow new features to be developed and deployed
using bitcoin as the asset,
without changing the Bitcoin network or protocol.
It is likely that any significant change in the future
will be deployed onto a side chain before those features
are included into Bitcoin itself.

***Past Attacks***
* Segwit 2x attempts to remove the block size limit safety feature.
https://medium.com/@jimmysong/segwit2x-what-you-need-to-know-about-the-2mb-hard-fork-27749e1544ce
* Bitcoin XT attempts to remove the block size limit safety feature.
https://medium.com/faith-and-future/why-is-bitcoin-forking-d647312d22c1
* Bitcoin Classic attempts to remove the block size limit safety feature.
https://bitcoinclassic.com/

***No Impact to Adoption***
This attack is unlikely to be successful.

---

### An attacker could create a copy of Bitcoin (aka fork) that is missing a safety feature and trick people into using it.
Because Bitcoin is an open source project anyone can copy the code
and build their own version of Bitcoin.
If they can convince someone that their version of Bitcoin is
the real Bitcoin they will have successfully removed
that safety for those users.

***Safety Features***
* If investors are deceived into using a version of Bitcoin that
lacks the safety features of Bitcoin that does not reduce the security of Bitcoin.
* While siphoning off investors from Bitcoin would delay Bitcoin
from becoming money in the near term,
it would accelerate the education of investors regarding
the safety features of the real Bitcoin
and this would accelerate Bitcoin becoming cash.
* Side chains allow new versions of Bitcoin to be created while still
using Bitcoin as an asset.
New versions of Bitcoin will likely be tested as a side chain before
those features are implemented into the original Bitcoin.
This would give people more time to understand any changes being proposed.
* It would be very difficult to promote a version of Bitcoin
without the Bitcoin community exposing the attempt as an attack.
* While it is still possible some investors would be deceived
they would almost certainly understand there is a significant controversy
and if they made the wrong choice they would be more immune
to this attack in the future.
* By it very nature this attack involves
creating a new digital asset
that doesn't work as well as Bitcoin as cash.
This fact will eventually become clear to all investors
making this attack ineffective over time.

***Past Attacks***
* Bitcoin Cash attempts to remove the block size limit safety feature.
https://web.archive.org/web/20170928124716/https://www.bitcoincash.org/

***No Impact to Adoption***
This threat is unlikely to impact adoption. The Bitcoin Cash fork
attack was well funded and benefited from a major design flaw in Bitcoin
(transaction malleability) that has now been fixed
and a method for deploying controversial changes (miner signaling)
that is unlikely to be used in the future and it still had negligible
effect on the adoption of Bitcoin.

---

### An attacker could create a variety of implementations of Bitcoin in order to add a security flaw.
If an attacker is able to create a new implementation
of the Bitcoin software that
is not thoroughly reviewed by
Bitcoin security experts he could
introduce a subtle security flaw that
is not discovered before it is deployed.

Currently the vast majority of expertise
is focused on a single repository and this
makes it very difficult for a flaw to go undiscovered.

If an attacker could create one or more
Bitcoin implementations of Bitcoin it would at minimum
spread out the efforts of security experts
and at most prevent some implementations from being
reviewed before deployment.

***Safety Features***
* The Bitcoin development community is aware of this attack
and has been very vocal about the need to prevent it.
* Bitcoin development is very difficult and
it would be difficult to recruit competent developers
to participate in this attack.
* The Bitcoin development community does
review other implementations and has offered
security fixes both to protect Bitcoin and
to expose the poor quality of some implementations
before they are adopted by the unwitting.

***Past Attacks***
* Bitcoin Unlimited contained security flaws that would have been caught in code review.
https://bitcoinmagazine.com/articles/security-researcher-found-bug-knocked-out-bitcoin-unlimited/
* Bitcoin ABC contained security flaw that would have been caught in code review.
https://reviews.bitcoinabc.org/rABCb7d5bda29c07cd80c900e3ddd6a9a37a2b23f347
* Bitcoin XT contained a security flaw that could have been cough in code review.
https://www.reddit.com/r/bitcoinxt/comments/43lty6/current_bitcoin_xt_contains_a_network_splitting/

---

## Observing confirmed transactions
In order for a transaction to be completed the receiver
must be confident the transaction has been irreversibly confirmed
by the Bitcoin network.
this is performed by Bitcoin "node" software.
This software maintains a copy of the longest set of transactions
presented to it that are valid.
The node software considers a transaction valid if it is structured correctly,
digitally signed by the bitcoin owner,
and does not attempt to transfer more bitcoin than is available to the sender.
Some Bitcoin wallets do not contain the node software,
but instead connect to a remote node to confirm that a transaction is completed.
This is called an SPV (Simple Payment Verification) wallet.

### An attacker could create a less secure digital asset and trick people into buying it.
If an attacker can trick investors into using his digital asset as cash it could prevent Bitcoin
from becoming cash (unit of account).

***Safety Features***
* If a digital asset is less secure than Bitcoin
it is also less suitable as cash.
Eventually this reality will be
understood by investors and they will
abandon the less secure coin.
* Many members of the Bitcoin community
are technically literate
and obsessed by the technology
and the incentive structure that makes Bitcoin secure.
* No criminal organizations in the world
have been successful at keeping security flaws secret.
* Digital assets contain the greatest rewards
for identifying security flaws. Security researchers and
hackers are highly incentivized to find every security flaw.
* Effort spent on promoting flawed digital assets
is most effective when targeting
people that are new to the technology
because existing members of the community
are more difficult to deceive.
The net effect of this attack is to
educate people of the value of Bitcoin.

***Past Attacks***
* Ethereum has no maximum limit of Ether and no built in difficulty adjustment.
https://github.com/ethereum/wiki/wiki/White-Paper
* Ripple does not use proof of work and requires trusted "validators."
https://ripple.com/consensus-whitepaper/
* Bitcoin cash removed the block size safety feature
https://www.bitcoincash.org/
* Litecoin removed the cutting edge chip design safety feature.
https://litecoin.info/

***No Impact on Adoption***
Although the market cap falsely indicates otherwise,
Bitcoin adoption has not been slowed by past attacks
and likely has been accelerated.

---

### An attacker could create a more secure digital asset so that investors will abandon Bitcoin.
If an attacker could create a more secure digital asset investors
would abandon Bitcoin and adopt this new asset as cash.

***Safety Features***
* The vast majority of cryptography experts
are working on Bitcoin.
* As an open source project Bitcoin is able
to incorporate any advances discovered in other projects.
* Digital assets benefit from "network effects" for adoption.
A new Digital asset would be starting at a great disadvantage
in this regard.
* Crypto-currencies require proof of work
to secure the network.
Bitcoin has the greatest amount of work
by several orders of magnitude.
* If a new digital asset is more secure
and honors past Bitcoin transactions
it would, be an upgrade to Bitcoin,
not a competitor of Bitcoin.

***Past Attacks***
This attack would result in improved Bitcoin security.
It is not really an attack when properly understood.

***No Impact on Adoption***
This attack would result in improved Bitcoin security.
It is not really an attack when properly understood.

---

### An attacker could mine invalid Bitcoin blocks to remove a safety feature from Bitcoin
If an attacker could make the network accept blocks
that don't include a safety feature
he would have effectively removed that safety feature.

***Safety Feature***
* The Bitcoin network enforces the rules
that include safety features
on every Bitcoin node, miner and wallet.
As a result blocks mined without the safety feature
will simply be ignored by the Bitcoin network.

***Past Attacks***
* Segwit 2x
https://medium.com/@jimmysong/segwit2x-what-you-need-to-know-about-the-2mb-hard-fork-27749e1544ce

***No Impact on Adoption***
This attack is not effective,
but it could be used to support
a misinformation campaign,
a fork to remove a safety feature,
or a new digital asset that is missing a safety feature.

---

### An attacker could deceive a Bitcoin node into thinking a transaction did or did not get confirmed.
Because Bitcoin nodes accept information from any other computer
running the Bitcoin node software it is possible to provide
a node or a group of nodes
false information about the current state of a transaction.

***Safety Features***
* Bitcoin nodes form a peer-to-peer network and obtain copies of transactions
from multiple nodes. An attacker would need to prevent a node
from communicating with all innocent nodes in order for this attack to be successful.
* In order to provide a set of false transactions
that appear valid the attacker would need to perform
the proof of work required by the current network difficulty
making this attack expensive.
* As soon as a node discovers that a longer block chain exists
with valid transactions it immediately accepts this new set of transactions
as correct and discards its previous set of transactions.
* Satellite connections allow nodes to download a copy of the block chain
even if they are using an Internet connection that keeps them ignorant
of a longer valid chain of transactions.
* If a node owner is concerned that he may be the victim of a network split attack
he could wait until he receives physical media containing the longest block
from another physical location.
* Absolute censorship is difficult for a short period of time and nearly impossible,
for a longer period of time,
as evidenced by the Chinese governments serious, yet ineffective, efforts to censor the Internet.
* In many ways this is not an attack on Bitcoin directly,
but an attack on the Internet itself.
Building a secure Internet is becoming more and more important
and there are several efforts underway to accomplish this goal.
As Bitcoin and other digital assets become more important the motivation
to create a secure Internet will grow.
* In order to make this attack more cost effective more nodes would need
to be deceived at the same time.
However, the more nodes are deceived into trusting an invalid chain of transactions
the more likely it becomes that the victims become aware of the attack
and stop trusting their node software.

---

### An attacker could deceive a Bitcoin partial node (SPV client) into thinking a transaction did or did not get confirmed by the Bitcoin network.

In some cases, such as operating on a mobile phone,
the Bitcoin client software can't perform the full validation
of the Bitcoin transaction history.
To the degree that the client doesn't perform complete validation
safety features are discarded.

* Bitcoin client software that doesn't perform
complete validation of the Bitcoin transaction history
often connects to another computer that it trusts to perform
this full validation on its behalf. While this is not ideal,
because an attacker could pretend to be this trusted computer,
it does provide greater security than outright skipping validation.
* The Bitcoin community encourages users to run a full node,
especially when acting as a merchant,
or accepting large amounts of Bitcoin from untrusted parties.
* In order for this vulnerability to effective Bitcoin as a whole
attacks would need to become systemic and this would likely result
in the awareness required to encourage full nodes.

### An attacker could introduce security flaws into Bitcoin mining hardware in order to break the security of Bitcoin.
If an attacker included a "back door" in mining hardware
before it was shipped to the buyer
he could gain control of the majority of the Bitcoin computing power.

***Safety Features***
* The Bitcoin network is not effected by the specific owners of mining
hardware. The attacker would be as legitimate a Bitcoin miner
as the previous owners before control of the hardware was stolen.
* As the new "owner" of Bitcoin hardware
he would be equally as incentivized to
use these resources to secure the Bitcoin network
as the rightful owners.
* Once the physical owners of hardware discovered the hardware was
not behaving according to their wishes
they would remove the security flaw.

***Past Attacks***
* Bitmain, the most popular mining hardware manufacturer, includes a backdoor.
http://www.antbleed.com/

***No Impact to Adoption***
Even if successful this attack would probably have no effect on the Bitcoin network.

---

# Human Threats
Bitcoin can be attacked by attacking
the humans that support the Bitcoin software as network operators,
investors, merchants, developers or hardware manufacturers.

## Network Operators
People that run the software needed to support Bitcoin can be attacked.

### An attacker could threaten to harm an individual or group mining bitcoin.
Bitcoin mining is a critical part of the Bitcoin network.
Without functioning mining software no new Bitcoin transactions could be trusted.

***Safety Features***

* Bitcoin mining can be done anonymously. In the most extreme case
a Bitcoin miner could obtain new transactions and distribute discovered blocks
via sneaker net. Before this extreme however Bitcoin miners could use
anonymizing technology such as VPNs or Tor.
* Bitcoin mining is decentralized. No single person controls all of the Bitcoin
mining computer power and Bitcoin mining equipment is distributed across the globe.
* Even if a large miner was intimidated into action there is little damage he could
do to the Bitcoin network.
Double spending is not cost effective.
Delaying specific transactions would have limited effect.
He could not create invalid bitcoins or steal bitcoins.
* An attacker that intimidates a miner has effectively stolen the mining equipment
and would be best served by mining bitcoins for profit and securing the network.

***No Impact to Adoption***
Although the attack is possible it is unlikely that it would succeed in disrupting
the Bitcoin network for any significant period of time.


---

### An attacker could threaten to harm node individual or group running a Bitcoin node
Bitcoin nodes are critical to the Bitcoin network.
Without a network of functioning nodes new transactions could not be relayed.

***Safety Features***
* Nodes simply validate and relay transactions.
Even if a node operator was intimidated into action he could at most slightly delay
the relay of traffic and deceive any partial nodes that trusted him to validate transactions
(not a best practice for significant transactions).
* Nodes can be operated anonymously. In the most extreme example node operators
could run software on computers not owned by them.
* Nodes could download all new transactions using Satellite connections
and transmit new transactions hidden inside pictures and using burner phones.
* Nodes could use anonymizing technology such as VPNs or Tor to hide their
physical location.
* Peer to peer networks such, as BitTorrent and Bitcoin, have proven
extremely difficult, if not impossible, to shut down.
This is in spite of the fact that well funded industries and governments
have attempted to shut them down in the past.

***No Impact to Adoption***
Although the attack is possible it is unlikely that it would succeed in disrupting
the Bitcoin network for any significant period of time.

---

## Investors
Without Investors Bitcoin would have no market value
and be unsuitable as cash.

### An attacker could extort the private keys from an investor.
An attacker could threaten to harm a Bitcoin investor
unless he handed over the private keys to his bitcoin holdings.

***Safety Features***
* Many Bitcoin investors are anonymous making extortion difficult.
* Bitcoin investors have unknown balances making
extorting all of the bitcoin held by an investor difficult.
* Even if this became a common problem for Bitcoin investors
it would not be a threat to Bitcoin becoming money unless
it was easier to extort a Bitcoin investor than an investor
in government money.
* Many Bitcoin wallets make it easy to create false bitcoin
balances making it appear that they have been emptied by an
attacker when bitcoin holdings remain.
* Public advocates of Bitcoin are often careful to own
only a small amount of bitcoin because they are security experts
and very aware of this threat.
* Bitcoin allows multi signature addresses that would require an attacker
to extort multiple people, simultaneously, in order to steal bitcoin
* Criminal organizations are comprised of acting individuals.
Senior decision makers would gain greater personal benefits
by becoming investors in Bitcoin
than attempting to prop up its organization's competing cash.

***No Impact to Adoption***
While the threat to an individual investor may be high
Bitcoin offers more investor security than the assets it competes with
so it is unlikely that extorted private keys will prevent Bitcoin from becoming money.

---

### An attacker could deceive investors regarding the utility of Bitcoin.
If investors were tricked into believing Bitcoin is less useful as money
than another asset they would sell. If this could be achieved at sufficient scale
Bitcoin would not become cash.

***Safety Features***
* To the extent that this attack is only partially successful
it would inoculate investors to future deception.
* This attack would be impossible to maintain for a long period of time.
* Access to information has been increasing at a rapid rate
for the last 50 years and it seems unlikely that this trend will reverse.

***Past Attacks***

* False story that the "Bitcoin network" was hacked.
https://www.wired.com/2014/03/bitcoin-exchange/
* False story that Bitcoin can't become cash because its supply is limited.
https://www.theatlantic.com/business/archive/2013/12/why-bitcoin-will-never-be-a-currency-in-2-charts/282364/
* False story that Bitcoin can't become cash because its price is *currently* volatile.
http://www.businessinsider.com/goldman-completely-debunks-all-the-arguments-for-bitcoin-2014-3
* Head of JP Morgan says Bitcoin is a fraud and can be shut down by governments.
https://www.bloomberg.com/news/articles/2017-09-12/jpmorgan-s-ceo-says-he-d-fire-traders-who-bet-on-fraud-bitcoin

***No Impact to Adoption***
In spite of the fact that
these attacks have been constant and well funded,
Bitcoin adoption has been rapid and
has arguably been faster than the technical advancements,
needed for Bitcoin to become cash.

---

### An attacker could threaten to harm Bitcoin investors if they don't sell or hand over their bitcoin.
This is a duplicate of the threat:
An attacker could extort the private keys from an investor.
Using the threat of violence to force someone to hand over their private
keys is essentially the same attack.
The only difference is that this attack may be more likely to be attempted
by larger criminal organization that have violent control over
a population within a specific geography,
whereas the other attack may be more likely to be attempted
by individual criminals or smaller criminal organizations,
but the safety features and the technical nature of the attack is identical.

### An attacker could threaten to harm anyone that attempts to buy or sell bitcoin.

If an attacker can make it impossible to buy or sell bitcoin
he wouldn't have to force existing investors to sell or hand over bitcoin
because an asset that can't be sold can't become money.

***Safety Features***
* As more of the world savings moves into digital assets
this becomes a more difficult attack
because digital assets can more easily be exchanged for one another anonymously.
* It is possible to buy and sell bitcoin anonymously through decentralized exchanges.
In these exchanges the buyer can send cash through the mail and the seller can
send bitcoin after the payment is received.
The buyer relies on the reputation of the seller,
including the number of previously successful sales,
to avoid being ripped off.
Millions of dollars in these type of Bitcoin transactions are executed daily
at the time of this writing.
* As the threat of violence in commerce becomes a greater issue
the utility of Bitcoin becomes more obvious.
This could backfire on the attacker and accelerate the move from assets,
such as physical cash, bank account balances, centrally controlled stocks and bonds,
and precious metals into bitcoin because it is more difficult to steal.
* As the number of people that own bitcoin increases
the more a given population would resist this attack.
* Some assets are more valuable specifically because they
represent rebellion or resistance to the threat of violence.
This could increase interest in Bitcoin in areas where it is
prohibited by a corrupt government or other criminal organization.

***No Impact to Adoption***
Even the announcement that China,
previously thought to be one of the most important regions for Bitcoin,
will ban all Bitcoin transactions merely caused
transactions to move to decentralized exchanges.

***Past Attacks***
* China ban's Bitcoin exchanges.
https://www.theverge.com/2017/9/18/16326078/chinese-regulators-ban-cryptocurrency-platforms-bitcoin

---

## Bitcoin Merchants
In order for Bitcoin to become electronic cash
(including a unit of account)
merchants, that sell goods or services,
must accept bitcoin for payment.
If an attacker can prevent merchants from accepting bitcoin
he would prevent Bitcoin from becoming cash.

### An attacker could threaten to harm anyone accepting bitcoin as payment.
An attacker could threaten merchants with direct violence
or they could tell merchants that they must perform free labor
or pay money,
if they accept bitcoin in order to prevent Bitcoin from
becoming cash (including the unit of account).

***Safety Features***
* Bitcoin transactions, like paper cash transactions, are difficult for governments to tax.
This provides significant financial incentive for merchants to accept bitcoins secretly
and to provide a "regular price" and a "bitcoin or cash price."
In the USA this "cash price" is often 20% - 30% lower
because sales tax, income tax, and payroll taxes to the business owner
can easily exceed 60%.
This means that the merchant is paid an additional 30% as compensation for the risk involved
in making a "secret transaction."
* Attackers are aware that as they increase the cost of "in the open" transactions
they increase the benefits of secret transactions.
This makes these type of attacks risky as they could result in the loss
of existing avenues of extortion.

***Medium Risk***
Although it is unlikely this attack could prevent Bitcoin from
becoming cash it could possibly slow adoption.

***Past Attacks***
* US Government requires capital gain tax calculation on every $1 cup of coffee transaction.
https://www.thebalance.com/how-bitcoins-are-taxed-3192871

---

## Bitcoin Developers
Bitcoin developers are critical for the continued improvement of Bitcoin software.
Without Bitcoin developers the Bitcoin code
would not be improved and could become unusable if vulnerabilities discovered in the future
are not repaired.

### An attacker could threaten to harm anyone contributing to Bitcoin software.
If an attacker could convince developers that contributing to Bitcoin
is likely to result in their death or kidnapping it is possible
that Bitcoin would fail to become cash.

***Safety Features***
* Bitcoin development can be done anonymously.
In fact the original white paper author
and first Bitcoin developer,
known as Satoshi Nakamoto,
has an identity that remains unknown.
* Bitcoin is the result of over 30 years of research and development
by the cypher punk community. This community has included the very best
software security researchers and cryptographers that have invested
the most basic building block of Internet and computer security (Public
Key Cryptography). If any group could operate anonymously,
and effectively,
it would be this community.
* If a security researcher that is part of a criminal organization
discovered a way to significantly improve Bitcoin
the best way to profit from this knowledge would be
to purchase a large amount of Bitcoin on margin
and then anonymously publish the code.
The market price of Bitcoin would increase and he would
make a large amount of money.
In this way, even well funded organizations that wish to destroy Bitcoin development
would likely end up funding improvements through "reverse-corruption."
* There are a large and growing number of Bitcoin developers.

***Past Attacks***
* Satoshi stopped contributing to Bitcoin out of fear of harm.
https://bitcointalk.org/index.php?topic=1813452.0
* Tim May left the cypherpunk mailing out of fear of the US Government after 9/11.
https://www.youtube.com/watch?v=TdmpAy1hI8g&t=2654s (42:30)

***No Impact to Adoption***
Given the roots of the Bitcoin development community it is unlikely that this attack would be successful.

---

### An attacker could bribe or extort a Bitcoin developer into introducing a security flaw into Bitcoin.
If an attacker could get flawed code into the next version of Bitcoin he could destroy
the features of Bitcoin that make it useful as money.

***Safety Features***
* Bitcoin code reviewed by hundreds of software security experts before any change is introduced.
It would be very hard to construct a change that contained a security flaw that wouldn't be noticed
by the Bitcoin community at large.
* The Bitcoin community is very risk averse.
It is aware that the success of Bitcoin would result in the destruction,
or at least a drastic reduction in funding,
of many monopolies and other criminal organizations.
As a result it is hyper vigilant regarding code changes.
* Side chains will allow new features to be tested with
millions or billions of dollars worth of bitcoin
before exposing all of Bitcoin to the risk associated with any new feature or change.
As more money is available for an attacker, without being a threat to the core Bitcoin network,
the more unlikely it is that a flaw will remain undiscovered until it is implemented in Bitcoin.
* A Bitcoin developer will only have one chance to introduce a flaw if he is caught as his
credibility will be destroyed.

***Past Attacks***
* Mike Hearn attempts to remove block limit safety feature
https://blog.plan99.net/the-resolution-of-the-bitcoin-experiment-dabb30201f7
* Gavin Andresen attempts to remove block limit safety feature
https://www.coingecko.com/buzz/gavin-andresen-unlimited-block-size-fine

***No Impact to Adoption***
Although it appears this attack has been attempted
more than once in recent years
no security flaws have been introduced to Bitcoin.

---

## Bitcoin Hardware Manufacturers
Bitcoin hardware manufactures produce hardware for mining.
This mining hardware is critical for confirming Bitcoin transactions.

### An attacker could threaten to harm Bitcoin mining hardware manufacturers if they sell to the public.
If cutting edge Bitcoin mining hardware was no longer available
it would make confirming transactions less secure.
This could reduce the security of Bitcoin enough to prevent it from becoming cash.

***Safety Features***
* Mining hardware makes confirming transactions more efficient,
but this action may motivate the Bitcoin community enough
to overcompensate for the loss of efficiency using less efficient hardware.
* There are currently more than one mining hardware manufacturer based in more than one
geographic region.
And it seems likely that more competition in the mining hardware space will result
in more manufacturers over time. This would make this attack more difficult over time.
* As the amount of computing power decreases on the network the rewards for operating
mining hardware increases.
If this attack was executed it would make Bitcoin mining more profitable
and this would attract additional manufacturers and mining operators.

***Past Attacks***
No past attacks have been disclosed.

***No Impact on Adoption***
It is unlikely this attack would significantly slow adoption.

---












