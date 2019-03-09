# Nutcoin
The time is now!

Getting started
Use the following instructions to mine a block.

Open your wallet, and make sure your wallet is connected with a node. 
Your wallet is connected when you see the icon Wallet connections Scrypt and SHA256 in the lower right corner of your wallet.

The message “Syncing Headers (0,0%)” will disappear once you mine your first block.

Close your wallet and create the file nutcoin.conf in the folder “%APPDATA%\nutcoin\”.

Paste the following text into nutcoin.conf and save the file.

rpcuser=rpc_nutcoin
rpcpassword=YourPAssword
rpcallowip=127.0.0.1
rpcport=7011
listen=1
server=1
addnode=node1.walletbuilders.com

Open your wallet.

Create a .bat file named mine.bat in the same folder where you extracted nutcoin-cli.exe and paste the following text into mine.bat.

@echo off
set SCRIPT_PATH=%cd%
cd %SCRIPT_PATH%
echo Press [CTRL+C] to stop mining.
:begin
 nutcoin-cli.exe generate 1 1000000000
goto begin 

Save the file.

Execute mine.bat to start mining your first block.

It will take about +/- 30 minutes to mine your first block, depending on your computer hardware.
