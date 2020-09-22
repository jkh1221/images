# Installation and Operation on “DApp For Sharing PDF on Smart Contract”

This is written for installation and operation on “DApp For Sharing PDF on Smart Contract”
### 1.	Node Package Application Download And Installation

 - If you have not yet installed node application, do as following  
  	 - Go to https://nodejs.org/en/download/ and Download  
    ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/node.PNG)  
  	 - Install the downloaded msi as keeping default.  

### 2.	Ganache Application Download , Installation and Configuration
  -	Go to https://www.trufflesuite.com/ganache and Download  
  -	Install the downloaded Ganache-2.1.2-win-x64.appx  
  -	Run the app and Have Configuration as following ( set port at 8545)  
    - Click “Setting” icon shown on top-right and Go to SERVER tab  
    - Change 7545 to 8545 on “PORT NUMBER”  

### 3.	Metamask Chrome Extension Installation and Configuration  
  -	Run Google Chrome Browser ( You have to install it, if you don’t have )  
  -	Click “Setting” on the top-right of chrome browser and Go to “Extensions” menu as following  
  
     ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/meta1.PNG)  
     
  -	Type “Metamask” on seach box and Get “MetaMask …” shown as fox icon on screen  
  -	Click it and Install Extension  
  -	Now you can look “Fox” icon on Chrome Browser.  
  -	Click “Fox” icon on chrom browser to run it.  
  -	Create new account and Set your own password to login to blockchain network.  
  -	Select your favourite network there as following.  
    For example “Main Ethereum Network” for real network , “Localhost 8545” for development and test. In my case I did “Localhost 8545”  
 
      ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/meta2.PNG)  

  -	Import account from Ganache. (Because all transactions need gas for both of test and development, you have to make a deposited account)
    - create account  
 
     ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/meta3.PNG)  


    - Go to “import” tab , Paste new account’s privatekey from Ganache and Click “import” button  

     ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/meta4.PNG)  

### 4.	Yarn Download and Installation

  -	Go to https://yarnpkg.com/lang/en/docs/install/#windows-stable And Click “Download Installer” button to download  
  -	Install “yarn-_.__.msi” file  

### 5.	Unzip project source file (pdfsharingDApp.rar) and move to your own location.
### 6.	Installation Dependencies one by one on command prompt as following
      npm i create-react-app  
      npm install react-scripts --save  
      npm install react-bootstrap --save  
      npm install fs-extra --save  
      npm install ipfs-api --save  
      npm install web3@^1.0.0-beta.26 --save  
      npm install -g create-react-app  
      yarn install  
      yarn start  

   Now you can get that your web application runs on chrome browser.

### 7.	Distribution smartcontract on local blockchain network running on Ganache and Metamask.
  - Go to https://remix.ethereum.org/ and Click “Open files”  
  - On “file open dialog”, Select to  “{your location}\pdfsharingDApp\src\contracts\StoreHash.sol”  
  - Click “compile ___”  
  
       ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/remix1.PNG)  
  
  - Go to “DEPLOY & RUN TRANSACTIONS” tab and Select “Web3 Provider” on Environment selectbox  
    Now you can get an account list created above 3.9 on Metamask 
    
      ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/remix2.PNG)  

  - Deploy the app  
  - Initialize your smartcontract app to add some accounts  
     Paste the following line by line on input box beside “Add Acount” button And Click “Add Acount” button each time.  
     0x89C80bA6C09048BE832C129Ad3b65d144289cA16, hattori, 1df7deb64b2712f0d2a2161953d2836d1f7fd6b645c8c94f47a5a6faa48cd31f  

     0x2FDb91Da9A591786373852CdDbb001C0FF30D0c3, andrew, 68d70d478f330c34ff617355247f54695c3c1d370aa4d3a23608562d5262aa78  

     0xddAe99490C4C736d6AE7De5fCa30051F22A1ACd8, seito, 4d1f017426b1d9a970af29859559845a09fd1a3455a1feac0ace027c49b8f817  

     0xD2BE7f3dCd66AFFf6114087B58556a25E2b065C6, pablo, c6db29471742c1f116fff5ef5c9bc1336ef598b359c40933b11a5bb42a9d89e6  

     ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/accounts.PNG)  
 

### 8.	Change the project configuration for current dapp And Refresh Browser.
  - copy the distributed contract’s address on remix deploy screen  
  - change the “address” value  in  “storehash.js” of project and Save file  
 
      ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/config.PNG)  

  - copy the distributed contract’s ABI on remix compile screen  
  - change the “abi” value  in  “storehash.js” of project and Save file  

     ![Image of Yaktocat](https://github.com/jkh1221/images/blob/master/readme/remix3.PNG)  
 

### 9.	Refresh Browser to press “F5” key on keyboard

That’s all And Thanks 

