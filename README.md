# homelab

I was running a bunch of different services w/ proxmox for my homelab on a minipc. It started to get a little annoying to have to do the same setup for each little lxc service, bootstrap debian, setup sync scripts for the app, etc.

So here we are, this repo is a WIP but working towards a Flux-controlled k8s installation instead. Just gonna run a single k8s master node and a single worker node, and instead deploy services over to that worker node. It'll be a lot easier (I think) to deal with gitops, building+running containers for my homelab things.

The tech stack is:
1. Proxmox VE 9 running a node on a Beelink MiniPC
    1. k8scontrolplane0: Virtual machine running Talos linux 2CPU 4gb RAM
    1. Worker0: Workin on it
1. Flux for managing the k8s installation (?)
1. GitHub for most automation
    1. Packages for container images
    1. Actions for, well, actions

