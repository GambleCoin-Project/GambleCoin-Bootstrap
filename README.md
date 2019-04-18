```
Current Bootstrap
Date:  
Block: 
MD5 Checksum: 705E1BA224E1F8B1BF47E45AEE5C18DC
SHA-1 Checksum: C47B0E27FCFE0AC0A2B4B9CD37190A6590BE791F
SHA-256 Checksum: 79D6FFC1A5C462863836197D79DC565B7E199EAE3AED60F523CCCBE7C3B6079E
SHA-512 Checksum: 1F40B813A9A9B36A52A1B63FB4E54E988B689E6D4A312BBC2799A728E09F85E7EDF97C1914D9E51FB3092CA6BB017E7DC2A308FDE79C61DBDE2E8C95D7802F66
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
wget https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/blob/master/gamblecoin-bootstrap.sha1
shasum -c gamblecoin-boostrap.sha1
```
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
