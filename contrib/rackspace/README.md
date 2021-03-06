# Heat resources for working with the Rackspace Cloud
The resources and configuration in this module are for using Heat with the Rackspace Cloud. These resources either
allow using Rackspace services that don't have equivalent services in OpenStack or account for differences between
a generic OpenStack deployment and Rackspace Cloud.

### 1. Install the Rackspace plugins in Heat

NOTE: These instructions assume the value of heat.conf plugin_dirs includes the
default directory /usr/lib/heat.

To install the plugin, from this directory run:
    sudo python ./setup.py install

### 2. Restart heat

Only the process "heat-engine" needs to be restarted to load the newly installed
plugin.


## Resources
The following resources are provided for compatibility:

* `Rackspace::Cloud::Server`:
>Provide compatibility with `OS::Nova::Server` and allow for working `user_data` and `Metadata`. This is deprecated and should be replaced with `OS::Nova::Server` once service compatibility is implemented by Rackspace.  

* `Rackspace::Cloud::LoadBalancer`:
>Use the Rackspace Cloud Loadbalancer service; not compatible with `OS::Neutron::LoadBalancer`.  

* `Rackspace::Cloud::DatabaseInstance`:
>Use the Rackspace implementation of Trove. This is deprecated and should eventually be replaced with `OS::Trove::Instance` or similar.  

## Usage
### Templates
### Configuration
