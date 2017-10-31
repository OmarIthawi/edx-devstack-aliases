# Open edX Devstack Aliases
Useful bash aliases for the edX devstack. I mainly use them to run tests
and paver commands quickly without having to SSH into my devstack.

## Warning
The aliases are highly opinionated. If you don't like
something you're welcome to submit pull requests and/or fork it!

## Aliases



## Installation
Clone this repo:
```
$ git clone https://github.com/OmarIthawi/edx-devstack-aliases.git
```

Add the following line to your `~/.bashrc` file:

```
source ~/edx-devstack-aliases/edx-devstack-aliases
```

Close your terminal and open it again!

This repo requires allowing SSH as `edxapp`. To enable that
SSH into vagrant and run the commands below.

```
$ sudo cp /home/vagrant/.ssh/authorized_keys /edx/app/edxapp/.ssh/authorized_keys
$ sudo chown edxapp:edxapp /edx/app/edxapp/.ssh/authorized_keys
$ sudo chmod 0600 /edx/app/edxapp/.ssh/authorized_keys
$ sudo vi /etc/passwd   # Change `/bin/false` to `/bin/bash` ONLY for `edxapp`
```


# Credit
The original repo was made while working at
[**@Edraak**](https://github.com/Edraak). It has been continued while
working at  [**@appsembler**](https://github.com/appsembler).
