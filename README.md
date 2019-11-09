```
Current Bootstrap
Date:  09-Nov-2019
Block: 469101

```
## gamblecoin-bootstrap.tar.gz Checksums
```
MD5 Checksum: 0250da9d7c9c300958e81601b08cb992
SHA-1 Checksum: bbc6f41b78f2bf93f3cd3ebbc0121731ec0cc3f0
SHA-256 Checksum: 9f4b3438a45f85015e73ceda47e1a6985c59ab7ae6e9c1f9f6455491b7eb9534
SHA-512 Checksum: 170dd7e53ee342aa713ad76971f76a49372564b3b76af9d919dc951753ada7daef5e6d3583a7a72d7bbe709a188f89243f059f4386adccfa0b572c81a5035419
```
## gamblecoin-bootstrap.zip Checksums
```
MD5 Checksum: CFAD5D739B8D467E4B0A51CC9352ACAD
SHA-1 Checksum: CADB28918395CBA11087DEAA008769C1568D3B85
SHA-256 Checksum: A1E2D487E81FA52EFDBAED57015F0F805CE9FDD3F1069626940ED024C3510361
SHA-512 Checksum: CE2B50116C162946D0F8D4B229E58EF616F9CA27D840CCCCE483BF4E1A92F7A7E5D6A02F30B465FF25BAEC46325089D32A2B8C8D5E66B4FFD9E9EEF29E682CA9
```

# Official GambleCoin Bootstrap Instructions
## Important Note
Loading a bootstrap into your full node is not the safest procedure, and one should take precautions to make sure that the bootstrap they are loading is validated and has not been modified in any way.  By installing a bootstrap, you are bypassing the validation that is made on each block as the node processes it; as you are effectively telling your node that it has already validated the blocks and it doesn't need to do it again.  There are many attack vectors that can be exploited if someone is able to convince you to load a counterfeit bootstrap.

However, as chains get longer; resynching your existing node, or initially synching your new node, is a time consuming and resource intensive process.  It is, and will always be, the right thing to do.  The second best thing to do is maintain your own bootstrap, generated from chains that you have had control over (e.g. a bootstrap generated from your vps masternode to fix a problem with your PC node, or to bring up a new masternode).  We provide this repository to do what we can, to ensure the validity of the bootstrap contained within; however it is, and will always be, **use at your own risk**.

## Basic Instructions
1. Download the bootstrap file
2. Validate the checksum of the file
3. Shutdown your gamblecoind and/or gamblecoin-qt
4. Wait for the shutdown to complete (watch the process)
5. Backup your wallet.dat off your computer
6. Backup your gamblecoin.conf and masternodes.conf files
7. remove your "blocks", "chainstate", "sporks" and "peers.dat" files
8. unpack the bootstrap file and place the 3 directories and peers.dat file where the others were.
9. start up gamblecoind and/or gamblecoin-qt

## Linux Specific Instructions
Please see [Linux Specific Instructions](https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/blob/master/README-linux.md).

## Windows Specific Instructions (tar.gz)
For Windows instructions utilizing the 7Zip utility, please see [Windows Specific Instructions](https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/blob/master/README-windows-7zip.md).

## Windows General Instructions (zip)
For General Windows instructions, please see [Windows General Instructions](https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/blob/master/README-windows.md).
