## ZK Demo:
A quick Demo, showcasing some ZK features

### Installation:
- run `curl -LSfs get.zokrat.es | sh`


### SHA256 Demo:
- We're going to create a zk program that calculates the SHA256 hash two given field elements
- The resulting proof can then be used to prove knpowledge of the premimage, without revealing it

#### compile
`zokrates compile -i sha.zok`

#### perform the setup phase
`zokrates setup`

#### execute the program
`zokrates compute-witness -a 2 4 6 8`

#### generate a proof of computation
`zokrates generate-proof`

#### export a solidity verifier
`zokrates export-verifier`

- visit `https://remix.ethereum.org/` and copy one of the contracts into the editor
- select Remix environment `Web3 Provider`
- select `Contract Verifier` as contract
