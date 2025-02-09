# Creation of a test VM

To be able to run tests on my lab, I'm going to create 2 test machines.
A debian VM and a Winows VM.

## Creation of Debian test VM

### Add Debian ISO to Datastores

First, I need to add the Debian ISO to the datastores.
I'm going to use the ISO from the [Debian website](https://www.debian.org/distrib/).

Once the ISO is downloaded onto the computer, we can send it to our datastore.

1. Go to `Inventory -> Storage` and select the datastore where you want to
upload the ISO. Here I'm going to use `HS-DS-01` (the first high-speed
datastore of the first ESX).
2. Go to the `Files` tab.
3. Click on `New Folder` and create a folder for ISOs (in my case `_ISO`).
4. In the right panel of the `Files` tab, click on your new folder.
5. Click on `Upload Files` and select the Debian ISO.

### Copy the ISO to the datastore of the other ESX

Now that the ISO is on the first ESX, we need to copy it to the second ESX.

1. Go to `Inventory -> Hosts and Clusters` and select the datastore where
you stored the Debian ISO.
2. Go to the `Files` tab and select the ISO folder.
3. Click on `Copy to` and select the target datastore (in my case `HS-DS-02`).

### Create the Debian Test VM

1. Go to `Inventory -> Hosts and Clusters` and right click on the ESX you
want to install the Debian VM to.
2. Click on `New Virtual Machine`.
3. Select `Create a new virtual machine` and click `Next`.
4. Virtual machine name: `Debian-test`.
5. Location for the virtual machine: `DC-homelab`.
6. Select the ESX where you want to install the VM.
7. Select the datastore: `HS-DS-01`.
8. Select the compatibility: `ESXi 8.0 U2 and later`.
9. Guest OS Family: `Linux`.
10. Guest OS Version: `Debian 12 (64-bit)`.

Here's the configuration I've put in for the hardware:

1. CPU: `4`.
2. Memory: `8Gb`.
3. Hard disk: `20Gb` (thin provisioned).
4. Network: `VMNet`.
5. CD/DVD drive: `Datastore ISO file` and select the Debian ISO.
Don't forget to check the `Connect at power on` box.

We can now run our Debian VM and proceed with the installation.
