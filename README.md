# Side-Protocol-Install-Node-Guide

![images](https://github.com/user-attachments/assets/bace43eb-f564-4318-9a40-8583fa426568)


This guide will help you through the installation and configuration of the `sided` binary.

## Hardware Specifications
### Recommended Specifications

- **CPU**: 8 cores
- **RAM**: 16 GB
- **Storage**: 800 GB
- **Network**: 1 Gbps

## Operating System

You can choose any operating system that suits your preference, as the `sided` daemon can be compiled on a variety of modern Linux distributions as well as recent versions of macOS.

This guide assumes you are using an Ubuntu LTS release. If you are using a different OS, you may need to adjust the commands accordingly.

## Prerequisites

Make sure you have Go version 1.22.0 installed. You can download the latest version and follow the installation instructions from the [official Go website](https://go.dev/dl/).

## Building `sided` from Source

### Step 1: Verify Golang Installation

First, ensure that the correct version of Go is installed on your system:

```bash
go version
```

The output should match the version specified in the prerequisites.

### Step 2: Clone the Repository

Next, you'll need to clone the `side` repository and navigate to the appropriate directory:

> **Note**: If you have an existing `side` directory from a previous clone, it's recommended to delete it before proceeding.

```bash
git clone https://github.com/sideprotocol/side.git
cd side
git checkout v0.9.0
```

### Step 3: Compile the `sided` Binary

Now, you can compile the `sided` binary using the following command:

```bash
make install
```

This will compile the binary and place it in your `$GOBIN` directory. If your `$GOBIN` is included in your `$PATH`, you should be able to run the `sided` binary directly.

### Step 4: Update Environment Variables

If needed, update your environment variables to ensure the binary can be executed:

```bash
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```

### Step 5: Verify the Installation

Finally, check the installed version of `sided` to confirm everything is set up correctly:

```bash
sided version
```

You should see output similar to:

```
0.9.0
```

If you run into any issues related to the `$PATH` settings, refer to the Go installation guide provided in the prerequisites.
