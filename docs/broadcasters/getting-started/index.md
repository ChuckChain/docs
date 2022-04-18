---
title: Quickstart
---

# Overview

The getting started tutorial will walk you through the steps required to set up Project Aqueduct, send a
livestream into the Livepeer Network for transcoding, and play it back
inside your application.

> Note: for the sake of this guide, we'll be livestreaming using the Rinkeby
> test network. You can think of this network like a sandbox environment for
> testing your livestreams. If you're livestreaming in a production setting make
> sure to change the network to `arbitrum-one-mainnet`. Learn more about supported networks,
> including Arbitrum mainnet and Arbitrum Rinkeby,
> [here](/installation/connect-to-arbitrum#supported-networks).

## Pre-requisites

- Make sure you have `livepeer` [installed](/installation/install-livepeer/)
- Make sure you have access to an
  [Arbitrum JSON-RPC URL](/installation/connect-to-arbitrum)

## Install Aqueduct

First, you will need to [install the Aqueduct client software](/broadcasters/getting-started/install). This will provide you with a Livepeer broadcaster node and the full-featured MistServer toolkit, which you can use to stream using the Livepeer Network or your own onchain or offchain transcoding capacity.

> **Note:** If you're interested in using a hosted service, [Livepeer Video Services](https://livepeer.com) provides a hosted gateway.

## Start your broadcaster and add funds

To stream into the network, you will need to [start your broadcaster](/broadcasters/getting-started/run-broadcaster) and [supply it with funds](/broadcasters/getting-started/deposit-broadcasting-funds) so that you are able to pay orchestrators for their services.

## Ensure that your broadcaster's private key is stored safely

When your broadcaster starts for the first time, it will generate a wallet for you. The key will be stored in `~/.lpData/<chain flag, e.g. arbitrum-one-mainnet>/keystore`. It is imperative that you safely store the keystore file in a secure locations outside the container; if you lose it you will lose access to your funds.

**If you delete the Docker container that the broadcaster is running in, this file will be deleted. It can be recovered from a stopped container, but not from a deleted container** 


## Launch the Aqueduct Dashboard and start your first stream

Once your broadcaster is running, you can [launch the Aqueduct Dashboard](/broadcasters/getting-started/run-broadcaster#viewing-the-aqueduct-dashboard) and [start your first stream](/broadcasters/getting-started/create-livestream).

## Set up monitoring 

To ensure that your instance of Aqueduct is healthy, it's helpful to set up monitoring. Two particularly important monitoring tools are [a Grafana dashboard](/broadcasters/how-to-guides/managing-broadcasters/monitoring) and a [low funds alert](/broadcasters/how-to-guides/managing-broadcasters/low-funds-alert) to let you know when your broadcaster is running low on funds.
