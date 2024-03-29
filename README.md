# ansible-collection-korbad.project_management

How to bootstrap: Execute the ansible-pull command below

Automation will:
1. git-clone the repo to your user space (~/managed_projects/<name>)
2. symlink the korbad.project_management collectionn into your ~/.ansible collections path

# Ansible Pull method (may or may not be allowed by network policy)

using git/ssh:

```ansible-pull -U git@github.com:Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge```

using https:

```ansible-pull -U https://github.com/Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge```

# Safely purge content

To safely purge existing managed (version controlled) content:

using git/ssh

```ansible-pull -U git@github.com:Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge isolated-safe_purge.yml --checkout=main```

using https:

```ansible-pull -U https://github.com/Korbad/ansible-collection-korbad.project_management.git -i localhost, --accept-host-key --clean --purge isolated-safe_purge.yml --checkout=main```

