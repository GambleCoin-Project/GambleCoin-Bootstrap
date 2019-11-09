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

# Official GambleCoin Bootstrap Instructions
## Important Note
Loading a bootstrap into your full node is not the safest procedure, and one should take precautions to make sure that the bootstrap they are loading is validated and has not been modified in any way.  By installing a bootstrap, you are bypassing the validation that is made on each block as the node processes it; as you are effectively telling your node that it has already validated the blocks and it doesn't need to do it again.  There are many attack vectors that can be exploited if someone is able to convince you to load a counterfeit bootstrap.

However, as chains get longer; resynching your existing node, or initially synching your new node, is a time consuming and resource intensive process.  It is, and will always be, the right thing to do.  The second best thing to do is maintain your own bootstrap, generated from chains that you have had control over (e.g. a bootstrap generated from your vps masternode to fix a problem with your PC node, or to bring up a new masternode).  We provide this repository to do what we can, to ensure the validity of the bootstrap contained within; however it is, and will always be, **use at your own risk**.

## Windows Specific Instructions (tar.gz)

In order to utilize the gzipped tarball, you need a utility such as [7-Zip](https://www.7-zip.org/download.html).  If you do not have 7zip, it is very useful; especially when working between Windows and Linux.  The following instructions assume you have 7zip.

**1. Download the bootstrap file**

Go to https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/releases and download the latest gamblecoin-bootstrap.tar.gz
 
**2. Validate the checksum of the file**

Right click on the downloaded file, and select "CRC SHA->SHA 256".  7zip will calculate the SHA256 CRC and display it for you.  Compare this with the SHA256 in the release notes to confirm a match.

**3. Shutdown your gamblecoind and/or gamblecoin-qt**
 
**4. Wait for the shutdown to complete (watch the process)**

When you "x" your gamblecoin-qt, wait for the "shutting down" window to go away, and then further look at your processes via "Windows Task Manager" to ensure it's completely shut down
 
**5. Backup your wallet.dat off your computer**

Browse via the file browser to your AppData/Roaming/GambleCoin folder (likely in C:/Users/<username>/), and copy [make sure you copy and don't move] your wallet.dat and backups folder to an alternate location, preferably a USB stick.

**6. Backup your gamblecoin.conf and masternodes.conf files**

In the AppData/Roaming/GambleCoin folder, copy [make sure you don't move] your masternode.conf and gamblecoin.conf files to an alternate location, preferably a USB stick.

**7. remove your "blocks", "chainstate", "sporks" and "peers.dat" files**

In the AppData/Roaming/GambleCoin folder; select the blocks, chainstate, and sporks folders, as well as the peers.dat file.  Take care that you did not accidentally select your masternode.conf, gamblecoin.conf, wallet.dat or backups folder.  After confirming you know what you have selected; delete those folders and peers.dat file.
 
**8. unpack the bootstrap file and place the 3 directories and peers.dat file where the others were.**

right click on your downloaded gamblecoin-bootstrap.tar.gz, in the 7-Zip menu, select "extract here".  After that is complete, you will have a gamblecoin-bootstrap.tar file.  again, right click, select 7-Zip menu and "Extract to gamblecoin-bootstrap\".  Once that is complete, you can delete the .tar.gz and .tar files.

Navigate into gamblecoin-bootstrap, select all 4 items, copy them (ctrl-c), and paste them in your AppData/Roaming/GambleCoin folder.
 
**9. start up gamblecoind and/or gamblecoin-qt**

After the copy has completed, you can re-open your gamblecoin-qt wallet; and it should start up at the last block from the bootstrap file.

