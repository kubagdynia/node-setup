# Kadena Node Installation

**Note**: this guide assumes your machine is running Ubuntu 20.04 or 22.04, that you have
`sudo` privileges, that you've bought a proper Domain Name and are pointing it
at the Public IP Address of your machine.

### Version

[2.25](https://github.com/kadena-io/chainweb-node/releases/tag/2.25)

### Installation

```bash
wget https://raw.githubusercontent.com/kubagdynia/node-setup/master/installnode.sh
sudo bash installnode.sh
```

### Installation without proper Domain Name

```bash
wget https://raw.githubusercontent.com/kubagdynia/node-setup/master/installnodeip.sh
sudo bash installnodeip.sh
```

And follow the instructions.

A log of the install is stored in `/tmp/install.log` if there were any errors.

### Update

```bash
cd /root/kda
systemctl stop kadena-node
rm chainweb-node
wget https://github.com/kadena-io/chainweb-node/releases/download/2.25/chainweb-2.25.ghc-9.6.5.ubuntu-22.04.7b2fb3b.tar.gz
tar -xvf chainweb-2.25.ghc-9.6.5.ubuntu-22.04.7b2fb3b.tar.gz
systemctl start kadena-node
```
