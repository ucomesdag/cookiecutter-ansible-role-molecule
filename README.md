# [cookiecutter-ansible-role-molecule](#cookiecutter-ansible-role-molecule)

Cookiecutter template for creating Ansible roles with the following features:
  - molecule with podman
  - tox
  - tekton
  - github actions

## Requirements

- [python](https://www.python.org/)
- [cookiecutter](https://cookiecutter.readthedocs.io/)

## Default variables

```json
{
  "role_name": "role_name",
  "role_description": "Ansible role to install and configure {{ cookiecutter.role_name }}.",
  "role_license": ["Apache-2.0", "GPL-2.0-or-later", "GPL-3.0-only", "BSD-3-Clause", "MIT", "CC-BY-4.0"],
  "role_namespace": "ucomesdag",
  "role_dependencies": "",
  "role_collections": "",
  "molecule_collections": "containers.podman,ansible.posix",
  "role_tags": "",
  "role_topics": "ansible, role, {{ cookiecutter.role_tags }}",
  "role_platforms": "Alpine:any;Amazon:Candidate;ArchLinux:any;EL:9,8;Debian:bullseye,buster;Fedora:36,35,34,33;OpenSUSE:15.2;Ubuntu:jammy,focal,bionic",
  "role_tested": "alpine:edge,latest;amazonlinux:latest;archlinux:latest;centos:latest,stream8;debian:latest,buster;fedora:rawhide,latest,34,33;opensus:latest;rhel:latest;rocky:latest;rpi-os:latest;ubuntu:jammy,latest,bionic",
  "min_ansible_version": "2.10",
  "min_jinja_version": "2.11.2",
  "author": "Uco Mesdag",
  "company": "none",
  "homepage": "https://mesd.ag/",
  "ansible_galaxy_id": "00000",
  "github_username": "ucomesdag",
  "_copy_without_render": [
    ".github/workflows/galaxy.yml",
    ".github/workflows/molecule.yml",
    ".github/workflows/requirements2png.yml",
    ".github/workflows/todo.yml"
  ]
}
```

## Usage

```shell
cookiecutter gh:ucomesdag/cookiecutter-ansible-role-molecule
```
