# blockchainhw

### Follow these instructions to create your own local blockchain network

---

#### Create local nodes

Here we will create 2 different nodes that will each have their own address. Follow the command as show below to create them.
![''](./Screenshots/1.png)

Copy this public key as it will be necessary in subsequent steps.
Re-run this command a second time with a new node name to create the second node.

#### Create the genesis network

Run the command ```./puppeth``` to open up the puppeth tool. This is the tool used for creating local networks.
It will now ask for you to specify a network name to administer. Call this whatever you please.
Run through the series of prompts as shown below. We will need to:
1. Configure a new genesis
2. Create a new genesis from scratch
3. Create a Clique or 'proof of authority' type network.
4. Authorize both accounts to be able to seal
5. Pre-fund both accounts

![''](./Screenshots/2.png)


Next we will define a chain ID. Make this any 3-digit number, and make sure to remember it.  

Follow the next prompts as seen below.  

![''](./Screenshots/3.png)

#### Getting ready

Next, initialize both of your nodes using the command ```./geth init yournet.json --datadir yournode1``` , and again with the second node.

![''](./Screenshots/4.png)


#### Starting the network

To start the network, begin mining with the first node using the command  
```./geth --datadir yournode1 --unlock "thelongpublickeyItoldyoutosave4stepsago" --mine --rpc --ipcdisable --minerthreads 1```

![''](./Screenshots/5.png)


We will run a similar command with our second node except that we will need to do 2 things differently.
1. This node will need to run on a different port than the first. (The fist node runs on the default 30303)
2. The two nodes need to be connected together. To do this, check the output from running the first node, somewhere near the top there should be 'enode://'. Copy that and the long string that follows

![''](./Screenshots/6.png)


#### Connect to the MyCrypto app

In order to send cryptocurrency between our two accounts we will need to use the MyCrypto app.  
Firstly, connect your local network with the app. Name the network and node whatever you please, but make sure the network type is set to custom AND the Chain ID is set to the 3-digit number you created earlier. 

![''](./Screenshots/7.png)


Next, log into the wallet for the first node. From here we will be able to send and receive transactions. Copy and paste the address to the second node in the 'To Address' bar, input how much you would like to send and press 'Send Transaction'.  

![''](./Screenshots/8.png)

Congrats, you have made yourself filty rich in fake money!