---
title: Getting Started with Exosuit
---

## Installation
```shell
$ brew tap jasonswett/exosuit && brew install exosuit
$ exo --version
```

## Usage

As of this writing Exosuit can:

- Launch an EC2 instance
- Install Ruby and nginx on an EC2 instance
- Terminate EC2 instances
- List EC2 instances
- SSH into an EC2 instance

Exosuit does not yet do anything to do with installing Rails, although that of course is in the plans.

### Launching an EC2 instance

You can launch an EC2 instance by using the `launch` command:
```shell
$ exo launch
```

The `launch` command will create a new key pair for you (unless one already exists) inside the `~/.ssh` and associate that keypair with your new EC2 instance.

Within a few seconds, your EC2 instance will be ready and Exosuit will show you the public DNS for that instance.

### Listing your EC2 instances

You can check on your EC2 instance by running the `instances` command, which will list the public DNS names for any running EC2 instances you have.

```shell
$ exo instances
```

To see all your instances, not just running instances, use `instances:all`:

```shell
$ exo instances:all
```

### SSHing into your EC2 instances

You can SSH into an EC2 instance by running the `ssh` command. You will be given a prompt to select which instances to SSH into.

```shell
$ exo ssh
```

## Terminating an EC2 instance

To terminate an instance, run:

```shell
$ exo terminate
```

You will be given a prompt of all your running instances. You can select any number of instances to terminate.

## Getting help

If you run the `exo` command, you'll see some help output, which will look something like this:

```shell
Usage:
  exo [command]

These are the commands you can use:
  launch                 Launch a new EC2 instance
  terminate              Terminate an EC2 instance
  instances              Show a summary of all running EC2 instances
  instances:all          Show a summary of EC2 instances (all states)
  dns                    List public DNS names for all EC2 instances
  ssh                    SSH into an EC2 instance
  initialize             Install Ruby and nginx on an instance
```
