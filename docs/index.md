# The Grid

A digital frontier?

## Overview

 * Turns hosts into a cluster of generic job runners
 * Jobs are containerized Unix processes with their own system environment
 * Jobs get service discovery and distributed coordination
 * Central job scheduling logic is written by you

The Grid is a distributed, container-based Unix process scheduling framework and service platform. It turns a set of networked hosts into a mostly homogeneous grid of nodes ready to run heterogeneous jobs. In this case, jobs are simply containerized Unix processes that can be long-running daemons (services) or one-off tasks, all with access to basic primitives for distributed coordination and discovery.

It acts as the Layer 0 of Flynn, made up of a small number of sub-components that together create a core platform for Flynn Layer 1 components or any other system components.

You can broadly compare The Grid to Mesos, but with a more modular, expressive approach. Similar to Mesos, you have to use or write your own scheduler(s). The Grid does not provide a scheduler, just the APIs to work with cluster state, interact with jobs, and submit jobs to hosts. It also comes with a service discovery system and a lower-level consistent datastore for distributed coordination and configuration, which are used by components of The Grid and can be used by anything running on The Grid.

## Using The Grid

TODO: High level description of process of using The Grid, then link to Getting Started


## How The Grid Works

TODO: High level architecture and components, then link to docs for individual components