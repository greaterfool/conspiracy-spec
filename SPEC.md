# conspiracy: Specification Doc
## Components/Functions
- DHT
- Crypto
- Message Transmission

## DHT
### Nearby Nodes
Standrd Node ID store, local based on Kademlia XOR routing.

### Friend Nodes & Routing
Friends in your "Friends List" become first choice for locating friends. In fact friend based routing is first choice for all routing, however the current design avoids announcing a users entire friends list for routing purposes in the interests of privacy.

The design is as such - user Alice is looking for user Charlie. Alice sends out a find request, to her only friend, Bob. What she sends is a friend request - which includes her Node ID. Bob uses XOR to determine the "closest" person in his friends list to Charlie. This continues down the line until Charlie is located. When it hits Charlie, the invitation stops there. Charlie now has the choise to add, or ignore. Once added, he sends a message back to Alice, using her Node ID, including his IP.

This setup allows for a little bit of extra privacy and safety as compared to Alice sending the inital frend request with her IP, in case the request happens to go to the wrong person, or any other kind of similar mistake.

## Reference Docs
- __DHT__:
    - [Kademlia DHT](https://pdos.csail.mit.edu/~petar/papers/maymounkov-kademlia-lncs.pdf)
    - [BitTorrent DHT](http://www.bittorrent.org/beps/bep_0005.html)
    - [Toxcore DHT](https://github.com/TokTok/c-toxcore/blob/master/docs/updates/DHT.md)
    - [Hydra (for consideration)](https://courses.csail.mit.edu/6.857/2015/files/athalye-gupta-yu.pdf)
