Network L3VPN CE Configuration
=========

This role will configure a CE router for L3VPN on various network vendors (still in development)

Requirements
------------
ncclient


Role Variables
--------------
* router_id: String
* bgp_global_asn: String
* bgp_groups: List
  * group: Dict
    * name: String
    * type: String
    * family_afi: String
    * family_safi: String
    * local_address: String
    * import_policy: String
    * export_policy: String
    * group_asn: String
    * neighbors: List
      * ip: String
      * asn: String

Dependencies
------------

Example Playbook
----------------

    - hosts: vmx1
      roles:
         - { role: network_l3vpn_ce_config }

License
-------

BSD

Author Information
------------------

Marc Colburn
