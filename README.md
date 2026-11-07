## Cortana-Rodney-Homelab-

    Aplication and Network-Infrastructure laboratory
    ANIL

    Laboratório de Aplicações e Infraestrutura de Redes
    LAIR

## About

ANIL (or LAIR, in Portuguese), is a selfhosted server that was developed initially to store my data and create a synced backup for all my devices. Eventually the project grew a little and the proposal changed for a multifunction automation and central toolbox for everything in my life. Literally Everything.

## How it works

My homelab can be divided in two nodes with distinct functions, the Cortana and Rodney.
Cortana is a network-infrastructure laboratory server, hosted on an old LG laptop (A410G from 2011) with a incredible i3 390M processor, 8GB of RAM and 220GB of storage. An absolute beast.

![The Beast itself](assets/cortana/cortana-pic1.jpg)
_the beast itself_

So, what's her function? Everything client and network related, like: services responses, requests, DNS records, reverse proxy, VPN tunnel, etc. It's all Cortana's work.

And Rodney? The Application and database server, the client never requests directly to him, his role is store the services, containers, databases, production projects, etc; To access the services, Cortana talks to him. He's the backend guy.

## Repository structure

```
├── assets
│   └── cortana
│       ├── cortana-pic1.jpg
│       └── cortana-pic2.jpg
├── cortana
│   ├── daemons
│   ├── dotfiles
│   ├── scripts
│   ├── services
│   ├── specs.yaml
│   └── system-configs
├── README.md
└── rodney
    ├── daemons
    ├── dotfiles
    ├── scripts
    ├── specs.yaml
    └── system-configs

13 directories, 5 files
```

## Network Infrastructure

I designed a diagram to represent the network hierarchy and infrastructure.

![Network Diagram](assets/cortana/infrastructure.png)
_It is in Portuguese, but i think the figures make it more understandable_
