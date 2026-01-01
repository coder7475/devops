# VMs vs. Containers

Containers = Docker
Virtual Machine = Hypervisors

## Linux keep tracks of 4 things:

1. Memory
2. CPU (Processors)
3. Disk
4. Devices

## Running a program in a VM or Container

Each program in a VM/Container will have its **own version of shared resources like files and network ports**

## How containers work:

Containers work by creating "namespaces"(sandbox), which are a linux feature that group shared resources together. For example, if you have five processors running together within a docker container, they'd still be running within linux itself

## How VMs Work:

- Idea behind containers are to create a "fake" version of Linux
- The idea for VMs is to **provide "fake" versions of the CPU, ram, disk, and devices**. That is, VM's are "faking" one level deeper.

## VMs vs. Containers Performance

- Various benchmarks show that the CPU in VMs is 10-20% slower than containers.
- VMs also usually use 50-100% more storage (Containers don't need all of the file that operating system would need)
- Finally, VMs use ~200mb of memory each for the 'inner operating system', whereas containers have essentially has no memory overhead

## When VMs are the better choice:

- **If you are running untrusted (e.g., user supplied) code**, it's difficult to be confident that they can't "escape" a container.
- **If you are running, e.g a Windows or MacOS guest within a Linux server**
- Finally, **you can emulate hardware devices (like graphics cards)** with a VM
