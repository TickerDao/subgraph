# The Graph Subgraph

This repository contains the code for deploying the L2 Storage subgraph on The Graph. Below, you'll find the necessary commands to install dependencies, build the code, and deploy the subgraph.

## Prerequisites

Ensure you have the following installed on your system:
- Node.js (version 12.x or higher)
- Yarn (version 1.x or higher)
- Docker (optional, only if used for the local Ethereum node)
- Graph node running locally

## Start a Local Graph Node

The Graph Node, IPFS, and Postgres can be set up locally using Docker. Clone this repo [graph-node](https://github.com/graphprotocol/graph-node) and edit the `ethereum` field in the `docker-compose.yml` with the preferred chain

Start the services:

```bash
docker-compose up
```

## Installing Dependencies

First, clone this repository and navigate to the project directory:

```bash
yarn install
```
## Configuration

Before building and deploying the subgraph, make sure to update the subgraph.yaml file with the correct details for your subgraph, such as contract address and start block.

## Generate Code from ABI
To generate code from the ABI files, use:

```bash
yarn codegen
```

## Create the Subgraph
Run the following command to create the subgraph on your local Graph Node:

```bash
yarn create-local
```


## Building the subgraph
To build the subgraph, run the following command:

```bash
yarn build
```

This will generate the subgraph code from the subgraph.yaml configuration file.

## Deploying the subgraph
Finally, deploy the subgraph with the following command:

```bash
yarn deploy-local
```