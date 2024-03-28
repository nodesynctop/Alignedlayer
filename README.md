# Alignedlayer

Website: https://alignedlayer.com/

Twitter: https://twitter.com/alignedlayer

Explorer: https://explorer.nodesync.top/Alignedlayer-Testnet/staking

Faucet: https://faucet.alignedlayer.com/

# 1. Minimum hardware requirement

2 Cores, 4G Ram,  80G SSD, Ubuntu 22.04

# 2. Auto Install
```
sudo apt install curl -y && source <(curl -s https://nodesync.top/alignedlayer_auto)
```
## 2.1 Wallet
Add New Wallet Key - Save seed
```
alignedlayerd keys add wallet
```
Recover existing key
```
alignedlayerd keys add wallet --recover
```
List All Keys
```
alignedlayerd keys list
```
## 2.2 Query Wallet Balance

```
alignedlayerd q bank balances $(alignedlayerd keys show wallet -a)
```
## 2.3 Check sync status
False is synced

```
alignedlayerd status 2>&1 | jq .sync_info
```
## 2.4 Create Validator
**Obtain your validator public key by running the following command:**
```
alignedlayerd comet show-validator
```
**The output will be similar to this (with a different key):**
{"@type":"/cosmos.crypto.ed25519.PubKey","key":"lR1d7YBVK5jYijOfWVKRFoWCsS4dg3kagT7LB9GnG8I="}

**Then, create a file named ```validator.json``` with the following content:**









