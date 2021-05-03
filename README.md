# Hetero_K8s_Cluster_Ansible
This aims at provisioning a multi-node heterogeneous kubernetes cluster using ansible playbook on AWS. The cluster will have mutli-os worker nodes (windows and linux) and a linux master node, making it a heterogeneous cluster. The cluster will have mutliple operating support as worker nodes. You can schedule a windows application as well as linux application on windows worker and linux worker respectively.
## Need for windows support in Kuberentes cluster
Windows applications constitute a large portion of the services and applications that run in many organizations. Windows containers provide a modern way to encapsulate processes and package dependencies, making it easier to use DevOps practices and follow cloud native patterns for Windows applications. Kubernetes has become the defacto standard container orchestrator. Organizations with investments in Windows-based applications and Linux-based applications don't have to look for separate orchestrators to manage their workloads, leading to increased operational efficiencies across their deployments, regardless of operating system.
## Features
- Full automation using the playbook
- Provisioning on AWS 
- Mutli-Node heterogeneous cluster
- Cluster supports linux as well as windows workloads
- Kubernetes dashboard configured
## Installation
### Prerequisites
- Create a ansible vault for aws access key ID and secret key
- Must have dynamic inventory configured
### To run master playbook (Master Node)
ansible-playbook --vault-id .....@prompt Master.yml
### To run worker playbook(Windows Worker Node)
ansible-playbook -i hosts --vault-id .....@prompt Windows-worker.yml
### To run worker playbook(Linux Worker Node)
ansible-playbook --vault-id .....@prompt Linux-worker.yml
