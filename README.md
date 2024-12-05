# open5gs-Ueransim

```sudo apt-get update```
```sudo apt-get install -y gnupg wget curl```

**Install Mongodb : **

```wget -qO - https://www.mongodb.org/static/pgp/server-6.0.asc | sudo apt-key add -```
```echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list```
```sudo apt update```

// Try to Use **VMWare** (In VirtualBox it can create an issue while downnloading mongodb)

for ubuntu 22.04 there is no official version of monogdb

So use forceful installation of libssl1 using the commands -> 

```echo "deb http://security.ubuntu.com/ubuntu focal-security main" | sudo tee /etc/apt/sources.list.d/focal-security.list```

```sudo apt-get update && sudo apt-get install libssl1.1 ```

Then delete the focal-security list file you just created:

```sudo rm /etc/apt/sources.list.d/focal-security.list```

```sudo apt install -y mongodb-org mongodb-org-database```

```sudo systemctl start mongod```

```sudo systemctl enable mongod```

// Check the stutus of mongod -> (It should be enables)

```sudo systemctl status mongod```

**After the Installation of mongod -> Now install nodeJs using the commands ->**

```curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -```

```sudo apt install nodejs```

**Install Open5GS using these commands -> **

```sudo add-apt-repository ppa:open5gs/latest```

```sudo apt-get install -y software-properties-common```

```sudo apt-get -y update && apt install -y open5gs```

**Install the webui**

```curl -fsSL https://open5gs.org/open5gs/assets/webui/install | sudo -E bash -```

**Steps to install UERANSIM ->**

```sudo apt install make gcc g++ libsctp-dev lksctp-tools iproute2 git```

```sudo snap install cmake --classic```

```sudo git clone https://github.com/aligungr/UERANSIM```

```cd ~/UERANSIM```

```sudo make```
