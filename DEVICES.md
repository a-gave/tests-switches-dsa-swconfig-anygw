## Devices
All running libremesh-master-ow2024.2 built with firmware-selector/imagebuilder
asus without shared-state-async

- name: Cudy WR3000S v1
  hostname: cudy
  target: mediatek/filogic
  switch: DSA
  ipv4: 10.13.15.35
  eth_ports: 4xLAN 1xWAN
  radios: 2ghz 5ghz

- name: Asus RT-AC51U
  hostname: asus
  target: ramips/mt7620
  switch: swconfig
  ipv4: 10.13.135.8
  eth_ports: 4xLAN 1xWAN
  radios: 2ghz 5ghz

- name: OpenWrt One
  hostname: openwrt
  target: mediatek/filogic
  switch: swconfig
  ipv4: 10.13.4.128
  eth_ports: 1xLAN 1xWAN
  radios: 2ghz 5ghz

- name: MikroTik 
  hostname: mikrotik
  target: ipq40xx/mikrotik
  switch: dsa
  ipv4: 10.13.x.x
  eth_ports: 1xLAN
  radios: 5ghz
