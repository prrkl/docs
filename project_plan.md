# Project Plan

Deploy a swarm of semi-autonomous network agents masquerading as an Eth2 node that communicate with a command & control service. This service will collect, aggregate and analyze information from individual agents to evaluate network health.  Additionally, the server will be capable to sending commands to the agents in order to coordinate attacks.

## Goals

Monitor network health in real time
* Realtime stats: latencies, propagation, forkiness, etc

Evaluate weaknesses in the Eth2 network
* What attacks could stall consensus?
* What is the cost of these attacks?

Propose fixes
* Findings will be used to harden the spec

## Design Overview

![](https://i.imgur.com/VOhqH2f.jpg)

### Command & Control Service
 - send commands to agents
 - collect data from agents

### Eth2 Node
 - REST API available for agents to query so they can can answer requests from real nodes on the network

### Network Agent
 - network crawler
 - send network data to command & control service
 - accept remote commands from c&c service
 - libp2p networking component (Mothra)


## Costs (TBD)
- servers and ip addresses











