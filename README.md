# IPFSProxy

## Description

A smart contract that emits events from a list of consortium members to add and remove persistent IPFS hashes.
Consortium members agree to pin IPFS hashes in their respective IPFS instances

## Install requirements

``` $ npm install ```

## Run the proxylistener ( on the ropsten testnet - via docker )

```
$ cd docker 
$ docker build -t ipfs-proxy .
$ docker run ipfs-proxy
```


## Run the proxylistener ( on localhost - via truffle )

run a local IPFS node with the API enabled

``` $ ipfs daemon ```

start testRPC

``` $ testrpc```

run the contract migrations 

``` $ truffle migrate ```

run the proxylistener script

``` $ truffle exec scripts/proxylistener.js ```

Then add a hash to the contract by calling the addHash function , or just run this script in another window which does exactly that:

``` $ truffle exec scripts/addhash.js ```

You should see a hash getting pinned, and after the TTL get unpinned.

```

pinning hash QmTXUwTJtrUPAT3DppvHd5dvzRNzJPqwWQg6iWxvHhMuxX
pinned... QmTXUwTJtrUPAT3DppvHd5dvzRNzJPqwWQg6iWxvHhMuxX null [ 'QmTXUwTJtrUPAT3DppvHd5dvzRNzJPqwWQg6iWxvHhMuxX' ]
unpinned... [ 'QmTXUwTJtrUPAT3DppvHd5dvzRNzJPqwWQg6iWxvHhMuxX' ]

```

## Run the tests

start testRPC

``` $ testrpc```

In a seperate window , run the unit tests

``` $ truffle test ```

## Useful links

### IPFS API

https://github.com/ipfs/interface-ipfs-core#api





