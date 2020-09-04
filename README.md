sriov-prep
=========

Ansible role to configure SRIOV BIOS settings on Dell server


Role Variables
--------------

    # Your allocation name/number in the shared labs
    cloud_name: cloud30
    # Lab name, typically can be alias or scale
    lab_name: scale

    alias:
    #lab specific vars, leave default
      lab_url: "http://quads11.alias.bos.scalelab.redhat.com"
    scale:
    # lab specific vars, leave default
      lab_url: "http://quads.rdu2.scalelab.redhat.com"



Example Playbook
----------------


    - hosts: localhost
      roles:
         - { role: sriov-prep }
