# Gpu-driver-Role

[![Alma9-CI](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/alma9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/alma9-ci-caller.yml)  [![Rocky9-CI](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/rocky9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/rocky9-ci-caller.yml)  [![CentOSStream9-CI](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/centosstream9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/centosstream9-ci-caller.yml)  [![Debian12-CI](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/debian12-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/debian12-ci-caller.yml)  [![Ubuntu2204-CI](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/ubuntu2204-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-gpu-driver/actions/workflows/ubuntu2204-ci-caller.yml)

Role description

This role includes a vagrant based molecule testing setup as a submodule at `molecule/default`

## Structure

```code
📦 ansible-gpu-driver
 ┣ 📂defaults
 ┃ ┗ 📜main.yml
 ┣ 📂handlers
 ┃ ┗ 📜main.yml
 ┣ 📂meta
 ┃ ┗ 📜main.yml
 ┣ 📂 molecule
 ┃ ┗ 📂 default
 ┃   ┗ 📜, 📜, 📜, scenario_files
 ┣ 📂tasks
 ┃ ┣ 📜absent.yml
 ┃ ┣ 📜debian_amd.yml
 ┃ ┣ 📜debian_nvidia.yml
 ┃ ┣ 📜main.yml
 ┃ ┣ 📜present.yml
 ┃ ┣ 📜redhat_amd.yml
 ┃ ┣ 📜redhat_nvidia.yml
 ┃ ┗ 📜tests.yml
 ┣ 📂vars
 ┃ ┗ 📜main.yml
 ┣ 📜.gitignore
 ┣ 📜.gitmodules
 ┗ 📜README.md

```

Describe and explain role structure.

## Requirements

Elaborate external dependencies and how to use them.

## Role Variables

* defaults/main.yml
  * first_var
  * sec_var
  * third_var
* vars/main.yml
  * first_var
  * sec_var
  * third_var

## Dependencies

List role ansible-galaxy dependencies - if any.

## Example Playbook

Add an example playbook

```yaml
---

tasks:
  - name: Include ansible-gpu-driver present
    ansible.builtin.include_role:
      name: ansible-gpu-driver
    vars:
      state: present

...
```

## License

Add license - if any.

## Notes

Includes special git configuration for submodule files that are most likely to get local overrides
`.git/info/attributes`

```code
molecule/default/cleanup.yml merge=ours
molecule/default/converge.yml merge=ours
molecule/default/verify.yml merge=ours
```

## Changes to role template

* Add github action that flags empty directories on release creation
