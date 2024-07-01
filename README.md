# Nubit

We suggest you use the [official documentation](https://docs.nubit.org/developer-guides/introduction). </br>
Below are the minimum system requirements for the project.</br>
CPU: 1 Core </br>
RAM: 500mb </br>
SSD: 40Gb </br>
OS: Ubuntu 22.04 </br>


### Server preparation + install docker+docker-compose.
```
sudo apt update && sudo apt update -y sudo apt install curl git wget build-essential jq screen -y
```

### Install node and run.
```
screen -S nubit
curl -sL1 https://nubit.sh | bash
```

Collapse the screen:
```
CTRL +A +D
```

### Backup mnemonic,address,pubkey:
```
cat $HOME/nubit-node/mnemonic.txt
$HOME/nubit-node/bin/nkey list --p2p.network nubit-alphatestnet-1 --node.type light
```
⚠️⚠️⚠️ PLEASE SAVE! ⚠️⚠️⚠️

### Registering a node:
```
We are going to the [site](https://alpha.nubit.org/)
We insert the pubkey that we took above in step 3.
Click verify.
```

### Useful commands:
```
cat $HOME/nubit-node/mnemonic.txt - backup mnemonic
$HOME/nubit-node/bin/nkey list --p2p.network nubit-alphatestnet-1 --node.type light - backupaddress,pubkey
screen -r nubit - check logs
```

### Remove node:
```
rm -rf .nubit-light-nubit-alphatestnet-1
rm -rf nubit-node
rm -rf .nubit-validator
```
