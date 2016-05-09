# ELK Kibana

This roles installs Kibana for the ELK stack.

For more information on Kibana please visit [elastic kibana](https://www.elastic.co/products/kibana).

## Example Playbook

To install:

```YAML
- name: Elk Kibana
  hosts: "{{ hosts }}"

  roles:
    - role: kibana
```

To configure:

```YAML
- name: Configure ELK Kibana
  hosts: "{{ hosts }}"

  vars_files:
    - ../js_roles/kibana/defaults/main.yml

  handlers:
    - include: ../js_roles/kibana/handlers/main.yml

  tasks:
    - name: Configure Kibana
      include: ../js_roles/kibana/tasks/configure.yml
```
