# Kibana

Master: [![Build Status](https://travis-ci.org/sansible/kibana.svg?branch=master)](https://travis-ci.org/sansible/kibana)  
Develop: [![Build Status](https://travis-ci.org/sansible/kibana.svg?branch=develop)](https://travis-ci.org/sansible/kibana)

* [Installation and Dependencies](#installation-and-dependencies)
* [Tags](#tags)
* [Examples](#examples)

This role installs Kibana.

For more information on Kibana please visit [elastic kibana](https://www.elastic.co/products/kibana).

**Note** Supports Kibana 4


## Installation and Dependencies

To install run `ansible-galaxy install sansible.kibana` or add this to your
`roles.yml`

```YAML
- name: sansible.kibana
  version: v2.0
```

and run `ansible-galaxy install -p ./roles -r roles.yml`


## Tags

This role uses two tags: **build** and **configure**

* `build` - Installs Kibana and all its dependencies.
* `configure` - Configure and ensures that the Kibana service is running.


## Examples

To install the defaul version (4.1.2):

```YAML
- name: Kibana
  hosts: "{{ hosts }}"

  roles:
    - role: kibana
```

To install RC 5

```YAML
- name: Kibana
  hosts: "{{ hosts }}"

  roles:
    - role: kibana
      sansible_kibana_tarball: "kibana-5.0.0-rc1-linux-x86_64"
      sansible_kibana_download_base_url: https://artifacts.elastic.co/downloads/kibana/
      sansible_kibana_version: 5.0.0-rc1
```

To install a specific version:

```YAML
- name: Kibana
  hosts: "{{ hosts }}"

  roles:
    - role: kibana
      kibana:
      sansible_kibana_tarball: kibana-4.5.2-linux-x64
      sansible_kibana_version: 4.5.2
```
