# documentation

## Ethereum RPC Node Archive Setup

Use ETH Docker to setup Ethereum clients with docker:

https://github.com/eth-educators/eth-docker

Setup with the following commands in Linux

```shell
git clone https://github.com/eth-educators/eth-docker
cd eth-docker
./ethd config
```

Expose RPC endpoints by modifying the .env file to have the following flag appended with `el-shared.yml` and `cl-shared.yml` (example with prysm and nethermind):
```shell
COMPOSE_FILE=prysm-cl-only.yml:nethermind.yml:el-shared.yml:cl-shared.yml
```

Then run:
```shell
./ethd up
```
See logs with:
```shell
docker compose logs -f
```
Consensus logs:
```shell
docker compose logs -f consensus
```
Execution logs:
```shell
docker compose logs -f execution
```

Source:

https://github.com/eth-educators/eth-docker/issues/1789#issuecomment-2028835211

## Consensus Layer Client Development Resources

### Prysm (Golang)

https://docs.prylabs.network/docs/contribute/contribution-guidelines

### Lighthouse (Rust)

https://lighthouse-book.sigmaprime.io/contributing.html

### Teku (Java)

https://github.com/Consensys/teku/blob/master/CONTRIBUTING.md

### Nimbus (Nim)

No contribution documentation.

### Lodestar (Typescript)

https://github.com/ChainSafe/lodestar/blob/unstable/CONTRIBUTING.md

### Prysm commands

https://docs.prylabs.network/docs/prysm-usage/parameters

## Delay Sync Conensus Clients

Ideally we delay the sync by 6 blocks to ensure transactions have settled over enough time to avoid potential Ethereum reorgs.

Details in Prysm issue:

https://github.com/prysmaticlabs/prysm/issues/13870

Idea 1:

Turn the ETH Docker containers on and off with a timer?

Idea 2:

Possibly done with the following clients:

### Prysm (Golang)

https://github.com/prysmaticlabs/prysm/compare/develop...MarcusWentz:prysm:delaySyncTest

### Lighthouse (Rust)

https://github.com/sigp/lighthouse/compare/stable...MarcusWentz:lighthouse:delaySyncTest

### Teku (Java)

https://github.com/Consensys/teku/compare/master...MarcusWentz:teku:delaySyncTest

### Nimbus (Nim)

https://github.com/status-im/nimbus-eth2/compare/stable...MarcusWentz:nimbus-eth2:delaySyncTest

### Lodestar (Typescript)

https://github.com/ChainSafe/lodestar/compare/unstable...MarcusWentz:lodestar:delaySyncTest
