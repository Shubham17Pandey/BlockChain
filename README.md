# BlockChain

Description
To design and develop a blockchain network to facilitate MICROPAYMENT transactions among users to
decrease the cost of transfers and move money quickly and reliably.


Instructions
Step 1:

Fire up one instance in command line with
$ npm run dev
 // default HTTP_PORT=3001 P2P_PORT=5001

Step 2: 

Run a second instance in a second command line tab:
$ HTTP_PORT=3002 P2P_PORT=5002 PEERS=ws://localhost:5001 npm run dev 
// web socket 5002 is now connected to the web socket 5001 for blockchain synchronization

Step 3:

In Postman, insert a POST request 'localhost:3002/transact'. Open 'Body' tab choose 'raw' and select 'JSON (application/json)'.

Step 4:

Enter the Recipient address and amount to be sent to the recipient form the sender host 3002
Ex: 
	{
		"recipient": "r-4ddr355",
		"amount": 50
	}

Step 5:

Fire the POST request by clicking the SEND button. Details of the transaction block will appear.

- Next step is to mine the transaction block in the blockchain. This can be done by either running a new instance with different HTTP and P2P ports
or the sender host 3002 itself can mine the transaction in the blockchain.

Step 6:

In Postman, open new tab and insert a GET request 'localhost:3002/mine-transactions'. 

Step 7:

Fire the GET request. The transaction block will be mined in the blockchain, the request will redirect to the '/blocks' and the complete blockchain will appear
with the transation block mined inside it.

- The details of the transaction can be verified using the details of transaction block. 
 
