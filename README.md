Development
Installation & setup
Make sure you have truffle installed on your computer.

# Install Truffle globally
npm install -g truffle
# Install truffle dependencies in root directory (./terratrack)
npm install
Ensure you create an .env file in root directory. Then to access the Ethereum network/node, create a project on infura and copy-paste the infura project-id url in .env with a variable name REACT_APP_INFURA_MATIC_TESTNET or REACT_APP_INFURA_RINKEBY.

REACT_APP_INFURA_MATIC_TESTNET=https://polygon-mumbai.infura.io/v3/YOUR_PROJECT_ID
REACT_APP_INFURA_RINKEBY=https://rinkeby.infura.io/v3/YOUR_PROJECT_ID
Paste the 12 word Secret Recovery Phrase of your (preferably newly generated and testnet-only) MetaMask wallet in .env with the variable name REACT_APP_MNEMONIC. This will be loaded by truffle at runtime, and the environment variable can then be accessed with process.env.REACT_APP_MNEMONIC.

REACT_APP_MNEMONIC=for example put your twelve word BIP39 secret recovery phrase here
OR

To develop on ganache blockchain, open ganache and import the accounts by adding your ganache private keys in MetaMask.

$ ganache-cli
Deployment
To deploy the smart contracts on blockchain networks, follow the given truffle command below.

# truffle migrate --network NETWORK_NAME
truffle migrate --network matic_testnet
truffle migrate --network rinkeby

# --reset: Run all migrations from the beginning, instead of running from the last completed migration.
For more information, read truffle docs.

React client
Start react app.

# cd into client directory
cd client

# Install dependencies
npm install

# Start the app
npm start
Starting the development server...
