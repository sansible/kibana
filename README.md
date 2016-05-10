# Kibana

Master: [![Build Status](https://travis-ci.org/sansible/kibana.svg?branch=master)](https://travis-ci.org/sansible/kibana)  
Develop: [![Build Status](https://travis-ci.org/sansible/kibana.svg?branch=develop)](https://travis-ci.org/sansible/kibana)

* [ansible.cfg](#ansible-cfg)
* [Installation and Dependencies](#installation-and-dependencies)
* [Tags](#tags)
* [Examples](#examples)

This roles installs Kibana for the ELK stack.

For more information on Kibana please visit [elastic kibana](https://www.elastic.co/products/kibana).




## ansible.cfg

This role is designed to work with merge "hash_behaviour". Make sure your
ansible.cfg contains these settings

```INI
[defaults]
hash_behaviour = merge
```




## Installation and Dependencies

To install run `ansible-galaxy install sansible.kibana` or add this to your
`roles.yml`

```YAML
- name: sansible.kibana
  version: v1.0
```

and run `ansible-galaxy install -p ./roles -r roles.yml`




## Tags

This role uses two tags: **build** and **configure**

* `build` - Installs Kibana and all it's dependencies.
* `configure` - Configure and ensures that the Kibana service is running.




## Examples

To install:

```YAML
- name: Elk Kibana
  hosts: "{{ hosts }}"

  roles:
    - role: kibana
```
