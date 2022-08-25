# Blockchain-for-Smart-Territoires
Blockchain technology security system for transactions in data platforms for the development of smart territories

# Prerequisites for the project

To deploy the project, you must first have some tools installed:
- NodeJs 16 => https://nodejs.org/
- Truffle 5 => https://trufflesuite.com/docs/truffle/quickstart/
- Ganache => https://trufflesuite.com/ganache/
- Metamask => https://metamask.io/

# Import the ganache acounts into Metamask, as shown in the following video:
https://www.youtube.com/watch?v=con8UhF_fVU

# Deploy smart contract on ganache network
1- Launch Ganache
2- Inter in the project Directory (the blockchan directory)
3- Launch a terminal and attache truffle framework to ganache network--> truffle console --network ganache
4- Compile the contracts --> migrate --compile-all --reset

# configure and start the back-end API
1- Create a Mongo DB account: https://www.mongodb.com/atlas/database
2- Create and configure a cluster, and copy the connexion string, as shown in this tutorial: https://openclassrooms.com/fr/courses/6390246-passez-au-full-stack-avec-node-js-express-et-mongodb/6466348-configurez-votre-base-de-donnees

# Make sure you follow the tutorial correctly

3- Paste the connexion string (the DB_CONNECTION) in the .env file, in the back-end-api directory
4- Inter in the back-end-api directory and launch a terminal
5- Install the project dependencies with the command: npm install
6- Start the back-end-api with the command: npm start

# configure and start the client App
A- Import the ganache contracts addresses into the client App
1- Go to ganache, and click on CONTRACTS
2- Click on each contract, copy the address and pass it in where it is necessary in the client App:
Ex: in client/src/components/Log/SignInForm, in the top of the file, we will have the User Identity contract address like this: let userIdentityContractAddress = '0x0Bd59f24205D6E13Dbbb46a5D0f29d9A6bC7515f';

Note that, some contract addresses are necessary in client/src/components/Log and in client/src/components/pages
3- Inter in the client directory and launch a terminal
3- Install the project dependencies with the command: npm install
4- Start the lient App with the command: npm start
5- When the App is launched in the browser, make sure you are on the correct network in metamask(the network where you have imported the ganache addrresses).
6- If the App does'nt launched,launch a browser and try with the URL localhost:3000/
Note: The first time the App is launched, you have to register a Role Assigner.

For that, you mus do some modification in the codes.
1- Go to client/src/components/pages/Roles/AddRoles
2- Comment the function verifyUserRole(), at line 162
3- Call the getUsers function at line 179 like this: getUsers()
4- Go to the App in the browser. In Role Module, register a Role Assigner with Role "Role Assigner" and data category "Any data".
5- After that, Return the codes to the initial version (comment the function call getUsers() at line 179 and uncomment the function verifyUserRole() at line 162).
