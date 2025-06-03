Very basic script. Haven't added any support for tls or auth. It loops through the subnets and the shared subnets to list the pool usage/total allocated.

If you give a pool-id to pools, it will show them individually. Pools without ids get combined as pool-id 0 and are displayed combined.

Example output:

```
Name                Network                   Used     Total
------------------------------------------------------------
Unshared Subnets
                    192.168.99.0/24              0        69
                    192.168.100.0/24             0       253
customer-networks
                    192.168.0.0/24               0       253
                    192.168.1.0/24               0       253
                    192.168.2.0/24               0       253
                    192.168.3.0/24               0       253
                    192.168.4.0/24               0       253
                    192.168.5.0/24               0       253
                    192.168.6.0/24               0       253
                    192.168.7.0/24               0       253
                    192.168.8.0/24               0       253
                    192.168.9.0/24               0       253
                    192.168.10.0/24              0       253
                    Total                        0      2783
mgmt-networks
                    10.0.16.0/20                 0      3838
                    Total                        0      3838
test-networks
                    192.168.88.0/24-1            1         4
                    192.168.88.0/24-2            1         7
                    Total                        2        11
```
