# documentation

## Ethereum RPC Node Archive Setup

Use ETH Docker to setup Ethereum clients with docker:

https://github.com/eth-educators/eth-docker

## Delay Sync Conensus Clients

Ideally we delay the sync by 6 blocks to ensure transactions have settled over enough time to avoid potential Ethereum reorgs.

### Prysm

https://github.com/prysmaticlabs/prysm/compare/develop...MarcusWentz:prysm:delaySyncTest

### Lighthouse

https://github.com/sigp/lighthouse/compare/stable...MarcusWentz:lighthouse:delaySyncTest

### Teku

https://github.com/Consensys/teku/compare/master...MarcusWentz:teku:delaySyncTest

### Nimbus

https://github.com/status-im/nimbus-eth2/compare/stable...MarcusWentz:nimbus-eth2:delaySyncTest

### Lodestar

https://github.com/ChainSafe/lodestar/compare/unstable...MarcusWentz:lodestar:delaySyncTest
