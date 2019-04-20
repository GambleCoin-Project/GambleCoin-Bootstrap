```
Current Bootstrap
Date:  19-Apr-2019
Block: ~305700
```
## gamblecoin-bootstrap.tar.gz Checksums
```
MD5 Checksum: 9C3569C987C64C452D2EDDC038BB53E2
SHA-1 Checksum: 4470C0D9A05E37D84E9B8F881B03B087A81D3D95
SHA-256 Checksum: EBBEF2F411858BC2C9D39B301F1DB856E53F179380F3AA5F4E7739C82F58BE13
SHA-512 Checksum: 9FBA218D6ED49ACDA8F61EA8D85AD56542202BEF36B75D7DD894460F2DCDA2875C01AFC633E35881711326A69B7B66F2D36EDBE0F4A47CAF5F45B08A741F510C
```
## gamblecoin-bootstrap.zip Checksums
```
MD5 Checksum: D29499409144D5629AD0C93E37C4D8FD
SHA-1 Checksum: 8BE78BBE9766B262B72E62F2350ECD6AE74E43C2
SHA-256 Checksum: 3419C8FE2ABA9F6DF8B8836E537AA6D1F8DF79CAC664D385F6B77AE47C1D33E8
SHA-512 Checksum: AAEBE11DAD931BD2388C01A739B9269CCF50AB892D87484EED4BA23AF471CD1325D1CCF5565670F5EA33E3C8F7539C80E03D57D58C9CDC81F7F923B2ED8397C2
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
