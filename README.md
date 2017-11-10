# minifed_deploy
This repository provides a Vangrantfile and Ansible playbook that creates, configures and launchs a minifed environment (fedoidc example), as described in http://fedoidc.readthedocs.io/en/latest/minifed.html.

## Usage
First, you have to edit the `playbook.yml` file and edit the `hostname` variable. You can leave it to `localhost` if you are just using it form your Vagrant host. But if you want to access it from outside, you should probably use your Vagrant host's name, so it can be reacheable.

The, you can create the VM and launch with
`vagrant up`

If you want to update the code to the latests version, you must `vagrant provision`. Note that this will remove any modification to the OP/RP configuration files you've done!
