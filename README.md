# nvim_kickstart

Thanks Prime.

Simple galaxy collection to install nvim, or optionally just set the local users nvim folder to kickstart.

## requirements

The primitives for MacOS are still present, and some debian pacakging details, but I jettisoned everything to add Fedora support.

## Simple usage:
(local ansible)

nvim.yml:

     - hosts: localhost
       connection: local
       gather_facts: yes
       collections:
       - joshland.nvim_kickstart
       roles:
         - nvim
	 - kickstart

Installation:

	 ansible-galaxy collection install joshland/nvim_kickstart

Execution:

Run sudo first, this will let ansible _become_ when it needs to for software install

    sudo ls
	ansible-playbook) jsnvim.yml  -vv
