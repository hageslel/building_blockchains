## Starting the Blockchain 
The first step to allow access to launching the blockchain will be to ensure all Go Ethereum (geth) tools are installed.  Additionally, a MyCrypto wallet will need to be created.  Instructions to complete both tasks can be found here: (figure out how to insert install instructions here)

Once all Go Ethereum dependencies are installed and a MyCrpto wallet is created, the blockchain can be launched via your terminal (GitBash on Windows).  The exact instructions outlined below are based on a Windows PC and utilizing GitBash.  Activation instructions may vary slightly depending on your operating system.  

- Launch a terminal window (GitBash) and navigate to your Blockchain-Tools folder (created in the above install instructions).  
- Unlock node1 (named jnode1 in this network) with the following command: ./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock
- Unlock node2 (named jnode2 in this network) with the following command: ./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock
- The SEALER_ONE_ADDRESS, SEALER_TWO_ADDRESS, and SEALER_ONE_ENODE_ADDRESS were provided when creating and initializing each node.  A best practice is to document these addresses for ease of blockchain unlocking.  This data can be viewed in the screen shots provided in the "Screenshots" folder, as well as in the document attached.  
- Once the above steps are complete the blockchain will be up and running again.  

## Testing the Blockchain - MyCrypto
To ensure the blockchain is operating as designed, it can be tested using MyCrypto.  The steps outlined below explain how to connect to a custom network on MyCrypto and test the network by sending transactions.  

- Open MyCrypto and click on "Change Network" in the bottom left corner. 
- Click "Add Custom Node". 
- Make sure to select "Custom" for the network.  This will generate additional fields to be filled in.  
- Enter the Node Name, the Network(should already be set to "Custom" from the step above), the Network Name, Currency, ChainID, and URL. 
- The Currency should be set to ETH, and the ChainID will be the chain id generated when creating the genesis block. 
- The URL will be: http://127.0.0.1:8545. 
- Click "Save & Use Custom Node".

Now that we are connected to the network created above, we can begin testing it by generating transactions between accounts.  Follow the steps outlined below to complete this. 

- Make sure you are on the "View & Send" tab in MyCrypto. 
- From there, click on "Keystore File".  This will bring up a new window, allowing you to unlock your keystore file. 
- Click on "Select Wallet File".  From there navigate to the directory where the node data was saved.  Access the node1 folder and then the keystore folder.  Click on the file within the keystore folder and click open.  
- The password created during the node generation will need to be entered to unlock the the file.  Once this is done, click "Unlock". 

Now that the account is unlocked, we are ready to send a transaction.  To do this, follow the steps below. 

- Enter the account address for node2 in the "To Address" box.  
- Enter an amount to be sent to that account and click "Send Transaction"
- A green confirmation message should populate below.  Within that box click on the "Check TX Status" button.  
- The transaction may still show in "Pending" status, but once "Check TX Status" is clicked again it should change to "Successful" status. 
- To view this transaction at a later time, you can also click on the "TX Status" button on the left hand side of the MyCrypto app.  From there you can enter the transaction hash (TX Hash), click "Check TX Status" and view the status once again.  






### Still need to do the following: 
- Be sure to include all of the geth flags required to get both nodes to mine and explain what they mean.
- Explain the configuration of the network, such as it's blocktime, chain ID, account passwords, ports, etc.
- Explain how to connect MyCrypto to your network and demonstrate (via screenshots and steps) and send a transaction.
- Upload the code, including the networkname.json and node folders.
- Enter photos
- Link install instructions

