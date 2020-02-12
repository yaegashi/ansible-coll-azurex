# Ansible Collection - yaegashi.azurex

Experimental plugin collection for Azure.

## filter: azure_rids

Example playbook: [tests/test_azure_rids.yml](tests/test_azure_rids.yml)

```console
$ ansible-playbook tests/test_azure_rids.yml 
PLAY [localhost] ***************************************************************

TASK [Test azure_rids filter] **************************************************
ok: [localhost] => (item=/subscriptions/11111111-1111-1111-1111-111111111111/resourceGroups/RG1/providers/Microsoft.Compute/virtualMachines/VM1) => {
    "msg": {
        "children": "",
        "name": "VM1",
        "namespace": "Microsoft.Compute",
        "resource_group": "RG1",
        "resource_name": "VM1",
        "resource_namespace": "Microsoft.Compute",
        "resource_parent": "",
        "resource_type": "virtualMachines",
        "subscription": "11111111-1111-1111-1111-111111111111",
        "type": "virtualMachines"
    }
}
ok: [localhost] => (item=/subscriptions/22222222-2222-2222-2222-222222222222/resourceGroups/RG2/providers/Microsoft.Network/virtualNetworks/VNET1/subnets/SUBNET1) => {
    "msg": {
        "child_name_1": "SUBNET1",
        "child_parent_1": "virtualNetworks/VNET1/",
        "child_type_1": "subnets",
        "children": "/subnets/SUBNET1",
        "last_child_num": 1,
        "name": "VNET1",
        "namespace": "Microsoft.Network",
        "resource_group": "RG2",
        "resource_name": "SUBNET1",
        "resource_namespace": "Microsoft.Network",
        "resource_parent": "virtualNetworks/VNET1/",
        "resource_type": "subnets",
        "subscription": "22222222-2222-2222-2222-222222222222",
        "type": "virtualNetworks"
    }
}
ok: [localhost] => (item=/subscriptions/33333333-3333-3333-3333-333333333333/resourceGroups/RG3/providers/Microsoft.Compute/galleries/SIG1/images/DEF1/versions/1.2.3) => {
    "msg": {
        "child_name_1": "DEF1",
        "child_name_2": "1.2.3",
        "child_parent_1": "galleries/SIG1/",
        "child_parent_2": "galleries/SIG1/images/DEF1/",
        "child_type_1": "images",
        "child_type_2": "versions",
        "children": "/images/DEF1/versions/1.2.3",
        "last_child_num": 2,
        "name": "SIG1",
        "namespace": "Microsoft.Compute",
        "resource_group": "RG3",
        "resource_name": "1.2.3",
        "resource_namespace": "Microsoft.Compute",
        "resource_parent": "galleries/SIG1/images/DEF1/",
        "resource_type": "versions",
        "subscription": "33333333-3333-3333-3333-333333333333",
        "type": "galleries"
    }
}

PLAY RECAP *********************************************************************
localhost                  : ok=1    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
```