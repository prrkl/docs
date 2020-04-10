# ETH2 Network Monitoring: Project Overview

Deploy a swarm of semi-autonomous network agents masquerading as an Eth2 node that communicate with a command & control service. This service will collect, aggregate and analyze information from individual agents to evaluate network health. Additionally the command & control service can coordinate the agents to perform attacks to the network, evaluating the security and resilience of the protocol.

## Goals

Monitor network health in real-time
* Realtime stats
    * message propagation times
    * pings/status of each peer
    * ENR changes of each peer (ip rotation, seqnr changes)

* Analysis
    * How quick can we discover peers?
    * What percent of peers are pingable?
    * How fast are messages propagated?
    * What does the network topology look like?

* Provide feedback to the network specification

## Design Overview

![](https://i.imgur.com/VOhqH2f.jpg)

> Note: Depending on how clients decide to treat non beacon chain nodes, the Eth2 node may or may not be needed.

### Command & Control Service
 - send commands to agents
 - collect data from agents

### Eth2 Node (if needed)
 - REST API available for agents to query so they can can answer requests from real nodes on the network

### Network Agent
 - network crawler
 - send network data to command & control service
 - accept remote commands from command & control service
 - libp2p networking component

## Costs (TBD)
- servers and ip addresses

## Future Work
Evaluate weaknesses in the Eth2 network
* What attacks could stall consensus?
* What is the cost of these attacks?

Propose fixes
* Findings will be used to harden the spec










