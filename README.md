# ansible-collection-korbad.project_management

How to bootstrap; note that 'Human' should be executed manually by a human

Human: git-clone this repo to anywhere

Human: Run the bootstrap playbook ```ansible-playbook boostrap_localhost_current_user.yml```

Automation will:
1. git-clone the repo to your user space (~/managed_projects/<name>)
2. symlink the korbad.project_management collectionn into your ~/.ansible collections path

Human:  delete the repo copy which you manually git-cloned

# Ansible Pull method (these will fail if git/ssh protocols are blocked by network policy)

```ansible-pull -U git@github.com:Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge```

```ansible-pull -U https://github.com/Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge```
