## Factom Binaries

The latest version of Factom is version **0.4.2.8**, released **30 August, 2017**

The latest version of Enterprise Wallet is Version **0.2.0.0**, released **7 September, 2017**

Install guide located [here](https://docs.factom.com/wallet#install-factom-federation-ff).

![Enterprise Wallet](img/enterprise.png)

### Factom Enterprise Wallet

| OS | Enterprise Installer | sha256sum |
|----|-----|-----|
| Windows 64bit | [enterprise-wallet-setup-amd64.exe](https://github.com/FactomProject/distribution/releases/download/v0.4.2.8/enterprise-wallet-setup-amd64.exe) | e069903edc03c9d24938f83cd853982d525596f65d462d172af96934ab95b355 |
| Mac |  [enterprise-wallet-setup.dmg](https://github.com/FactomProject/distribution/releases/download/v0.4.2.8/enterprise-wallet-setup.dmg) | c6885ba3e78993e913ef51a6fcfb0066cb32ea7d420f960e7d33ffe347b7eddc |
| Linux (Ubuntu/Debian) 64bit | [enterprise-wallet-setup-amd64.deb](https://github.com/FactomProject/distribution/releases/download/v0.4.2.8/enterprise-wallet-setup-amd64.deb) | 671cd69f64ff395ce58fa14742323b238f799ed9f857d6b1acf95bf89b37ee97 |
| Linux (Redhat/Centos) | [enterprise-wallet-linux.zip](https://github.com/FactomProject/distribution/releases/download/v0.4.2.8/enterprise-wallet-linux.zip) | f187236d6968f1625216d034225305087edd56968f8f1081372725953fcca70b |


#### Release notes for v0.2.0.0
- [new] added a password protected, encrypted wallet option
- [new] revamped the seed backup and restore processes, no longer exposing their 12 words on the user's hard drive
- [new] a fresh coat of paint! Cleaned up portions of the UI

See our [blog post](https://www.factom.com/blog/encrypted-enterprise-wallet) for details.

#### Release notes for v0.1.3.1
- [fix] Now able to enter a "." character to increase precision of a factoid sending transaction.

#### Release notes for v0.1.3
- [fix] An error regarding the wallet's sync status was showing despite the wallet saying 100% synced. This message would only go away when factomd's second pass hit 100%. This has been rectified.
- [fix] The screen appearing blank/freezing when editing an address has been fixed. All addresses will have special characters in their names replaced with '_'
- [new] The courtesy remote node has a new domain, all users using factomd-live.cloudapp.net will automatically be updated to courtesy-node.factom.com.
- [new] The courtesy remote node will now be the default blockchain target.  This will help new users with getting started.

#### Release notes for v0.1.2
- GUI now remains responsive with slow API responses




### Factom Command Line Interface Programs

![Factom CLI apps](img/factomd.png)

| OS | Factomd Installer | sha256sum |
|----|-----|-----|
| Windows 64bit | Please install from [source](https://github.com/FactomProject/FactomDocs/blob/master/installFromSourceDirections.md) or use [earlier release](https://github.com/FactomProject/distribution/blob/eca929370f214426751f261477c1b69ec989d698/README.md#factom-command-line-interface-programs) |  |
| Windows 32bit | Please install from [source](https://github.com/FactomProject/FactomDocs/blob/master/installFromSourceDirections.md) or use [earlier release](https://github.com/FactomProject/distribution/blob/eca929370f214426751f261477c1b69ec989d698/README.md#factom-command-line-interface-programs) |  |
| Mac | Please install from [source](https://github.com/FactomProject/FactomDocs/blob/master/installFromSourceDirections.md) or use [earlier release](https://github.com/FactomProject/distribution/blob/004d0b75082255ef26b608c857c9f598d18c7f9d/README.md#factom-command-line-interface-programs) |  |
| Linux (Ubuntu/Debian) 64bit | Please install from [source](https://github.com/FactomProject/FactomDocs/blob/master/installFromSourceDirections.md) or use [earlier release](hhttps://github.com/FactomProject/distribution/blob/004d0b75082255ef26b608c857c9f598d18c7f9d/README.md#factom-command-line-interface-programs) |  |
| Linux (Ubuntu/Debian) 32bit | Please install from [source](https://github.com/FactomProject/FactomDocs/blob/master/installFromSourceDirections.md) or use [earlier release](https://github.com/FactomProject/distribution/blob/004d0b75082255ef26b608c857c9f598d18c7f9d/README.md#factom-command-line-interface-programs) |  |
| Linux (Redhat/Centos) | Please install from [source](https://github.com/FactomProject/FactomDocs/blob/master/installFromSourceDirections.md) | |



Source code archive: [factom_source_v0.4.2.8.zip](https://github.com/FactomProject/distribution/releases/download/v0.4.2.8/factom_source_v0.4.2.8.zip)

## Release notes for v0.4.2.8
- [new] Added ability to suppress raw data when printing blocks with -r flag
- [new] Shifted to CircleCI for automated testing.
- [fix] Updated Pending Entries duplicate checking


## Release notes for v0.4.2.7
- [new] added FACTOM_HOME environment variable or -factomhome flag for .factom directory
- [fix] reduced load on api of factom-walletd under heavy traffic
- [fix] updated savestate to correct potential balance corruption
- [new] improved authority management code in factomd
- [new] added config option -exp for enabling profiling from non-localhost
- [new] update Entry Credit Block API response
- [fix] correct a printout for negative numbers in factom-cli

## Release notes for v0.4.2.6
- [fix] better handling of Chain Heads between creation and when an Entry Block is made
- [fix] ignore duplicate commits which pay for a disallowed duplicate reveal
- [fix] resolved a bug where more commits could be acknowledged than the net Entry Credits should have allowed
- [fix] remove CPU overload when factomd is run in container with "-nosim=true" flag
- [new] framework for supporting additional plugins
- [new] add support for logrus for better log handling
- [new] add additional Prometheus instrumentation across various functions
- [new] add new API calls "admin-block", "factoid-block", "entrycredit-block" which output unmarshaled versions of those blocks
- [new] add "ack" api call which takes a ChainID, setting the stage to accommodate nodes that only download some chains

## Release notes for v0.4.2.5
- [new] Added 'current-minute' API to check status of factomd node, enabling faster detection of stalls
- [new] Added addresses of inputs and outputs of factoid transactions to 'pendingtransactions' API and factom-cli call
- [new] Better logging infrastructure for debugging at scale
- [fix] Stop leaders from stalling when restarting after a fault

## Release notes for v0.4.2.4
- [fix] Don't save unverified ancillary data received from a misbehaving peer
- [new] Create utility to fix corrupted database chain heads
- [fix] Immediately flush DBstates that will never become valid
- [fix] Improve order of operations when saving DBstates with an incomplete process list

## Release notes for v0.4.2.3
- [Fix] Fixed a bug which prevented nodes from processing messages following initial blockchain download.
- [Fix] Speedup boot while synching by ignoring messages which won't affect the state.
- [Fix] Now discard dbsig messages which will never become valid, and handle potential collisions better.
- [Fix] Handle EOM messages better with an invalid signature.
- [New] Chain creation in wallet API now no longer forces user calculation of the ChainID.
- [New] Add more historical checkpoints.
- [New] Protect users from paying too many entry credits for an entry.

## Release notes for v0.4.2.2
- Fast bootup mode is now enabled by default.  Factomd will complete the startup process faster after booting with a previously downloaded blockchain.  (To disable this feature, start factomd with -fast=false)
- The P2P connection is now less likely to be dropped with low numbers of peers.
- Entry acknowledgement feedback is now more likely to succeed between minute 0 and 1 of block creation.
- Chain creation acknowledgement feedback is now more likely to give timely results
- More instrumentation of the API accessors
- more fidelity of loading metrics from the database

## Release notes for v0.4.2.1
- This is a feature preview of the fast bootup mode.
- Upgrade is only needed to try the new mode.
- With this version, when booting after downloading the blockchain, factomd will save most of the work it does when starting.  When starting again, it will fully startup much faster.
- To try, start with this command `factomd -fast=true`
- This release does not include any bugfixes beyond what 0.4.2.0 fixed.

## Release notes for v0.4.2.0
- Better discovery of the highest block.
- Catches up to highest block more quickly from 1-2 blocks behind.
- Fix some bugs in process list handling.
- Allow to download past block 87623.  Older versions will likely get stuck. 


## Release notes for v0.4.1.3
- Fix bug where block height stays 1-3 block behind servers for an extended period of time.
- Fix bug where client can lose synchronization with the servers.
- Fixed bug where data was downloaded then ignored/deleted.


## Release notes for v0.4.1.2
- This improves some network message management.
- Improve handling of entries over the p2p network
- Added some instrumentation


## Release notes for v0.4.1.1
- This fixes a problem which causes network disconnections when many peers are connecting to a node.
- Increase the broadcast rate of p2p messages


## Release notes for v0.4.1.0

**This is a required upgrade.**  Older versions of software will not download new blocks from the network.

- Large fix for network connection problems
- Prioritized Directory Block and Factoid Block downloading over Entry downloading.  This is apparent when viewing the control panel 1st and 2nd pass.
- Limitations on outgoing peers
- reduce outgoing message traffic
- add computed balance messaging to prevent out-of sync balances (thanks to [34ro](https://github.com/34ro) for reporting the error)
- add prometheus logging for nice graphana performance graphs
- expose API for checking leader status
- add API call to get network transaction rate
- Database consistency fixes
- updated leveldb to include upstream fixes


Known issues:
- If an earlier version of factomd was run, it may have corrupted your local database.  If you are seeing panics as you are booting the latest factomd, the safest fix is to delete (or rename) your ~/.factom/m2/main-database folder
- On machines with 4GB or less of RAM, memory spikes have been observed which cause the OS to stop factomd while downloading the blockchain.


## Release notes for v0.4.0.3

- This latest update fixes some consistency bugs.  It is more aggressive in filling in gaps introduced when synching the blockchain with marginal network connections.  This fixes some problems people were seeing with missing entries. (factoid transactions did not fall under this bug)
- This updates to Golang 1.8, which gives better garbage collection.
- Added some stabilization of the network connectivity.


## Release notes for 0.4.0.2

- Resolve "too many files" error

On Linux and Mac, factomd would crash due to using too many open files.  This bug has been solved, and factomd no longer needs the adjust the ulimit in order to work.

- Resolve Windows Database Problem

Enterprise Wallet and factom-walletd on some Windows systems would not cache factoid transactions.  This solves the User Map Restriction bug.

- Networking more Resiliant

Timeouts for network connections have been increased.  This gives an incremental improvement for some stalling problems that factomd nodes have been seeing.

- Lower CPU usage

Idle time CPU usage has been decreased for times after factomd boot and syncs.

- Right Click in Wallet

Now the Enterprise Wallet supports right clicking for copy/pasting etc.



- Workarounds

One known issue is that factomd does not keep up with new blocks if it needs to download many blocks after starting.  The workaround is to start factomd, allow it to download all the blocks so far created.  Close factomd (ctrl+c) and restart it.  it should keep up with blocks after the second start.


The blockchain is fairly large and the P2P sync code is not fast.  To expedite the startup time, the first 70k blocks can be downloaded via http.
 https://www.factom.com/assets/site/factom_bootstrap.zip
 SHA256: 2d4d256c337cdabc8f75aa71180c72129f807c365c78356471350ac1e0a4faed

Extract the zip file to your home directory. It will create files in the location: ~/.factom/m2/main-database/ldb/MAIN/factoid_level.db/   Compressed the blockchain is currently about 5 GB and uncompressed is over 9 GB.


factomd is much slower to start on a spinning hard drive, compared to a solid state drive.  It is recommended to save the blockchain on a solid state drive.


