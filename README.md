# Detailed steps to install your project and executing instruction:

* Install Python version 3.8, Jupyter Notebook to run the code
* Modules required: Flask, cryptography, requests.
* At least 3 Peer machines are required to view the correct working of the code.
* Implementation should be carried out on the Virtual Machines as the IP address needed should be different for all the peers.
* Open the Manager.ipynb file in the Jypyter Notebook and change the Manager IP address to your machine address and run the
     entire notebook

<br>
<hr>
<br>

(_**NOTE: In Peer.ipynb file, the stakes of all the peers should be different: you can change it on the following piece of code**_)
```bash
client._add_stake(60)
``` 

<br>
<hr>
<br>

* Open the *Peer.ipynb file* in the Jupyter Notebook and change the **Manager IP** mentioned in the Class Peer to your machine IP
     address and also change the **Peer IP** address to your machine IP address and run the notebook upto
     ```bash
     client.blockchain.to_json()
     ```
* To add transaction run the following piece of code.
  ```bash
  transaction_data = {
    'recipient': '7a48aba3',
    'amount': 70  
  }
  ```
* To add the transaction to the pool run: 
  ```bash 
  client.transaction_pool.transaction_data()
  ``` 
* To mine the added transaction run: 
    ```bash
    client.mine_dpos_transaction()
    ```
* To corrupt the block run: 
  ```bash
  client.blockchain.to_json()[1]["last_hash"] = "corrupt"
  ```
<br>
<hr>
<br>

(_**NOTE: Always sync after running corrupt to reflect it on the blockchain**_)

* To sync the block run: 
  ```bash
  client.sync_chain()
  ```

<br>
<hr>
<br>

(_**NOTE: the steps of adding block to the blockchain always go in the flow: transact --> mine --> sync**_)

* To view your blockchain run:
  ```bash
  client.blockchain.to_json()
  ```
