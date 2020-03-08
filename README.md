# Ansible playbooks for Debian on WSL

These playbooks were written to quickly set up my preferred development
environment for [Debian](https://www.microsoft.com/store/productId/9MSVKQC78PK6)
running on [Windows Subsystem for Linux](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux).

## Getting started

First, upgrade system packages.

```
sudo apt-get update -y && sudo apt-get upgrade && apt-get install ssh python3-pip -y
```

For convenience, let's remove the need for a `sudo` password.

```
sudo visudo
```

Then add `username ALL=(ALL) NOPASSWD: ALL` to the bottom of the file. Now you can `sudo` without a password!

Upgrade pip (Python package manager)

```
sudo pip3 install --upgrade pip
```

Now, install Ansible using pip

```
sudo pip install ansible
```

Next, generate your SSH keys

```
ssh-keygen -t rsa -b 4096 -C "francommit@host"
```

Finally, clone this repository and run the initial setup playbook.

```
$ git clone git@github.com:francommit/ansible-wsl.git
$ cd ansible-wsl
$ ansible-playbook -i hosts setup.yml
```
