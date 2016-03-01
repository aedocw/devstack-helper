# devstack-helper
A shell script to give you a devstack config with neutron
(OVS or Linuxbridge) on a single-nic VM

If you ever have a need to spin up a [Devstack](http://devstack.org)
instance you have probably discovered it can get complicated
if you need to play with Neutron. After having run into
issues multiple times (usually because I forget one line, or
set something True instead of False), I finally made a quick
shell script to create my local.conf config file.

This script assumes you are running devstack in a VM (and
SERIOUSLY, you should only ever do that, never run it on a
machine you care about because it will wreck things!). It
also assumes you're running the VM under something like KVM,
VMWare Fusion or VirtualBox with a *single* NAT'd nic. The
script will set up the Devstack instance with the provider
network, under a single NIC. This one also configures
the [App Catalog](http://apps.openstack.org) UI (a Horizon
panel).  Have fun with it!
