# Crop_Disease_Prediction
Blockchain based prediction services for crop diseases using Flask and web3.py 

This is an implementation of a project paper which can be found in the repo.

The python packages required are as follows:

->For backend and frontent management:			flask

->For setting up deep learning network:		      	tensorflow
						      	numpy
							opencv-python
							keras
							
->For connecting to ipfs api:			        ipfshttpclient

->For deploying and interacting with contracts:		web3
						        py-solc-x

Setting up the project:
1) Deploy smart contract by running "python3 deploy.py"(Make sure that ganache is running in the background and required account address and private key have been added in the file).
2) Run "ipfs daemon" in another terminal for helping with image uploads(ipfs should be installed beforehand)
3) Run "python3 app.py" and open "http://127.0.0.1:5000/" on any browser to see its working.

access_blockchain.py has been made to ensure that app.py is not too long.It handles all the transactions and calls to the smart contract.

contract.sol is the main contract and it maintains all the solution.Compiled_code.json is created by py-solc-x (python solidity compiler) to access the compiled contract.

model.pkl contains the deep learning model which was trained beforehand.

Images named predict.jpeg, before1.jpeg,after1.jpeg etc were used for quick demonstration, to try other images please bring them into the directory where app.py resides.

The project was last tried on Dec 20 2021 and it worked fine. If an error occurs with ipfs please install an older version of ipfs (https://docs.ipfs.io/install/command-line/#official-distributions) with version preferably 0.8.0.
