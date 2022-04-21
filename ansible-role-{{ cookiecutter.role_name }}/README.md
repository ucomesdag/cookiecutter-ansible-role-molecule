# [{{ cookiecutter.role_name }}](#{{ cookiecutter.role_name }})

{{ cookiecutter.role_description }}

|GitHub|Version|Ansible Galaxy|Quality|Downloads|
|------|-------|--------------|-------|---------|
|[![github](https://github.com/ucomesdag/ansible-role-{{ cookiecutter.role_name }}/workflows/Ansible%20Molecule/badge.svg)](https://github.com/ucomesdag/ansible-role-{{ cookiecutter.role_name }}/actions)|[![version](https://img.shields.io/github/v/release/ucomesdag/ansible-role-{{ cookiecutter.role_name }})](https://github.com/ucomesdag/ansible-role-{{ cookiecutter.role_name }}/releases/)|[![role](https://img.shields.io/ansible/role/{{ cookiecutter.ansible_galaxy_id }})](https://galaxy.ansible.com/ucomesdag/{{ cookiecutter.role_name }})|[![quality](https://img.shields.io/ansible/quality/{{ cookiecutter.ansible_galaxy_id }})](https://galaxy.ansible.com/ucomesdag/{{ cookiecutter.role_name }})|[![downloads](https://img.shields.io/ansible/role/d/{{ cookiecutter.ansible_galaxy_id }})](https://galaxy.ansible.com/ucomesdag/{{ cookiecutter.role_name }})|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/resources/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: Converge
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: {{ cookiecutter.role_namespace }}.{{ cookiecutter.role_name }}
```

## [Role Variables](#role-variables)

These variables are set in `defaults/main.yml`:
```yaml
---
# defaults file for {{ cookiecutter.role_name }}


```

## [Dependencies](#dependencies)

Overview of role dependencies:

![dependencies](https://raw.githubusercontent.com/ucomesdag/ansible-role-{{ cookiecutter.role_name }}/png/requirements.png "Dependencies")

## [Requirements](#role-requirements)

- pip packages listed in [requirements.txt](https://github.com/ucomesdag/ansible-role-{{ cookiecutter.role_name }}/blob/master/requirements.txt).

## [Compatibility](#compatibility)

{% if cookiecutter.role_tested -%}
This role has been tested on these [container images](https://quay.io/user/ucomesdag):

|container      |tags                     |
|---------------|-------------------------|
{%- for platform in cookiecutter.role_tested.split(';') %}
  {%- set platform_name = platform.split(':')[0] -%}
  {%- set platform_versions = platform.split(':')[1] %}
|{{ "%-15s" | format(platform_name) }}|
  {%- if not platform_versions -%}
    {{ "%-11s" | format("latest") }}
  {%- else -%}
    {{ "%-25s" | format( platform_versions.replace(',', ', ') ) }}
  {%- endif -%}|
{%- endfor %}

{%- endif %}

The minimum version of Ansible required is {{ cookiecutter.min_ansible_version }}, tests have been done to:

- The previous version.
- The current version.
- The development version.

See the [Ansible community changelogs](https://docs.ansible.com/ansible/devel/reference_appendices/release_and_maintenance.html#ansible-community-changelogs) for details.

## [Exceptions](#exceptions)

Some variarations of the build matrix do not work. These are the variations and reasons why the build won't work:

| variation   | reason                                |
|-------------|---------------------------------------|
|             |                                       |


If you find issues, please register them in [GitHub](https://github.com/ucomesdag/ansible-role-{{ cookiecutter.role_name }}/issues)

## [License](#license)

{{ cookiecutter.role_license }}
