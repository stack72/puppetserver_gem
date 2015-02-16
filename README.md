# puppetserver_gem module

PLEASE NOTE: This is a direct clone of the pe_puppetserver_gem provider. This was done as a provider didn't exist for FOSS Puppet. I will make this provider compatible for both PE and FOSS in the hope that we can move away from naming conventions like `pe_puppetserver_gem`

This module provides management of Ruby gems for Puppet Server.

For Puppet Server:

    package { 'json':
      ensure   => present,
      provider => puppetserver_gem,
    }

This uses gem as a parent and uses the `puppetserver gem` command for all gem operations.

The module has been tested on both centos and debian based systems

```
root@test:~# puppet apply -e "package { 'deep_merge': ensure => present, provider => 'puppetserver_gem' }"
Notice: Compiled catalog for test.vagrant.local in environment production in 0.20 seconds
Notice: /Stage[main]/Main/Package[deep_merge]/ensure: created
Notice: Finished catalog run in 72.76 seconds
root@test:~# puppetserver gem list

*** LOCAL GEMS ***

deep_merge (1.0.1)
ffi (1.9.3 java)
jar-dependencies (0.0.9)
jruby-openssl (0.9.5 java)
json (1.8.0 java)
krypt (0.0.2)
krypt-core (0.0.2 universal-java)
krypt-provider-jdk (0.0.2)
rake (10.1.0)
rdoc (4.0.1)
```
