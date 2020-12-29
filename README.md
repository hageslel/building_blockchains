## Starting the Blockchain 
The first step to allow access to launching the blockchain will be to ensure all Go Ethereum (geth) tools are installed.  Additionally, a MyCrypto wallet will need to be created.  Instructions to complete both tasks can be found here: (figure out how to insert install instructions here)

Once all Go Ethereum dependencies are installed and a MyCrpto wallet is created, the blockchain can be launched via your terminal (GitBash on Windows).  The exact instructions outlined below are based on a Windows PC and utilizing GitBash.  Activation instructions may vary slightly depending on your operating system.  

- Launch a terminal window (GitBash) and navigate to your Blockchain-Tools folder (created in the above install instructions).  
- Unlock node1 (named jnode1 in this network) with the following command: ./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock
- Unlock node2 (named jnode2 in this network) with the following command: ./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock


