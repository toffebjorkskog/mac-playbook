# Genero Mac Development Ansible Playbook

This playbook installs required Mac tools for developers at Genero. The playbook contained in this repo does nothing except delegate all functionality to [`geerlingguy/mac-dev-playbook`](https://github.com/geerlingguy/mac-dev-playbook)'s playbook.

*See also*:

- [`geerlingguy/mac-dev-playbook`](https://github.com/geerlingguy/mac-dev-playbook) (the actual playbook used to provision)
- [`generoi/dotfiles`](https://github.com/generoi/dotfiles) (Genero dotfiles not installed but a suggestion)

## Installation

    # Clone this repository to your local drive.
    git clone --recursive https://github.com/generoi/mac-playbook.git
    cd mac-playbook

    # Install dependencies.
    make install

    # Run the playbook.
    make provision

### Running a specific set of tagged tasks

You can filter which part of the provisioning process to run by specifying a set of tags using `ansible-playbook`'s `--tags` flag. The tags available are `dotfiles`, `homebrew`, `mas` and `osx`.

    ansible-playbook main.yml -i geerlingguy.mac-dev-playbook/inventory -K --tags "dotfiles,homebrew"
