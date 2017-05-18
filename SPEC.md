# conspiracy Specification
## Components/Functions
- DHT
- Crypto
- Message Transmission

## DHT
### Nearby Nodes
Standrd Node ID store, local based on Kademlia XOR routing.

### Friend Nodes & Routing
**Explanation by way of example:** Alice wants to talk to Charlie. Alice sends out the request To Bob, person in her friends list, who XORs closest to Charlie. If he does not know Charlie, he sends the request in turn to the closest XOR contact he knows.
*Note: Is this necessary? Does it have any real benefits over regular XOR routing?*


## Reference Docs
- __DHT__:
    - [Kademlia DHT](https://pdos.csail.mit.edu/~petar/papers/maymounkov-kademlia-lncs.pdf)
    - [BitTorrent DHT](http://www.bittorrent.org/beps/bep_0005.html)
    - [Toxcore DHT](https://github.com/TokTok/c-toxcore/blob/master/docs/updates/DHT.md)
    - [Hydra (for consideration)](https://courses.csail.mit.edu/6.857/2015/files/athalye-gupta-yu.pdf)
    - [SAFE Network - XOR Routing](http://ericklavoie.com/talks/safenetwork/1-xor-routing.pdf)

