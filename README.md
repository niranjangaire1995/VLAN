A Clinic that only Requires 5 Computers in IT for telemedication, 2 For Registration, and 3 computers for Finance Department.
The Network Address they use is : 10.0.0.0/24

After VLSM the Ip for
IT: 10.0.0.1/ 29,                    .2, .3, .4, .5, .6, .7
Finance: 10.0.0.9/ 29,               0.10, .11, .12, .13, .14, .15,
Registration: 10.0.0.17/ 30,        .18, .19 

Setting VLAN Names:                                     IT   ->    Vlan 10          ->     Finance ->   Vlan 20   ->   Registration   ->   Vlan 30
Switch>
Switch>enable
Switch#config t
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#vlan 10
Switch(config-vlan)#name IT
Switch(config-vlan)#exit
Switch(config)#vlan 20
Switch(config-vlan)#name FINANCE
Switch(config-vlan)#exit
Switch(config)#vlan 30 
Switch(config-vlan)#name REGISTRATION
Switch(config-vlan)#exit
Switch(config)#
