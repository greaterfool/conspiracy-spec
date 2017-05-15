# Friends List
## Precis
This is the design document for how a friends list works in conspiracy, particularly in regard to DHT and discovery.

## Friend-to-Friend Discovery
This is essentially the equivalent of the "six-degrees of separation" theory, in technological form. Part of the discovery and DHT routing can be based on the principle that, if you're friends with someone, then whoever that person is friends with, is more likely to be friends with you. This assumption can be used to increase the speed of user discovery.

## The Issue With Hashing
In tox, friends can be added via their hash id. This works, but it's inconveient. Hashes are long, and difficult to remember, or share, outside of copying and pasting them to someone else.
