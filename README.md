# Prufus
Shell script to install a [Prufus Masternode](http://prufus.com/) on a Linux server running Ubuntu 16.04. Use it on your own risk.

***
## Installation:
```
wget -q https://raw.githubusercontent.com/zoldur/Prufus/master/prufus_install.sh
bash prufus_install.sh
```
***

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open the **Prufus Desktop Wallet**.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **10000** **PRUFUS** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  **Tools -> "Open Masternode Configuration File"**
8. Add the following entry:
```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* Output index:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
12. Select your MN and click **Start Alias** to start it.
13. Alternatively, open **Debug Console** and type:
```
startmasternode "alias" "MN1"
```
***

## Usage:
```
prufus-cli mnsync status
prufus-cli getinfo
prufus-cli masternode status #This command will show your masternode status
```

Also, if you want to check/start/stop **prufus** , run one of the following commands as **root**:

```
systemctl status Prufus #To check the service is running.
systemctl start Prufus #To start prufus service.
systemctl stop Prufus #To stop prufus service.
systemctl is-enabled Prufus #To check whetether prufus service is enabled on boot or not.
```
***

## Donations:  

Any donation is highly appreciated.  

**PRUFUS**: EHkqw6HEeGy3c17xK6Mh1ohyzWik51HG66  
**BTC**: 3MQLEcHXVvxpmwbB811qiC1c6g21ZKa7Jh  
**ETH**: 0x26B9dDa0616FE0759273D651e77Fe7dd7751E01E  
**LTC**: LeZmPXHuQEhkd8iZY7a2zVAwF7DCWir2FF

