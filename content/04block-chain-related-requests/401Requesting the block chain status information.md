---
title: 'Requesting the block chain status information'
weight: 401
---

 
## Requesting the block chain status information 
### Block chain height 
| API path: | Request type:  |
|------|------|
| /chain/height | GET|

 
**Description:**
 
Gets the current height of the block chain.

 
**No parameter:**
 
**Example:**
 
`http://127.0.0.1:7890/chain/height`
 
**Example of returned JSON object:**

`(no. 19) `

>    (no. 19) Example of returned JSON object:

 
```json
       {
        "height": 42799
        }
``` 
**Possible Errors:**
 
None.

 
### Block chain score 
| API path: | Request type:  |
|------|------|
| /chain/score | GET|

 
**Description:**
 
Gets the current score of the block chain. The higher the score, the better the chain. During synchronization, nodes try to get the best block chain in the network.

 
**No parameter:**
 
**Example:**
 
`http://127.0.0.1:7890/chain/score`
 
**Example of returned JSON object:**

`(no. 20) `

>    (no. 20) Example of returned JSON object:

 
```json
       {
        "score": "18722d5a7d590deb"
        }
``` 
**Possible Errors:**
 
None.

 
### Last block of the block chain score 
| API path: | Request type:  |
|------|------|
| /chain/last-block | GET|

 
**Description:**
 
Gets the current last block of the chain.

 
**No parameter:**
 
**Example:**
 
`http://127.0.0.1:7890/chain/last-block`
 
**Example of returned JSON object (main network):**

`(no. 21) `

>    (no. 21) Example of returned JSON object (main network):

 
```json
       {
        "timeStamp": 9232968,
        "signature": "0a1351ef3e9b19c601e804a6d329c9ade662051d1da2c12c3aec9934353e421c79de7d8e59b127a8ca9b9d764e3ca67daefcf1952f71bc36f747c8a738036b05",
        "prevBlockHash": {
        "data": "58efa578aea719b644e8d7c731852bb26d8505257e03a897c8102e8c894a99d6"
        },
        "type": 1,
        "transactions": [
        ],
        "version": 1744830465,
        "signer": "2afca04d2cb8d16cf3656274bc55b95e60be823cfb7230d82f791ed42a309ee7",
        "height": 42804
        }
``` 
**Possible Errors:**
 
None.

 
