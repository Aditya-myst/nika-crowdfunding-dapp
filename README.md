# Project Title
Nika Crowdfunding dApp


# How to Install and Run the Project
**Clone the repository**

```javascript
https://github.com/Aditya-myst/nika-crowdfunding-dapp
```

**cd into the Client Folder**

**Install the dependencies**

```javascript
npm install
```

```bash
cd nika-crowdfunding-dapp && cd client
```

**Start the development server**

```javascript
npm run dev
```
**Port to Run the Website**

```
http://localhost:3000
```
or any other port available to view it in the browser.

- No required input/output files.

- Ensure you are using the `Goerli Test Network` on your `metamask wallet` or any other wallet when connecting.# How Nika-Crowdfunding-Project was setup with Thirdweb, Hardhat, and Vite

## Technologies
- Thirdweb (Web3 Framework)
- Hardhat (Smart Contract development environment)
- Vite (React Framework)

## Contract setup
1. Run `npx thirdweb@latest create --contract` to create a new contract project.
2. Install `dotenv` with `npm install dotenv`.
3. Get the private key from your MetaMask account.
4. Find the endpoint for the network you want to use (e.g. Goerli). You can find the endpoint at https://www.ankr.com/rpc/eth/eth_goerli/.
5. Add the following code to your `hardhat.config.js` file:

```hardhat
defaultNetwork: 'goerli',
networks: {
hardhat: {},
goerli: {
url: 'https://rpc.ankr.com/eth_goerli',
accounts: [0x${process.env.PRIVATE_KEY}]
}
},
```

6. Run `npm run deploy` to deploy the contracts to the network.

## Client setup
1. Run `npx thirdweb@latest create --app` to create a new client project.
2. Choose the app name with `./`.
3. Select EVM (or Solana as needed).
4. Select Vite to replace using `create-react-app` for React.
5. Select JavaScript (or TypeScript as needed).
6. Install `react-router-dom` with `npm install react-router-dom`.
7. Run `npm run dev` to check your build so far.
8. Delete the `src` folder.
9. Create a new `src` folder and an `index.js` file.
10. Create a new `App.js` file with a React function component using the `rafce` snippet (ES7).
11. Convert `index.js` to `main.jsx` and `App.js` to `App.jsx`.
12. Install Tailwind CSS with Vite by running `npm install -D tailwindcss postcss autoprefixer`.
13. Run `npx tailwindcss init -p` to create the configuration files for Tailwind CSS.
14. Add the following code to your `tailwind.config.cjs` file:

```tailwind
/** @type {import('tailwindcss').Config} /
module.exports = {
content: [
"./index.html",
"./src/**/.{js,ts,jsx,tsx}",
],
theme: {
extend: {},
},
plugins: [],
}
```
