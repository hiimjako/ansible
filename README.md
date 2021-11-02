# Run ansible

1. `pacman -S ansible`
2. `ansible-galaxy collection install -r requirements.yml`
3. `sudo ansible-pull -U {{github repo}} local.yml`
