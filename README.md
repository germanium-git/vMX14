# vMX14
Ansible playbooks for configuring vMX routers


### Merge with existing configuration

ansible-playbook junos_config/pref-list_merge_xml_pb.yml -i hosts


### Replace existing configuration

ansible-playbook junos_config/pref-list_replace_xml_pb.yml -i hosts

- The xml configuration must include the replace="replace" attribute in the opening container tag.
- The parameter of junos_config update of must be set to replace    

```sh
<policy-options>
    <prefix-list replace="replace">
    ...
```

