# Kubernetes Research Lab for Raspberry Pi clusters

This project's goal is to ease deployment (and re-deployment) of Kubernetes in a Raspberry Pi cluster. 

## Tested Configuration 

I'm building this to work in my own home lab that consists of:

* 4 Raspberry Pi model 4s with 4GB of RAM each
  * Running Ubuntu 19.10
* Connected to the same switch
* With internet access

## Usage 

Right now it's all ansible, although I do hope to wrap that with some additional logic down the road. 

`ansible-playbook -i inventory site.yaml`

## Kubernetes Config 

Right now it deploys a basic cluster with a single control node and 3 workload nodes. The SDN is currently Calico. Under the covers it uses kubeadm to handle the deployment and configuration of the cluster.