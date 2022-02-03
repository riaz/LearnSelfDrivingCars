Features of HD Maps
====================

1. Accurate 3D representation of Road Network

2. Location of sign posts, lane boundries, bike lanes,parking lans in cm precision.

3. Semantic Info [Speed Limit of Road, What each light of signal means, Where the left turn begins, Other traffic signals]

4. Precision [Prime purpose of HD Maps]


### Flow: [Localization/Perception/Planning]

Once we have a HD map , we need to localize ourself wrt. to that map to navigate well and be aware we are.

To locate ourself, the vehicle tries to localize itself using data obtained from sensors [preprocessong/co-ordinate transform/data fusion]

The localization process needs HD maps and is a critical component of a SDC platform.

Ref: Apollo HD Maps Module
https://github.com/ApolloAuto/apollo/tree/master/modules/map

Apollo uses OpenDrive format [industry wide mapping standard]

Applo relies on crowd-sourcing HD maps generation.


