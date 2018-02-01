# Ethereum-full-node

Run the ETH fullnode in a Docker container that is provisioned with Vagrant and Ansible.

## Requirements

- Vagrant
- Vagrant-disksize

```
vagrant plugin install vagrant-disksize
```

## Usage

Dockerfile gets provisioned to `/vagrant/storage/Dockerfile`

        # create volume
        sudo docker volume create ethereum-blockchain
     
        # either run in foreground
        sudo docker run --name ethereumd -v ethereum-blockchain:/root/ -it r3lik/ethereum-full-node --fast --cache=512

        # or in background
        sudo docker run -d --name ethereumd -v electroneum-blockchain:/root/ -it r3lik/ethereum-full-node --fast --cache=512
