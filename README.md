
# PCF - Pool Cool Fender

PCF enables free (or cheap) serverless WebRTC signalling bucket. 

The point is to allow people to deploy WebRTC-enabled applications without having to manage or worry (much) about a signalling server. Out of the box the library will "just work" using a free public worker (run by the author) that is subject to quota. However, is easy and takes just a few minutes. Once it is deployed, signalling will work without any further maintenance.

P2PCF also has some additional features:

- Room-based keying for easy connection management + acquisition
- Minimal initial signalling (1 or 2 signalling messages) using the technique [put together]
- Subsequent signalling over DataChannels
- Efficient chunking + delivery of DataChannel messages that exceed the ~16k limit
- Peers handed back from the API are [tiny-simple-peer] instances which provides a simple API for interacting with the underlying PeerConnections (adding + removing media tracks, etc.)
A basic chat + video sharing example demonstrates the library.

