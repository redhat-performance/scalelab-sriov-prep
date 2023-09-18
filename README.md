sriov-prep
=========

Ansible plabook to configure SRIOV BIOS settings on Dell server


Role Variables
--------------

    # Your allocation name/number in the shared labs
    cloud_name: cloud30
    # Lab name, typically can be alias or scale
    lab_name: scale

    alias:
    #lab specific vars, leave default
      lab_url: "http://quads.example.com"
    scale:
    # lab specific vars, leave default
      lab_url: "http://quads.example.com"



Example Playbook
----------------


    - hosts: localhost
      roles:
         - { role: sriov-prep }

Execution
---------

    ansible-playbook playbook.yml -e "cloud_name=cloud30 lab_name=scale"


To only enable SR-IOV on selected nodes, provide the list of nodes mgmt address

```yaml
nodes_pm_addr:
- mgmt-e24-h03-000-r640.example.com
- mgmt-e24-h05-000-r640.example.com
```
