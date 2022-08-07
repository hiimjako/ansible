# Run ansible

Installare prima:
1. `ansible`
2. `git`

1. `pacman -S ansible`
2. `ansible-galaxy collection install -r requirements.yml`
3. `sudo ansible-pull -U https://{{https://github.com/settings/tokens}}:x-oauth-basic@github.com/hiimjako/ansible.git local.yml --vault-password-file {{path}}`

# Vars:
Take a look on vars for customize ansible `roles/workstation/vars`

# Tags
- init: Basic tags for the first ansible run on fresh install
    - Includes all the next
- packages: installs the core packages for os (apt/pacman)
- Os specific:
    - Ubuntu: 
    - Arch: 
- Software specific:
    - ssh: installs ssh keys
    - git: configure git
    - nodejs: installs node, nvm and npm
    - nvim: installs nvim 
    - zsh: installs zsh and ohmyzsh
- Repos:
    - dotfiles: install the personal dotfile repo

# Bug
1. Se lanciato tramite remote repo con un tag che usa `ansible_distribution` non funzionerà, c'è da fare il pull e poi avviarlo da li
    - fix, metto always per i pacchetti
