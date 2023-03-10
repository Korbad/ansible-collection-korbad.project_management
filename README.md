# ansible-collection-korbad.project_management

How to bootstrap: Execute the ansible-pull command below

Automation will:
1. git-clone the repo to your user space (~/managed_projects/<name>)
2. symlink the korbad.project_management collectionn into your ~/.ansible collections path

# Ansible Pull method (may or may not be allowed by network policy)

```ansible-pull -U git@github.com:Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge```

```ansible-pull -U https://github.com/Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge```

# To safely purge existing projects

```ansible-pull -U https://github.com/Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge safe_purge_managed_projects_localhost_current_user.yml --checkout=main```

# To provision a minimal Ansible python virtual environment

```ansible-pull -U https://github.com/Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge bootstrap_ansible_venv.yml```
