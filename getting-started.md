---
title: Getting Started with Exosuit
---

## Installation

The [Exosuit CLI]({% link exosuit-cli.md %}) currently only works on macOS.
The Exosuit CLI can be installed using [Homebrew](https://brew.sh/).

```shell
$ brew tap jasonswett/exosuit && brew install exosuit
$ exo --version
```

## Usage

As of this writing Exosuit can:

- Launch an EC2 instance
- SSH into an EC2 instance
- Terminate EC2 instances
- List EC2 instances

Exosuit does not yet do anything to do with installing Rails, although that of course is in the plans.

### Launching an EC2 instance

You can launch an EC2 instance by using the `launch` command:
```shell
$ exo launch
```

Within a few seconds, your EC2 instance will be ready.

### SSHing into your EC2 instance

The next thing you might want to do is SSH into the instance you just created.
You can do that like this:

```shell
$ exo ssh
```

### Listing your EC2 instances

Want to see all the instances you've launched? Run this command.

```shell
$ exo instances
```

## Terminating an EC2 instance

To terminate an instance, run:

```shell
$ exo terminate
```

You will be given a prompt of all your running instances.
You can select any number of instances to terminate.

## Getting help

If you run the `exo` command, you'll see some help output, which will look something like this:

```shell
Usage:
  exo [command]

These are the commands you can use:
  launch                 Launch a new EC2 instance
  ssh                    SSH into an EC2 instance
  terminate              Terminate an EC2 instance
  instances              Show a summary of all running EC2 instances
  instances:all          Show a summary of EC2 instances (all states)
```
