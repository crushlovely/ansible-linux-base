# Ansible Role For A Base Linux System

[![Build Status](https://circleci.com/gh/crushlovely/ansible-linux-base.svg?style=shield)](https://github.com/crushlovely/ansible-linux-base)
[![Current Version](http://img.shields.io/github/release/crushlovely/ansible-linux-base.svg?style=flat)](https://galaxy.ansible.com/list#/roles/1362)

This Ansible role that updates `apt` and upgrades all packages. It then installs the following packages:

* `git`
* `ntp`
* `unattended-upgrades`
* `build-essential`
* `libreadline6`
* `libreadline6-dev`
* `curl`
* `zlib1g`
* `zlib1g-dev`
* `libssl-dev`
* `libyaml-dev`
* `libsqlite3-dev`
* `sqlite3`
* `libxml2-dev`
* `libxslt1-dev`
* `autoconf`
* `libc6-dev`
* `libncurses5-dev`
* `automake`
* `libtool`
* `bison`
* `pkg-config`

Finally it sets the default timezone for the server.  We use this as the base image for all our Ruby and Node.js applications.

## Installation

``` bash
$ ansible-galaxy install crushlovely.linux-base,v1.0.0
```

## Variables

``` yaml
time_zone: UTC
```

## Usage

Once this role is installed on your system, include it in the roles list of your playbook.

``` yaml
---
- hosts: localhost
  roles:
    - crushlovely.linux-base
```

## Dependencies

None

## License

MIT