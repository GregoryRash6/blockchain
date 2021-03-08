# Proof of Authority Development Chain

## Steps to Start the Network:

### Step One: Install MyCrypto

#### How to Install MyCrypto:
1. Open a browser and navigate to the MyCrpyto download [link](https://download.mycrypto.com).
2. Download the correct version, based on your operating system.
3. Follow the installation wizard.
4. Open MyCrypto.
5. Select "Create New Wallet".
6. Select "Generate a Wallet".
7. Select "Generate a Mnemonic Phrase".
8. Write down the mnemonic phrase provided.
9. Provide the mnemonic phrase.
10. Select "View & Send".
11. Select "Mnemonic Phrase".
12. Input your mnemonic phrase.
13. Select "Choose address".
14. Select "Testnet (ETH)" for the "Addresses" dropdown.
15. Select the first address and select "Unlock".
16. Write down your "Account Address".
17. Select "Wallet Info".
18. Write down your "Private Key".

### Step Two: Install Go Ethereum Tools

#### How to Install Go Ethereum Tools:
1. Open a browser and navigate to the Go Ethereum Tools download [link](https://geth.ethereum.org/downloads).
2. Scroll down to the "Stable Releases" section.
3. Download "Geth & Tools 1.9.25".
4. Decompress the archive found in your "Downloads" folder, and rename the decompressed folder as "Blockchain-Tools".

### Step Three: Navigate to "Blockchain-Tools" Folder in Terminal

#### How to Navigate to "Blockchain-Tools" Folder in Terminal
1. Open Terminal.
2. Navigate to your "Downloads" folder.
3. Navigate to your "Blockchain-Tools" folder.

### Step Four: Run Puppeth

#### How to Run Puppeth
1. Type the following command and press "Enter":
``` ./puppeth ```
2. Name your network whatever you'd like and press "Enter":
``` NETWORK_NAME ```
3. Type `2` to pick the `Configure new genesis` option.
4. Type `1` to `Create new genesis from scratch`.
5. Type `1` to choose `Proof of Work` and continue.
6. Type in your "Account Address" from MyCrypto.
7. Press "Enter" to be asked the next prompt.
8. Press "Enter" again to navigate to the next prompt.
9. Come up with a three digit number for your chain ID and press "Enter".
10. Write down your chain ID number.
11. Type `2` to `Manage existing genesis`.
12. Type `2` to `Export genesis configurations`.
13. Exit `puppeth` by using the `Ctrl+C` keys combination.
14. Type the following command and press "Enter":
```./geth account new --datadir node1```
15. Type the following command and press "Enter":
```./geth account new --datadir node2```
16. Type the following command, adjusting for your network name, and press "Enter":
```./geth init NETWORK_NAME.json --datadir node1```
17. Type the following command, adjusting for your network name, and press "Enter":
```./geth init NETWORK_NAME.json --datadir node2```
18. Type the following command and press "Enter":
```./geth --datadir node1 --mine --minerthreads 1```
19. Write down the enode from "Started P2P Networking".
20. Open a new terminal.
21. Follow Step Three to navigate to the "Blockchain-Tools" Folder.
22. Type the following command, adjusting for your enode, and press "Enter":
```./geth --datadir node2 --port 30304 --rpc --bootnodes "enode://<replace with node1 enode address>"```

### Step Five: Set Up Your Custom Node in MyCrypto

#### How to Set Up Your Custom Node in MyCrypto
1. Open MyCrypto.
2. Select "Change Network".
3. Select "Add Custom Node".
4. Input your network name as the "Node Name".
5. Select "Custom" in the "Network" dropdown.
6. Input your network name as the "Network Name".
7. Input "ETH" for the "Currency".
8. Input your chain ID number as the "Chain ID".
9. Input "https://127.0.0.1:8545/" as the "URL"
10. Select "Save & Use Custom Node".

### Step Six: Send Transaction

#### How to Send Transaction
1. Open MyCrypto.
2. Select "View & Send".
3. Select "Private Key" sign in option.
4. Input your private key.
5. Select "Unlock".
6. Input the address you want to send money to as the "To Address".
7. Input your desired amount of currency.
8. Select a transaction speed.
9. Select "Send Transaction".
10. Select "Send".
11. Write down "TX Hash".

### Step Seven: Check TX Status

#### How to Check TX Status
1. Open MyCrypto.
2. Select "TX Status".
3. Input your TX Hash.
4. Select "Check TX Status".