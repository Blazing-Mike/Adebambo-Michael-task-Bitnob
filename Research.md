  # Taproot and its importance
 
The world is gradually becoming a cashless society and in a society like this, there is a need for autonomy, privacy and anonymity.
Physical cash is not a practical alternative in our ever increasing digital world because people want to move value over the internet. We are then forced to seek electronic replacement that is equal to or better in utility and benefits - such as  preservation of one's autonomy, privacy, and anonymity - to cash.


Bitcoin, an electronic peer-to-peer, open, decentralized, and censorship-resistant Cryptocurrency is  designed for such a purpose. 
Though it is still yet to be fully privacy and anonymity preserving, it is getting closer to be with development techniques like **Taproot**.

## What is Taproot

Taproot is a soft fork that improves Bitcoin’s script to increase bitcoin’s scalability, privacy, and throughput rate while reducing fees and laying the foundation for upgrades in the future. It was proposed by Greg Maxwell in 2018 and officially activated on 14 November 2021

## Technical specifications

The Taproot update encompasses three Bitcoin Improvement Proposals (BIPs), including;

 - [BIP340(BIP – Schnorr)](https://github.com/bitcoin/bips/blob/master/bip-0340.mediawiki)

 - [BIP341 (BIP – Taproot)](https://github.com/bitcoin/bips/blob/master/bip-0341.mediawiki)

 - [BIP342 (BIP – Tapscript)](https://github.com/bitcoin/bips/blob/master/bip-0342.mediawiki)

I explained them briefly as follows;
 
 **BIP340 (Schnorr signatures)** : A signature is what allows users to send (spend) bitcoins and for nodes to verify that transactions are valid. 
Bitcoin’s current signature system uses Elliptic Curve Digital Signature Algorithms (ECDSA).
Schnorr signatures are mathematically simpler, secure and flexible than ECDSA signatures.

Schnorr allows two  parties to efficiently combine their signatures, this linear combination of public and private keys allows for batch verification of a transaction whereby nodes add up public keys, add up signatures and confirm that the transaction is valid.
 With Schnorr Signatures, a single aggregated public key and a single aggregated signature are both recorded, rather than all of the public keys and signatures of all involved participants.





  **BIP341 (BIP – Taproot)** : This proposal builds on the last major update on the bitcoin network, which is the segwit in 2017. 
It combines Merkel branches, new sighash modes, taproot and a few improvement proposals. Taproot implements Merkel branches (MAST) to scale the amount of transaction data on bitcoin blockchain by only revealing or committing to the blockchain executed conditions of a smart contract transaction to be committed to the blockchain rather than the full details as opposed to other ways a script can be executed.
 
The idea behind MAST is  to use a Merkle tree to encode branches in a script and it comes from two pre-existing concepts, [abstract syntax trees](https://en.wikipedia.org/wiki/Abstract_syntax_tree) and [merkle trees](https://en.wikipedia.org/wiki/Merkle_tree). Since, ASTs allows us to split a program into its individual parts, and merkle trees allow us to verify the individual parts belong to a complete program without the entire program being present. 
MAST Allows spenders to replace the unused parts of encumbrances with a [merkle proof](https://computersciencewiki.org/index.php/Merkle_proof) — reducing transaction size, increasing privacy, and making larger smart contracts possible.




 **BIP342 (BIP – Tapscript)** :  Tapscript updates the Script coding language used to write bitcoin transaction parameters in order to make Schnorr signatures, batch validation, and signature hash improvements available to spends that use the script system as well.
 [Multi-signature](https://help.interdax.com/hc/en-001/articles/360002545817-What-is-a-Multi-signature-Wallet-) opcodes ```OP_CHECKMULTISIG``` and ```OP_CHECKMULTISIGVERIFY``` are replaced by a ```OP_CHECKSIGADD``` opcode — which allows for signature batch verification with Schnorr.
Tapscript will also make it easier to implement future updates to Bitcoin by allowing new types of opcodes (transaction instructions) to be more seamlessly introduced.


## Importance

1. **Privacy**: With Schnorr signatures and key aggregation, multisignature contracts no longer look different from single signature contracts, providing privacy to all Taproot users. 
Since Taproot also allows for locking bitcoin with different scripts, only the script used to execute the condition is revealed which thereby improves privacy.


2. **Smart contacts**: This has nothing to do with De-Fi and NFTs functionalities that smart contracting platforms like Ethereum provide.
 A smart contract is a way of making certain things happen when certain conditions are met and locking it into the code of transaction. 
A simple example of that may be a timelock contract that makes a UTXO spendable when a particular time is clocked. 

   With schnorr signatures it is possible to enable simpler higher-level protocols, such as atomic swaps that are indistinguishable from normal payments. These can be used to build more efficient payment channel constructions.


3. **Lower transaction fees** : Spending Taproot outputs is cheaper because the public key is included in the scriptPubKey, and thus does not need to be included in the witness data.
 Also because schnorr signatures allow for batch verification on transactions it makes it easier to verify transactions on the Bitcoin network and reduces fees as well. 


4. **Scalability**: Improves network scalability by reducing the amount of data to be transferred and stored on the blockchain.















