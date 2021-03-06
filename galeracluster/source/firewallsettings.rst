=============================
 Firewall Settings
=============================
.. _`Firewall Settings`:
.. index::
   pair: iptables; Firewall settings
.. index::
   single: iptables; Ports
.. index::
   single: Firewall settings; Ports

Galera Cluster requires a number of ports in order to maintain network connectivity between the nodes.  Depending on your deployment, you may require all or some of these ports on each node in the cluster:

- ``3306`` For MySQL client connections and State Snapshot Transfers that use the ``mysqldump`` method.

- ``4567`` For Galera Cluster replication traffic, multicast replication uses both UDP transport and TCP on this port.

- ``4568`` For Incremental State Transfers.

- ``4444`` For all other State Snapshot Transfers.

How to open these ports for Galera Cluster can vary depending upon your distribution and what you use to configure the firewall.  

.. toctree::
   :maxdepth: 2
   
   iptables
   pf
