# anygw not working via cable in dsa devices


## utils

watch bridge fdb
```
while true; do sleep 1; clear; date ; bridge fdb | grep aa;  echo ""; done
```

## workarounds
1. set devices on different batman networks and use only babeld
2. manual configuration, example_1: 
    - swconfig_device:
      * remove the port from being member of br-lan, creating a switch_vlan on it
    - dsa_devices:
      * remove the network device lan1 from br-lan
3. ? on dsa_device: disable learning on dsa_user ports?802
4. ? on dsa_device: create mesh protocols 
5. ? on dsa_device: setup a different dns/dhcp instance for br-dsa?
6. ? on dsa_device: run mesh protocols on 802.1ad on top of br-dsa or on a 802.1q untagged vlan built on br-dsa
7. ? on dsa_device: block dhcpoffer of anygw coming from swconfig_device

## Possibly related issues?
https://github.com/openwrt/openwrt/issues/11650
https://github.com/openwrt/openwrt/issues/9706
https://github.com/rany2/openwrt/commit/052ac07fcf47e9d6d84576ea8b99025e3834e6d5

