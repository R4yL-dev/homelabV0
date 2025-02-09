# Setup vCenter

## Adding the vCenter license

As usual, we'll start by looking at the licences.

1. Go to `Administration -> Licensing -> Licenses -> Licenses` and click on `ADD`.
2. Enter the key in the text field and click `Next`.
3. License name: `vCenter 8 Standard`.

> **Note**: The [magic repository](https://gist.github.com/ayebrian/646775424393c9a35fb8257f44df1c8b)
has everything you need in the way of keys.

### Activate the vCenter key

We've added a licence to our invention. Now we need to assign it to our vCenter.

1. Go to `Administration -> Licensing -> Licenses -> Assets`.
2. Select the vCenter and click on `Assign License`.
3. Select the license (`vCenter 8 Standard`) and click `Ok`.

The vCenter is now finally activated and should no longer cause any licensing problems.

## Creation of the Datacenter

Now that the vCenter is activated, we can create the Datacenter
that will enable us to manage our ESXs.

1. Go to `Inventory -> Hosts and Clusters`.
2. Right-click on the vCenter and select `New Datacenter`.
3. Name: `DC-homelab`.
4. Click `Ok`.

## Adding ESXs to the Datacenter

Now that the Datacenter is created, we can add our ESXs to it.

1. Go to `Inventory -> Hosts and Clusters`.
2. Right-click on the Datacenter and select `Add Host`.
3. Host name or IP address: `192.168.1.10` or `192.168.1.11` (it depends on the host).
4. Username: `root`.
5. Password: `<my_super_password>`.
6. Manage host with an image: `Yes`.
7. Compose a new image: `Yes`.

> **Note**: Adding an ESX to the Datacenter takes a little time. You can see the
progress at the bottom of the page in Recent Tasks. \
> **Note**: You need to add all the ESXs.

## Delete the default Datastore

By default, the vCenter creates a Datastore on the ESX. We will delete it.

1. Go to `Inventory -> Storage`.
2. Right-click on the Datastore and select `Delete`.

> **Note**: The Datastore is not deleted on the ESX, only on the vCenter.
