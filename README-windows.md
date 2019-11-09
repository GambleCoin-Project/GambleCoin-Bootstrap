```
Current Bootstrap
Date: 12-Jul-2019
Block: 373048
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

## Windows General Instructions (zip)
**1. Download the bootstrap file**

Go to https://github.com/GambleCoin-Project/GambleCoin-Bootstrap/releases and download the latest gamblecoin-bootstrap.zip
 
**2. Validate the checksum of the file**

Download your favorite MD5 and/or SHA checksum tool.  You can find one [here](http://raylin.wordpress.com/downloads/md5-sha-1-checksum-utility).

Browse to the location where you stored the gamblecoin-bootstrap.zip file, and select the file.  The program will crunch for a bit, and then display several checksums.

Choose your favorite checksum from the list under gamblecoin-bootstrap.zip in the release notes, and paste the hash in the bottom field, and select "verify".  A window should open stating that the hash matched.

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

right click on your downloaded gamblecoin-bootstrap.zip and select "Extract All" and extract the bootstrap to a gamblecoin-bootstrap/ directory.   Once that is complete, you can delete the .zip file.

Navigate into gamblecoin-bootstrap, select all 4 items, copy them (ctrl-c), and paste them in your AppData/Roaming/GambleCoin folder.
 
**9. start up gamblecoind and/or gamblecoin-qt**

After the copy has completed, you can re-open your gamblecoin-qt wallet; and it should start up at the last block from the bootstrap file.
