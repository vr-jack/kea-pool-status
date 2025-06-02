Very basic script. Haven't added any support for tls or auth. It loops through the subnets and the shared subnets to list the pool usage/total allocated.

The version of Kea (2.6.2) that was tested against appears to combine the pools into a single pool for the purpose of statistics. The script checks to see if other pool indexes exist just in case it changes.

Example output:

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
                    192.168.88.0/24              2        11
                    Total                        2        11
