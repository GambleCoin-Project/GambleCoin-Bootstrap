```
Current Bootstrap
Date:  12-Jul-2019
Block: 373048
```
## gamblecoin-bootstrap.tar.gz Checksums
```
MD5 Checksum: 315b43d26f46d4c17f6d1179a01cc205
SHA-1 Checksum: c55b59078c5e4645a0ce321ad2202264c344fa95
SHA-256 Checksum: 3061a7e3181aea0fbde4eba91c8dcb850bc83b72e980c94aed749b852337c672
SHA-512 Checksum: 7f9ccc1dbaca48f70b67c21a137889bce0867f6a9e7c88a141d634da869c139475704a5278651d03cd042467fa9816dc816a864cfbc2541d58c57039e4bf7d1c
```
# Official GambleCoin Bootstrap Instructions
## Important Note
Loading a bootstrap into your full node is not the safest procedure, and one should take precautions to make sure that the bootstrap they are loading is validated and has not been modified in any way.  By installing a bootstrap, you are bypassing the validation that is made on each block as the node processes it; as you are effectively telling your node that it has already validated the blocks and it doesn't need to do it again.  There are many attack vectors that can be exploited if someone is able to convince you to load a counterfeit bootstrap.

However, as chains get longer; resynching your existing node, or initially synching your new node, is a time consuming and resource intensive process.  It is, and will always be, the right thing to do.  The second best thing to do is maintain your own bootstrap, generated from chains that you have had control over (e.g. a bootstrap generated from your vps masternode to fix a problem with your PC node, or to bring up a new masternode).  We provide this repository to do what we can, to ensure the validity of the bootstrap contained within; however it is, and will always be, **use at your own risk**.

## Linux Specific Instructions
**1. Download the bootstrap file**
```
wget https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/releases/download/v19.07.12-373048/gamblecoin-bootstrap.tar.gz
```
**2. Validate the checksum of the file**
```
wget https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/raw/master/gamblecoin-bootstrap.sha512
shasum -c gamblecoin-bootstrap.sha512
```
(note: md5, sha1, sha256 and sha512 checksums are available, you are free to pick and chose whichever you prefer)

**3. Shutdown your gamblecoind and/or gamblecoin-qt**
```
gamblecoin-cli stop
```
**4. Wait for the shutdown to complete (watch the process)**
```
ps aux | grep gamblecoin
watch ps p <pid>
```
**5. Backup your wallet.dat, gamblecoin.conf and masternodes.conf files off your computer**
```
cd ~/.gamblecoin
tar czf ~/gamblecoin-config.tar.gz backups/ wallet.dat gamblecoin.conf masternodes.conf
```
(and copy the resulting gamblecoin-config.tar.gz off your computer to a safe place)

**7. remove your "blocks", "chainstate", "sporks" and "peers.dat" files**
```
pwd # to confirm you are still in your approprate directory
rm -r blocks/ chainstate/ sporks/ peers.dat
```
**8. unpack the bootstrap file and place the 3 directories and peers.dat file where the others were.**
```
pwd # to confirm you are still in your approprate directory
tar xzf ~/gamblecoin-bootstrap.tar.gz
```
**9. start up gamblecoind and/or gamblecoin-qt**
```
gamblecoind -daemon
```

