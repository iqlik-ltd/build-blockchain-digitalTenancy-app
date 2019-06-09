*Read this in other languages: [中国語](README-cn.md),[日本語](README-ja.md).*

# Build Blockchain Insurance Application

This project showcases the use of blockchain in insurance domain for claim processing. In this application, we have four participants, namely insurance, police, repair shop and the shop. Furthermore,
each participant will own its own peer node. The insurance peer is the insurance company providing the insurance for the products and it is responsible for processing the claims. Police peer is responsible for verifying the theft claims. Repair shop peer is responsible for repairs of the product while shop peer sells the products to consumer. The value of running this network on the IBM Blockchain Platform is that 
you can easily customize the network infrastructure as needed, whether 
that is the location of the nodes, the CPU and RAM of the hardware, the
endorsement policy needed to reach consensus, or adding new organizations and members to the network.  

*Note:* This code pattern can either be run locally, or connected to the IBM Blockchain Platform. <b>If you only care 
about running this pattern locally, please find the local instructions [here](./README-local.md).</b>

Audience level : Intermediate Developers

When the reader has completed this code pattern, they will understand how to:

* Create a Kubernetes Cluster using the IBM Kubernetes Service
* Create an IBM Blockchain service, and launch the service onto the Kubernetes cluster
* Create a network, including all relevant components, such as Certificate Authority, MSP (Membership Service Providers),
  peers, orderers, and channels.
* Deploy a packaged smart contract onto the IBM Blockchain Platform by installing and instantiating it on the peers.
* Use the connection profile from IBM Blockchain Platform to create application admins, and submit transactions from our 
client application.
* View transaction details on our channel from IBM Blockchain Platform.

## Application Workflow Diagram
![Workflow](images/app-arch.png)

1. The blockchain operator creates a IBM Kubernetes Service cluster (<b>32CPU, 32RAM, 3 workers recommended</b>) and an IBM Blockchain 
Platform 2.0 service.
2. The IBM Blockchain Platform 2.0 creates a Hyperledger Fabric network on an IBM Kubernetes 
Service, and the operator installs and instantiates the smart contract on the network.
3. The Node.js application server uses the Fabric SDK to interact with the deployed network on IBM Blockchain Platform 2.0.
4. The React UI uses the Node.js application API to interact and submit transactions to the network.
5. The user interacts with the insurance application web interface to update and query the blockchain ledger and state.

## Included Components
*	[IBM Blockchain Platform V2 Beta](https://console.bluemix.net/docs/services/blockchain/howto/ibp-v2-deploy-iks.html#ibp-v2-deploy-iks) gives you total control of your blockchain network with a user interface that can simplify and accelerate your journey to deploy and manage blockchain components on the IBM Cloud Kubernetes Service.
*	[IBM Cloud Kubernetes Service](https://www.ibm.com/cloud/container-service) creates a cluster of compute hosts and deploys highly available containers. A Kubernetes cluster lets you securely manage the resources that you need to quickly deploy, update, and scale applications.


## Featured technologies
* [Hyperledger Fabric v1.4](https://hyperledger-fabric.readthedocs.io) is a platform for distributed ledger solutions, underpinned by a modular architecture that delivers high degrees of confidentiality, resiliency, flexibility, and scalability.
* [Node.js](https://nodejs.org) is an open source, cross-platform JavaScript run-time environment that executes server-side JavaScript code.
* [React](https://reactjs.org/) A declarative, efficient, and flexible JavaScript library for building user interfaces.
* [Docker](https://www.docker.com/) Docker is a computer program that performs operating-system-level virtualization. It was first released in 2013 and is developed by Docker, Inc.


