# blockchain_test

This is a testing blockchain, created using Python. It's a direct copy of the one shown here: https://www.geeksforgeeks.org/create-simple-blockchain-using-python/
As of now, the blockchain can be run locally, can mine blocks(http://localhost:5000/mine_block), can view blocks(http://localhost:5000/get_chain) and can show the validity of the chain(http://localhost:5000/valid).
To do any of the shown above, the program must be run in an Pycharm(Probably other IDE's will also work, but I've yet to try it). After the blockchain is run, open any of the links in a browser and the information will displayed.

18.02.2023
Added the ability to store the blocks in a json format file. The code will check if the file exists. If it doesn't, it will create it. If it does exist, it is supposed to use it and to continue the blockchain from the stored information in the file. Currently is broken. Will need to continue working on it later.

19.02.2023
Fixed the blockchain saving and usage. Now, the code will search for a blockchain file. If it exists, it will continue the blockchain from the last block in the file and add any new ones to it.

20.02.2023
Added a resolver to the Blockchain class. It's function is, if the blockchain is found to be invalid, to seek out a valid chain and replace the invalid one. It requires another valid blockchain to work, so it currently doesn't.

25.02.2023
Reverted some of the changes, since the program was fully broken and I didn't understand them myself. Also, changed some of the functions in it. Now, the resolver method should work, if there are more nodes in the network.

27.02.2023
Reworked the resolver method. Added a /resolve_conflicts route to the app. Currently works on a preset number of nodes, all on my system. Will work on adding a Node class, if it's possible. The new links are http://localhost:5000/resolve_conflicts and http://localhost:5000/get_chains is the old link, but I didn't add it last time. Also, added the option to add and remove nodes.

28.02.2023
Added a class Node. It is where the nodes will be stored. It has methods to add, remove, block nodes, aswell as to return all valid, non-blocked and non-removed nodes.
