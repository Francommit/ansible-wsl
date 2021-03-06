# Ansible playbooks for Debian on WSL

These playbooks were written to quickly set up my preferred development
environment for [Debian](https://www.microsoft.com/store/productId/9MSVKQC78PK6)
running on [Windows Subsystem for Linux](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux).

## Attempted one-liner

Grab a coffee, and hopefully return to a setup terminal

```
sudo apt-get update -y && sudo apt-get upgrade -y && sudo apt-get install ssh git ansible -y && git clone https://github.com/Francommit/ansible-wsl.git && cd ansible-wsl && sudo ansible-playbook -i hosts setup.yml
```

## Re-run Ansible Palybook

Same as above:

```
sudo ansible-playbook -i hosts setup.yml
```
