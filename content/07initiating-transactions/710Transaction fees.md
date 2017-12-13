---
title: 'Transaction fees'
weight: 710
---

 
## Transaction fees 
In order for the harvesters to have an incentive to run a node that is harvesting blocks, users have to pay a fee for every transaction that is going to be included in a block chain.

 
Different transaction types have different fees. In order to get a transaction validated by a NIS, the fee provided must be at least the minimum fee.

 
**Note:** Depending on the transaction type there could be additional fees due to the action during transaction execution (e.g. renting a namespace)

 
The following summarizes the minimum fees for each transaction type. All calculation are done with rounded amounts of XEM (i.e. micro XEM are ignored):

 
###  Message Transfer transactions: 
**a) messages:**

 
0.05 xem per commenced 32 message bytes = 0.05*(Rounddown(messageLength / 32,0) + 1). If there is no message, then the message fee is 0 XEM

 
Example: `message length of 48 bytes has 0.1 xem fee.`

 
**b) XEM transfer:**

 
0.05 xem per rounddown(10,000) xem transferred, capped at 1.25 xem. Minimum transfer fee is 0.05 XEM, i.e., 0.05 XEM for transfer 

 
Example: `0.2 xem fee for a 45,000 xem transfer, 1.25 xem for a 500,000 xem transfer.`

 
**c) mosaic transfers:**

 
i) mosaics with divisibility of 0 and a maxmimum supply of 10,000 are called small business mosaics. 0.05 xem fee for any transfer of a small business mosaic.

 
ii) for other mosaics as before the same formula is applied to calculate the xem equivalent, then the fee for transferring xem is applied. Call that fee xemFee. To take into account the total quantities for different mosaics, an adjustment term is calculated. For a mosaic called m calculate

 
maxMosaicQuantity = 9,000,000,000,000,000 - This is a constant for all mosaics

 
totalMosaicQuantity = mosaic m supply * 10 ^ (mosaic m divisibility)

 
supplyRelatedAdjustment = floor(0.8 * ln(maxMosaicQuantity / totalMosaicQuantity)

 
Then the transaction fee is calculated as

 
xemfee= Min(25,y*900_000/MosaicSupply), where y is the number of mosaics to be sent out, e.g., 150 mosaics. MosaicSupply is the number of Mosaics in whole numbers.

 
Example:

 
i) Mosaic with 9,000,000 supply and divisibility of 3

 
totalMosaicQuantity = 9,000,000 * 1,000 = 9,000,000,000

 
supplyRelatedAdjustment = floor(0.8 *ln(9,000,000,000,000,000 / 9,000,000,000)) = floor(11.052) = 11

 
transferring 150 such mosaics is like transferring 150_000 xem:

 
xemFee = 15 xem

 
Transaction fee = 0.05*(15 xem - 11 xem) = 0.2 xem

 
`fee formula = 0.05*Max(1, Min(25,y*900_000/MosaicSupply) - floor(0.8*ln(9_000_000_000_000_000 / MosaicSupply*10^divisibility)))`

 
### MultisigAggregateModificationTransaction 
Base fee is 10 XEM

 
Fee factor is 0.05

 
Transaction fee is 0.5 XEM

 
### ProvisionNamespaceTransaction/MosaicCreationTransaction 
Fee for root namespace provisioning: 100

 
Fee for sub-namespace provisioning: 10

 
Fee for mosaic creation: 10

 
Transaction fee for the above is 

 
Base fee is 3 XEM

 
Fee factor is 0.05

 
Transaction fee is 0.15 XEM

 
### Other transactions like MosaicSupplyChangeTransaction, ImportanceTransferTransaction, SignatureTransaction... 
Transaction fee for the above is 

 
Base fee is 3 XEM

 
Fee factor is 0.05

 
Transaction fee is 0.15 XEM

 
