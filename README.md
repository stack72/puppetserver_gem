# puppetserver_gem module

This module provides management of Ruby gems for Puppet Server.


For Puppet Server:

    package { 'json':
      ensure   => present,
      provider => puppetserver_gem,
    }

This uses gem as a parent and uses the puppetserver gem` command for all gem operations.

PLEASE NOTE: This is a direct clone of the pe_puppetserver_gem provider. This was done as a provider didn't exist for FOSS Puppet.

The module has been tested on both centos and debian based systems
