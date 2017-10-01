# Ansible scripts to setup a L2TP/IPsec VPN server on a RPi

This ansible playbook implements @ritazh's [blog post](https://ritazh.com/setup-your-own-l2tp-vpn-server-with-raspberry-pi-170d3d4df04c) on how to setup your own L2TP/IPsec VPN server on a Raspberry Pi device. Check out Rita Zhang's blog post to find the answer to why, what and how questions.

## Howto

1. Make sure your Raspberry Pi's ip address is static.
1. Forward UDP port 500 and UDP port 4500 from your Router/Gateway to your Raspberry Pi.
1. Copy `config.yml.example` to `config.yml` and change the settings according to you own setup.
1. Run setup playbook
```
ansible-playbook -i 'RPI_ADDRESS,' -u RPI_USER_ID -k setup.yml
```

## Compatibility

These scripts have been tested on a Raspberry Pi 3 running Raspbian Stretch 9, while executing the playbook using Ansible 2.2.1.0 on OS X 10.12.6.
