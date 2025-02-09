# Install vCenter

To manage my 2 ESXs, I'm going to install vCenter.
To do the installation, I'm going to use the VCSA and its GUI.

I chose to deploy the vCenter on the first ESX (192.168.1.10).

As I'm doing a new installation and not an upgrade or
migration, I'm going to choose Install.

## vCenter Server deployement target

1. ESXi host or vCenter Server: `192.168.1.10`.
2. HTTPS port: `443`.
3. User name: `root`.
4. Password: `<my_super_password>`.

## Set up vCenter Server VM

1. VM name: `vcs01`.
2. Set root password: `<my_super_password>`.
3. Confirm root password: `<my_super_password>`.

## Select deployment size

1. Deployment size: `Tiny`.
2. Storage size: `Default`.

## Select datastore

1. Datastore: `HS-DS-01`.
2. Enable Thin Disk Mode: `Yes`.

## Configure network settings

1. Network: `VMNet`.
2. IP version: `IPv4`.
3. IP assignment: `Static`.
4. FQDN: `none`.
5. IP address: `192.168.1.20`.
6. Subnet mask: `255.255.255.0`.
7. Default gateway: `192.168.1.1`.
8. DNS servers: `62.2.24.162,62.2.17.60`.
9. HTTP: `80`.
10. HTTPS: `443`.
11. Mac Address Prefix: `none`.
12. Prefix Length: `none`.

## vCenter Server Configuration

1. Time synchronization: `Synchronize time with the NTP servers`.
2. NTP servers: `0.ch.pool.ntp.org,1.ch.pool.ntp.org,2.ch.pool.ntp.org,3.ch.pool.ntp.org`.
3. SSH access: `Activated`.

## SSO Configuration

1. Create a new SSO domain: `Yes`.
2. Single Sign-On domain name: `vsphere.local`.
3. Single Sing-On username: `administrator`.
4. Single Sign-On password: `<my_super_password>`.
5. Confirm password: `<my_super_password>`.
