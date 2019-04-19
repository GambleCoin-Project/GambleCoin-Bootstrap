```
Current Bootstrap
Date:  19-Apr-2019
Block: ~305700
MD5 Checksum: 9c3569c987c64c452d2eddc038bb53e2
SHA-1 Checksum: 4470c0d9a05e37d84e9b8f881b03b087a81d3d95
SHA-256 Checksum: ebbef2f411858bc2c9d39b301f1db856e53f179380f3aa5f4e7739c82f58be13
SHA-512 Checksum: 9fba218d6ed49acda8f61ea8d85ad56542202bef36b75d7dd894460f2dcda2875c01afc633e35881711326a69b7b66f2d36edbe0f4a47caf5f45b08a741f510c
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
**1. Download the bootstrap file**
```
wget https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/blob/master/gamblecoin-bootstrap.tar.gz
```
**2. Validate the checksum of the file**
```
wget https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/blob/master/gamblecoin-bootstrap.sha512
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

## Windows Specific Instructions
**1. Download the bootstrap file**
 
**2. Validate the checksum of the file**
 
**3. Shutdown your gamblecoind and/or gamblecoin-qt**
 
**4. Wait for the shutdown to complete (watch the process)**
 
**5. Backup your wallet.dat off your computer**

**6. Backup your gamblecoin.conf and masternodes.conf files**

**7. remove your "blocks", "chainstate", "sporks" and "peers.dat" files**
 
**8. unpack the bootstrap file and place the 3 directories and peers.dat file where the others were.**
 
**9. start up gamblecoind and/or gamblecoin-qt**
